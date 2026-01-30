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
