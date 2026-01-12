import React, { useState, useMemo } from 'react';
import { Folder, FileText, ChevronRight, ChevronDown, MapPin, Anchor, Scale, AlertTriangle, Layers, Zap } from 'lucide-react';

// --- Types ---
type NodeType = 'root' | 'category' | 'folder' | 'page' | 'hub' | 'article';

interface SitemapNode {
  id: string;
  label: string;
  type: NodeType;
  icon?: React.ReactNode;
  children?: SitemapNode[];
  meta?: string; // For SEO notes
}

// --- Data Generation ---

// Standard Service Suites for Cities
const coastalSuite = [
  "Structural Forensic Assessment",
  "Condo Milestone Inspection (SB 4-D)",
  "Expert Witness Services",
  "Flood vs. Wind Damage Claims",
  "Seawall & Marine Inspection"
];

const inlandSuite = [
  "Structural Forensic Assessment",
  "Expert Witness Services",
  "Roof Damage Assessment",
  "Sinkhole & Foundation Analysis",
  "Construction Defect Claims"
];

// Helper to generate city nodes
const createCityHub = (cityName: string, suite: string[], specials: string[] = []): SitemapNode => ({
  id: `loc-${cityName.toLowerCase().replace(/\s/g, '-')}`,
  label: `${cityName} Hub`,
  type: 'hub',
  children: [
    ...suite.map((svc, i) => ({
      id: `page-${cityName}-${i}`,
      label: `${cityName} ${svc}`,
      type: 'page' as NodeType,
    })),
    ...specials.map((svc, i) => ({
      id: `page-${cityName}-special-${i}`,
      label: `${cityName} ${svc}`,
      type: 'page' as NodeType,
      meta: 'High Value Niche'
    }))
  ]
});

