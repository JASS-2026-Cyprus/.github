# Intelligence-Driven Smart Eco City
## Building Urban Digital Twins with Distributed AI Agents

## Overview

JASS 2026 challenges international student teams to build an Intelligence-Driven Smart
Eco City -- a comprehensive digital twin that integrates distributed AI agents for urban
environmental monitoring and infrastructure management. Over 8 intensive days, teams
will design, implement, and deploy autonomous monitoring systems that communicate
through a unified intelligent core.

The project continues JASS's evolution toward AI-augmented cyber-physical systems,
building on previous work with autonomous vehicles (2023), LLM-controlled smart cities
(2024), and hardware abstraction for robotics (2025). This year, we take the next step:
creating a distributed multi-agent system where each component reasons about
temporal data streams and collaborates through shared context.

## Core Concept: The Urban Digital Twin

The Intelligence-Driven Smart Eco City is a digital twin architecture consisting of two
interconnected layers:

### Central Intelligence Hub

A unified coordination center responsible for aggregating data from all monitoring
subsystems, generating city-wide state representations, forecasting trends using
Time-Series Language Models (TSLM), detecting anomalies and cross-domain
correlations, and orchestrating responses to critical events. The hub maintains a shared
context that enables different monitoring agents to understand each other's
observations and coordinate their actions.

### Distributed Monitoring Agents

Semi-autonomous edge systems that operate independently while contributing to the
collective intelligence. Each agent handles local data collection and preprocessing,
edge inference for real-time decision making, context formation using Model Context
Protocol (MCP), and bidirectional communication with the central hub.

## Monitoring Domains

The digital twin incorporates four primary monitoring domains, each addressing critical
aspects of urban environmental health:

### 1. Structural Health Monitoring (Post-Earthquake Assessment)

Drone-based visual inspection system for detecting and classifying structural
cracks in buildings. Particularly relevant to the Mediterranean seismic zone, this
system enables rapid post-earthquake damage assessment. The agent
processes visual data streams to identify crack patterns, estimate severity, and
prioritize inspection routes.

### 2. Air Quality Monitoring

Mobile and stationary sensor networks measuring particulate matter, gases, and
environmental conditions. Mobile units (Duckietown vehicles) patrol the city while
fixed stations provide continuous baseline measurements. The agent correlates
air quality with traffic patterns, weather conditions, and time-of-day factors.

### 3. Waste Management Monitoring

Aerial and ground-based detection of waste accumulation in urban areas. Drones
identify illegal dumping sites and overflow conditions, while ground sensors
monitor container fill levels. The agent optimizes collection routes and predicts
maintenance needs based on historical patterns.

### 4. Water Quality Monitoring

Sensor networks tracking water quality parameters across the urban water
system. Monitors turbidity, pH, dissolved oxygen, and contamination indicators.
The agent detects anomalies that may indicate pollution events or infrastructure
failures.

## Key Technologies

### Time-Series Language Models (TSLM)

Based on Stanford's OpenTSLM framework, we integrate time series as a native
modality into Large Language Models. This enables natural-language reasoning over
sensor data streams, automatic generation of human-readable descriptions of temporal
patterns, trend forecasting with explainable rationales, and anomaly detection with
contextual understanding. TSLM bridges the gap between continuous sensor signals
and discrete reasoning, allowing agents to "understand" what sensor readings mean
rather than just processing numbers.

### Model Context Protocol (MCP)

MCP provides the integration layer connecting all components. Each monitoring agent
exposes its capabilities as MCP tools, while the central hub aggregates contexts from
all agents. This architecture enables seamless tool interoperability across
heterogeneous systems, dynamic context sharing between agents, standardized
interfaces for LLM-agent communication, and an extensible plugin architecture for new
sensors and capabilities.

### LLM-Based Agents

