# Quantum-Classical Hybrid Middleware for InMoov Robot

This repository contains middleware that enables quantum computing capabilities for the InMoov robot through integration with a custom QPU chip. The middleware provides both simulation and hardware interfaces for quantum operations.

## Overview

The middleware consists of two main components:
- A simulation interface for testing and development
- A hardware interface for direct QPU chip integration

## Features

- Quantum pattern recognition for enhanced visual processing
- Quantum optimization for robot movement planning
- Error mitigation and hardware calibration
- Robust error handling and logging
- MyRobotLab integration

## Prerequisites

- Python 3.8 or higher
- MyRobotLab installed and configured
- InMoov robot hardware setup
- Custom QPU chip installed (for hardware version)

## Installation

1. Install required dependencies:
```bash
pip install -r requirements.txt
```

2. Ensure MyRobotLab is properly configured with your InMoov robot
3. Verify QPU chip installation and connections (for hardware version)

## Usage

### Simulation Version
```python
from middleware_simulation import optimize_movement

# Run movement optimization simulation
optimize_movement()
```

### Hardware Version
```python
from middleware_hardware import QPUHardwareInterface, QuantumPatternRecognition, QuantumMovementOptimizer

# Initialize QPU interface
qpu = QPUHardwareInterface()

# Initialize quantum modules
pattern_recognition = QuantumPatternRecognition(qpu)
movement_optimizer = QuantumMovementOptimizer(qpu)

# Process vision data
vision_data = [0.5, 0.3, 0.8, 0.1]
pattern_result = pattern_recognition.process_vision_data(vision_data)

# Optimize movement
movement_params = {'angle': 3.14/4, 'speed': 0.5}
movement_result = movement_optimizer.optimize_movement(movement_params)
```

## Architecture

The middleware is structured in layers:
1. Hardware Interface Layer (QPUHardwareInterface)
2. Quantum Processing Layer (QuantumPatternRecognition, QuantumMovementOptimizer)
3. Integration Layer (MyRobotLab interface)

## Error Handling

The middleware includes comprehensive error handling:
- Hardware status monitoring
- Automatic calibration attempts
- Logging of all operations
- Graceful failure recovery

## Contributing

Contributions are welcome! Please ensure your code follows the existing structure and includes appropriate tests and documentation.

## License

This project is open source and available under the MIT License.