const sitemapData: SitemapNode = {
  id: 'root',
  label: 'meforensics.com',
  type: 'root',
  children: [
    // 1. Core Navigation
    {
      id: 'core',
      label: 'Core Navigation',
      type: 'category',
      icon: <Layers className="w-4 h-4" />,
      children: [
        { id: 'home', label: 'Home (The Florida Horseshoe USP)', type: 'page' },
        { id: 'about', label: 'About Us', type: 'folder', children: [
          { id: 'team', label: 'Our Team (CVs)', type: 'page' },
          { id: 'certs', label: 'Certifications (WBE, Licenses)', type: 'page' },
          { id: 'map', label: 'Service Area Map', type: 'page' },
        ]},
        { id: 'contact', label: 'Contact / Intake', type: 'page' }
      ]
    },

    // 2. Service Silos
    {
      id: 'services',
      label: 'Service Silos (Capabilities)',
      type: 'category',
      icon: <Zap className="w-4 h-4" />,
      children: [
        { id: 'svc-forensic', label: 'Forensic Engineering', type: 'folder', children: [
          { id: 'fail-analysis', label: 'Structural Failure Analysis', type: 'page' },
          { id: 'origin-cause', label: 'Origin & Cause', type: 'page' },
          { id: 'fire-struct', label: 'Fire Damage Structural Assessment', type: 'page' },
          { id: 'vehicle-impact', label: 'Vehicle Impact Analysis', type: 'page' }
        ]},
        { id: 'svc-legal', label: 'Expert Witness & Legal', type: 'folder', children: [
           { id: 'constr-defect', label: 'Construction Defect Witness', type: 'page' },
           { id: 'premises', label: 'Premises Liability (Trip & Fall)', type: 'page' },
           { id: 'umpire', label: 'Insurance Appraisal Umpire', type: 'page' }
        ]},
        { id: 'svc-condo', label: 'Condo & HOA (SB 4-D)', type: 'folder', children: [
           { id: 'milestone', label: 'Milestone Inspections', type: 'page', meta: 'CRITICAL FL LAW' },
           { id: 'sirs', label: 'SIRS Reserve Studies', type: 'page' },
           { id: 'turnover', label: 'Turnover Reports', type: 'page' }
        ]},
        { id: 'svc-disaster', label: 'Disaster Response', type: 'folder', children: [
           { id: 'hurricane', label: 'Hurricane Damage Assessment', type: 'page' },
           { id: 'wind-water', label: 'Wind vs. Flood Determination', type: 'page' },
        ]},
        { id: 'svc-tech', label: 'Advanced Tech', type: 'folder', children: [
           { id: 'underwater', label: 'Underwater Drone Inspections', type: 'page', meta: 'LINK TO UNDERWATERDRONES.NET' },
           { id: 'aerial', label: 'Aerial Drone Roof Inspections', type: 'page' }
        ]}
      ]
    },

    // 3. The Horseshoe (Locations)
    {
      id: 'locations',
      label: 'The Florida Horseshoe (Location Silos)',
      type: 'category',
      icon: <MapPin className="w-4 h-4" />,
      children: [
        // Southeast
        {
          id: 'region-se',
          label: 'Southeast (Miami/Broward/Palm Beach)',
          type: 'folder',
          children: [
            createCityHub("Miami", coastalSuite, ["High-Rise Recertification"]),
            createCityHub("Fort Lauderdale", coastalSuite, ["Concrete Spalling Repair"]),
            createCityHub("West Palm Beach", coastalSuite, ["Historic Structure Analysis"]),
            createCityHub("Boca Raton", coastalSuite, ["Luxury Condo Inspections"]),
            createCityHub("Hialeah", coastalSuite, ["Commercial Claims Support"])
          ]
        },
        // Central
        {
          id: 'region-central',
          label: 'Central (Orlando/I-4 Corridor)',
          type: 'folder',
          children: [
            createCityHub("Orlando", inlandSuite, ["Theme Park Structure Analysis"]),
            createCityHub("Kissimmee", inlandSuite, ["Resort & Hotel Engineering"]),
            createCityHub("Winter Park", inlandSuite, ["Residential Forensics"]),
            createCityHub("Lakeland", inlandSuite, ["Sinkhole Investigations"]),
            createCityHub("Altamonte Springs", inlandSuite)
          ]
        },
        // Tampa Bay (West)
        {
          id: 'region-west',
          label: 'Tampa Bay (West Coast)',
          type: 'folder',
          children: [
            createCityHub("Tampa", coastalSuite, ["Commercial Roof Consulting"]),
            createCityHub("St. Petersburg", coastalSuite, ["Old Northeast Foundation Repair"]),
            createCityHub("Clearwater", coastalSuite, ["Scientology/Institutional Property"]),
            createCityHub("New Port Richey", coastalSuite, ["Pasco Flood Engineering"]),
            createCityHub("Brandon", inlandSuite)
          ]
        },
        // Southwest
        {
          id: 'region-sw',
          label: 'Southwest (Naples/Ft Myers)',
          type: 'folder',
          children: [
            createCityHub("Sarasota", coastalSuite, ["Luxury Waterfront Forensics"]),
            createCityHub("Fort Myers", coastalSuite, ["Hurricane Ian Recovery"]),
            createCityHub("Naples", coastalSuite, ["High-Net-Worth Claims"]),
            createCityHub("Cape Coral", coastalSuite, ["Canal Wall Failure (Drone)"]),
            createCityHub("Marco Island", coastalSuite, ["Windstorm Analysis"])
          ]
        }
      ]
    },

    // 4. Content Strategy
    {
      id: 'resources',
      label: 'Resources & Articles (Topic Clusters)',
      type: 'category',
      icon: <FileText className="w-4 h-4" />,
      children: [
        { id: 'blog-legal', label: 'Legal & Compliance', type: 'folder', children: [
          { id: 'art-sb4d', label: 'Guide to SB 4-D for HOAs', type: 'article' },
          { id: 'art-558', label: 'Understanding Chapter 558 Claims', type: 'article' },
          { id: 'art-daubert', label: 'Daubert Standard in FL Courts', type: 'article' }
        ]},
        { id: 'blog-tech', label: 'Technology & Drones', type: 'folder', children: [
          { id: 'art-rov', label: 'Why ROVs are Safer than Divers', type: 'article' },
          { id: 'art-thermal', label: 'Thermal Imaging for Roof Moisture', type: 'article' }
        ]},
        { id: 'blog-disaster', label: 'Disaster Recovery', type: 'folder', children: [
          { id: 'art-ian', label: 'Post-Ian Structural Lessons', type: 'article' },
          { id: 'art-flood', label: 'FEMA Elevation Certificates Explained', type: 'article' }
        ]}
      ]
    }
  ]
};

// --- Components ---

const NodeIcon = ({ type }: { type: NodeType }) => {
  switch (type) {
    case 'root': return <Anchor className="w-5 h-5 text-blue-600" />;
    case 'category': return <Folder className="w-5 h-5 text-gray-700" />;
    case 'folder': return <Folder className="w-4 h-4 text-blue-400" />;
    case 'hub': return <MapPin className="w-4 h-4 text-red-500" />;
    case 'page': return <FileText className="w-4 h-4 text-gray-500" />;
    case 'article': return <FileText className="w-4 h-4 text-green-600" />;
    default: return <FileText className="w-4 h-4" />;
  }
};

