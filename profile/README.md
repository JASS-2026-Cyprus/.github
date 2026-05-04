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

Stationary sensor networks measuring temperature, humidity, and turbidity, 
supplemented by open-source media and satellite data streams. 
The agent correlates air quality with traffic patterns, weather conditions, 
and time-of-day factors.

### 3. Maintenance Monitoring

Aerial and ground-based detection of waste accumulation in urban areas. Drones
identify illegal dumping sites and overflow conditions, while ground sensors
monitor container fill levels. The agent optimizes collection routes and predicts
maintenance needs based on historical patterns.

### 4. Water Quality Monitoring

Sensor networks tracking water quality parameters and monitoring the broader 
urban water infrastructure. Monitors turbidity, pH, dissolved oxygen, and 
contamination indicators. The agent detects anomalies that may indicate pollution 
events or infrastructure failures.

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

- Drone Fleet: Aerial platforms for visual inspection and wide-area monitoring
- Sensor Networks: Air quality sensors (temperature, humidity, turbidity), water quality probes, environmental monitors
- Edge Computing: Jetson/Orange Pi units for local inference and agent hosting
- OptiTrack System: Precision positioning for an indoor testing environment

## System Architecture

The system follows an Agentic Swarm architecture, where each agent exposes a defined 
set of MCP tools that are registered with the shared swarm. Although individual 
agent repositories may include a local hub and blackboard implementation for development 
purposes, at runtime all agents participate in a unified swarm that acts as a collective blackboard. 
Agents communicate directly with one another, cross-validating hypotheses across domains 
to enable collaborative diagnostics. A Cockpit Dashboard aggregates and displays the results 
and measurements from all individual agents in a single operator-facing view.

The four top level uses case are:

### 1. Air Quality Monitoring – Multi-Event Use Case
Stationary sensors and satellite and open-source media data streams feed the 
TSLM pipeline, which detects temporal patterns in temperature, humidity, and turbidity.
The agent correlates air quality degradation with impacting events such as earthquakes, 
rush hour traffic, or other urban incidents, identifies anomalous pollution spikes, and 
generates actionable recommendations for city operators and citizens on how to respond. 
Deliverable: end-to-end air quality monitoring from stationary sensor, news and satellite data through 
TSLM analysis to operator dashboard with event-driven alerts and citizen guidance.

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

### 4. Maintenance Management – Visual Drone Inspection Use Case

Drone-based aerial inspection using Vision Language Models (VLM) for visual
waste detection and classification. Drones capture imagery of urban areas to
identify illegal dumping sites, overflowing containers, and waste accumulation
patterns. The VLM agent interprets visual data to classify waste types, estimate
volumes, and prioritize cleanup routes. Deliverable: end-to-end visual waste
monitoring from drone imagery through VLM-based classification to optimized
collection route recommendations.

This architecture ensures each team delivers independently deployable functionality.
Daily evening demos validate end-to-end integration, and the MCP-based
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
