PROJECT OVERVIEW: (microservices-based public transportation platform
The Public Bus Live Tracking & Crowding Estimator is designed to improve public transportation by providing commuters with accurate and up-to-date information about buses.
The system collects bus GPS telemetry, processes route and stop information, estimates arrival times, and determines the approximate crowding level of buses.
The project follows a Microservices Architecture, where major system functions are implemented as independent services.
                    
                    +----------------------+
                    | Passenger Web/Mobile |
                    |        App           |
                    +----------+-----------+
                               |
              +----------------+----------------+
              |                |                |
              v                v                v
       +-------------+  +-------------+  +-------------+
       | GPS Tracking|  | ETA         |  | Crowding    |
       | Service     |  | Calculation |  | Estimator   |
       +------+------+  | Service     |  | Service     |
              |         +------+------+  +------+------+
              |                |                |
              +----------------+----------------+
                               |
                    +----------v-----------+
                    | Route & Fleet        |
                    | Management Service   |
                    +----------+-----------+
                               |
                    +----------v-----------+
                    |   Transit Database   |
                    +----------------------+