const SitemapNodeItem = ({ node, level, defaultOpen = false }: { node: SitemapNode; level: number; defaultOpen?: boolean }) => {
  const [isOpen, setIsOpen] = useState(defaultOpen || level < 2);
  const hasChildren = node.children && node.children.length > 0;

  return (
    <div className="select-none">
      <div 
        className={`flex items-center py-1 px-2 hover:bg-blue-50 cursor-pointer rounded transition-colors ${level === 0 ? 'bg-blue-100 font-bold' : ''}`}
        style={{ paddingLeft: `${level * 20 + 8}px` }}
        onClick={() => setIsOpen(!isOpen)}
      >
        <div className="mr-2 w-4 flex justify-center">
          {hasChildren && (
            isOpen ? <ChevronDown className="w-4 h-4 text-gray-400" /> : <ChevronRight className="w-4 h-4 text-gray-400" />
          )}
        </div>
        <div className="mr-2">
          {node.icon || <NodeIcon type={node.type} />}
        </div>
        <div className="flex-1 flex items-center">
          <span className={`text-sm ${node.type === 'hub' ? 'font-semibold text-gray-800' : 'text-gray-700'}`}>
            {node.label}
          </span>
          {node.meta && (
            <span className="ml-2 text-xs bg-yellow-100 text-yellow-800 px-1.5 py-0.5 rounded border border-yellow-200">
              {node.meta}
            </span>
          )}
        </div>
      </div>
      
      {isOpen && hasChildren && (
        <div className="border-l border-gray-200 ml-5">
          {node.children!.map((child) => (
            <SitemapNodeItem key={child.id} node={child} level={level + 1} />
          ))}
        </div>
      )}
    </div>
  );
};

const StatsCard = ({ title, value, icon, color }: { title: string, value: number, icon: any, color: string }) => (
  <div className={`bg-white p-4 rounded-lg shadow border-l-4 ${color} flex items-center space-x-4`}>
    <div className={`p-2 rounded-full bg-gray-50`}>{icon}</div>
    <div>
      <p className="text-sm text-gray-500">{title}</p>
      <p className="text-2xl font-bold text-gray-800">{value}</p>
    </div>
  </div>
);

export default function SitemapVisualizer() {
  // Calculate Stats
  const stats = useMemo(() => {
    let totalPages = 0;
    let cityHubs = 0;
    let servicePages = 0;
    let articles = 0;

    const traverse = (node: SitemapNode) => {
      if (node.type === 'page') {
        totalPages++;
        servicePages++;
      }
      if (node.type === 'article') {
        totalPages++;
        articles++;
      }
      if (node.type === 'hub') {
        totalPages++; // The hub itself is a page
        cityHubs++;
      }
      
      if (node.children) {
        node.children.forEach(traverse);
      }
    };
    
    traverse(sitemapData);
    return { totalPages, cityHubs, servicePages, articles };
  }, []);

  return (
    <div className="min-h-screen bg-gray-50 p-8 font-sans">
      <div className="max-w-6xl mx-auto">
        <header className="mb-8">
          <h1 className="text-3xl font-bold text-gray-900 mb-2">The Florida Horseshoe Sitemap</h1>
          <p className="text-gray-600">Exhaustive Structure for meforensics.com • Miami to Naples</p>
        </header>

        {/* Dashboard */}
        <div className="grid grid-cols-1 md:grid-cols-4 gap-4 mb-8">
          <StatsCard 
            title="Total URL Count" 
            value={stats.totalPages} 
            icon={<Layers className="w-6 h-6 text-blue-600"/>} 
            color="border-blue-600" 
          />
          <StatsCard 
            title="City Hubs" 
            value={stats.cityHubs} 
            icon={<MapPin className="w-6 h-6 text-red-500"/>} 
            color="border-red-500" 
          />
          <StatsCard 
            title="Service Landing Pages" 
            value={stats.servicePages} 
            icon={<Zap className="w-6 h-6 text-yellow-500"/>} 
            color="border-yellow-500" 
          />
          <StatsCard 
            title="Articles & Resources" 
            value={stats.articles} 
            icon={<FileText className="w-6 h-6 text-green-600"/>} 
            color="border-green-600" 
          />
        </div>

        {/* Tree Visualizer */}
        <div className="bg-white rounded-xl shadow-lg border border-gray-200 overflow-hidden">
          <div className="bg-gray-100 px-6 py-4 border-b border-gray-200 flex justify-between items-center">
            <h2 className="font-semibold text-gray-700 flex items-center">
              <Anchor className="w-4 h-4 mr-2" /> 
              Sitemap Structure
            </h2>
            <span className="text-xs text-gray-500">Click folders to expand/collapse</span>
          </div>
          <div className="p-6 overflow-x-auto">
            <SitemapNodeItem node={sitemapData} level={0} defaultOpen={true} />
          </div>
        </div>
      </div>
    </div>
  );
}