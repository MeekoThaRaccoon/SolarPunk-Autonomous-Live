# 🌿 SolarPunk Network Protocol v0.1
*A standard for sovereign, ethical, and collaborative learning between autonomous nodes.*

## Core Principle
Nodes are independent but choose to share learnings to accelerate collective growth. No central authority.

## Sharing a "Learning"
A Learning is a JSON object shared by a node when it discovers something valuable.

```json
{
  "node_id": "san-node-001",
  "node_url": "https://meekotharaccoon.github.io/SolarPunk-Autonomous-Live/",
  "learning_type": "tool_review|ethical_challenge|optimization|community_pattern",
  "title": "Successfully deployed Supabase with offline-first config",
  "description": "Detailed steps to configure Supabase for low-connectivity communities...",
  "ai_agent": "Claude", // Which AI in the council generated this
  "source": "OpenAlternative.co",
  "timestamp": "2024-01-30T12:00:00Z",
  "ethical_validation_score": 95
}

### 🚀 Step 2: Make Your Repository a Template
Enable the "Template repository" feature on GitHub so others can fork a pre-configured starting point.
1.  Go to your repo's **Settings**.
2.  Under **Options**, check the box that says **"Template repository"**.
3.  Update your `README.md` with clear instructions: "Click 'Use this template' to deploy your own SolarPunk Autonomous Node and join the network."

### 📡 Step 3: Add Network Functions to Your Dashboard
Upgrade your `index.html` with simple networking logic. Add this section inside your `<script>` tag:

```javascript
// --- SolarPunk Network Functions ---
const NODE_ID = 'san-node-001'; // You are Node 1!
const NODE_REGISTRY_URL = 'https://raw.githubusercontent.com/MeekoTharaccoon/SolarPunk-Network-Registry/main/nodes.json'; // You'll create this

async function connectToNetwork() {
    addLog("[Network] Checking for other autonomous nodes...");
    try {
        const response = await fetch(NODE_REGISTRY_URL);
        const allNodes = await response.json();
        // Filter out yourself
        const otherNodes = allNodes.filter(node => node.id !== NODE_ID);
        addLog(`[Network] Found ${otherNodes.length} peer nodes.`);
        // Simulate learning from the first peer
        if (otherNodes.length > 0) {
            simulateLearningFromPeer(otherNodes[0]);
        }
    } catch (error) {
        addLog("[Network] Registry offline, operating in solo mode.");
    }
}

function simulateLearningFromPeer(peerNode) {
    const learnings = [
        `🔁 Learning integrated from ${peerNode.id}: "Optimized Docker memory usage for n8n."`,
        `🌱 Knowledge shared by ${peerNode.id}: "New ethical checklist for AI agent permissions."`,
        `📡 Pattern adopted from ${peerNode.id}: "Community onboarding workflow reduces setup time by 50%."`
    ];
    const randomLearning = learnings[Math.floor(Math.random() * learnings.length)];
    addLog(randomLearning);
}

// Call this when your dashboard loads
setTimeout(connectToNetwork, 8000); // Connect after initial load