Each subsystem operates as an intelligent agent capable of autonomous
decision-making within its domain, natural language interaction with operators,
collaborative reasoning with other agents, and learning from historical patterns. The
distributed agent architecture ensures resilience -- individual agents continue operating
even if central coordination is temporarily unavailable.

## Hardware Platform

- Duckietown Platform: Autonomous vehicles equipped with environmental sensors for mobile monitoring
- Drone Fleet: Aerial platforms for visual inspection and wide-area monitoring
- Sensor Networks: Air quality sensors (PM2.5, PM10, CO2, NO2), water quality probes, environmental monitors
- Edge Computing: Jetson/Orange Pi units for local inference and agent hosting
- OptiTrack System: Precision positioning for an indoor testing environment

## System Architecture

The software is organized as vertical slices rather than horizontal architectural layers.
Each slice represents an independent use case that spans the full stack – from sensor
data acquisition through agent intelligence to central hub integration. This vertical
structure enables continuous integration and daily releases, allowing each team to
demonstrate working end-to-end functionality in evening demos throughout the 8-day
program. Teams work in groups of approximately 3–6 members, each owning one
complete use case.

The system follows the Broker Pattern, with the Central Intelligence Hub (JASS Orb)
acting as a broker mediating between all use case slices via MCP. Combined with the
Blackboard Pattern, the hub provides a shared workspace where each slice contributes
its domain-specific observations, enabling cross-domain correlation and collaborative
diagnostics.

The four top level uses case are:

### 1. Air Quality Monitoring – Rush Hour Use Case

Mobile Duckiebots equipped with air quality sensors patrol the city during rush
hour periods. The TSLM pipeline detects temporal patterns in particulate matter
and gas concentrations, correlating them with traffic density and time-of-day
factors. The agent identifies anomalous pollution spikes, forecasts air quality
degradation, and generates alerts for city operators. Deliverable: end-to-end air
quality monitoring from mobile sensor data through TSLM analysis to operator
dashboard with rush hour predictions.

### 2. Earthquake Monitoring – Post-Earthquake Unusual Pattern Identification

Structural health monitoring focused on post-earthquake assessment in the
Mediterranean seismic zone. The TSLM pipeline analyzes seismic sensor time
series to identify unusual vibration patterns and aftershock sequences. The agent
correlates structural sensor readings with external earthquake data to detect
anomalies that may indicate building damage. Deliverable: end-to-end
earthquake response system from seismic sensors through TSLM-based pattern
detection to damage assessment reports.

### 3. Water Quality Monitoring – Swimming Pool Use Case

Water quality sensors continuously monitor swimming pool parameters including
pH, turbidity, dissolved oxygen, and contamination indicators. The TSLM pipeline
processes these time-series streams to detect quality degradation trends and
anomalous chemical patterns. The agent provides early warnings before water
quality falls below safe thresholds. Deliverable: end-to-end water quality system
from sensor probes through TSLM temporal analysis to automated quality alerts
and maintenance recommendations.

### 4. Waste Management – Visual Drone Inspection Use Case

Drone-based aerial inspection using Vision Language Models (VLM) for visual
waste detection and classification. Drones capture imagery of urban areas to
identify illegal dumping sites, overflowing containers, and waste accumulation
patterns. The VLM agent interprets visual data to classify waste types, estimate
volumes, and prioritize cleanup routes. Deliverable: end-to-end visual waste
monitoring from drone imagery through VLM-based classification to optimized
collection route recommendations.

This architecture ensures each team delivers independently deployable functionality.
Daily evening demos validate end-to-end integration, and the MCP-based Broker
architecture ensures slices can evolve independently without breaking the overall
system.

## Learning Outcomes

Participants will gain hands-on experience with:

- Designing and implementing distributed multi-agent systems
- Integrating LLMs with real-time sensor data streams
- Building digital twins for cyber-physical systems
- Working with time-series reasoning and TSLM architectures
- Implementing MCP-based tool integration
- Edge computing and embedded AI deployment
- Drone and autonomous vehicle programming
- Agile development in international teams
