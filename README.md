## Chat Application in Python and Rust

### 1. Problem Statement:

*Original Statement:*
We aim to develop a chat application that allows users to connect, send messages, and receive messages in real-time. The primary goal is to create a cross-language comparison between Python and Rust implementations.

*POPL Angle:*
The Principles of Programming Language (POPL) aspect in this problem lies in the design and implementation of concurrent communication between clients and the server. While the problem of creating chat applications is not new, our approach involves comparing the trade-offs and language-specific nuances in Python and Rust.

### 2. Software Architecture:

*Architecture Overview:*
Our solution follows a client-server architecture. The server, implemented in both Python and Rust, listens for incoming connections and manages communication between clients. Clients, written in Python and Rust, connect to the server to send and receive messages.

*Components:*
- *Server:* Handles incoming connections, manages clients, and broadcasts messages.
- *Client:* Connects to the server, sends user messages, and receives broadcasted messages.

*Testing Component:*
Testing is currently conducted locally during development. However, future iterations may include remote testing environments.

*Database:*
No database is involved in the current implementation.

### 3. POPL Aspects:

1. *Concurrency Handling:*
   - *Python:* Threading is used for concurrent communication.
   - *Rust:* Utilizes multi-threading and non-blocking I/O for concurrency.

2. *Error Handling:*
   - *Python:* Exception handling is used for error management.
   - *Rust:* Utilizes Result and Option types for effective error handling.

3. *Memory Management:*
   - *Python:* Memory is managed automatically (garbage collection).
   - *Rust:* Employs ownership and borrowing to ensure memory safety.

4. *Type Systems:*
   - *Python:* Dynamically typed language.
   - *Rust:* Statically typed language with a strong emphasis on memory safety.

5. *Message Serialization:*
   - *Python:* Messages are encoded and decoded using ASCII.
   - *Rust:* Messages are sent as byte streams with dynamic resizing.

### 4. Results and Testing:

*Tests Conducted:*
- Unit tests for individual components (client and server).
- Functional tests for overall system behavior.

*Dataset Used:*
- Test messages with varying lengths and special characters.

*Benchmarks:*
- Latency and throughput benchmarks for message transmission.

*Graphs:*
- Insert relevant graphs showing latency and throughput performance.

*Validation:*
- Systematic testing ensures that the implemented solution aligns with the initial problem statement.
- Comparison of Python and Rust implementations in terms of performance and resource utilization.

### 5. Potential for Future Work:

*Additional Features:*
- Implement encryption for secure communication.
- Explore the use of external libraries for enhanced functionality.

*POPL Aspects for Future Consideration:*
- Explore formal verification methods for ensuring correctness.
- Investigate the impact of language-specific features on scalability.

*Conclusion:*
The current implementation provides a functional chat application in both Python and Rust, offering insights into the language-specific considerations in terms of concurrency, error handling, and memory management. Future work could focus on expanding features and further optimizing performance.


Steps for running both the applications.

For the Python Applications
Python is an interpreted language, so you don't need to compile the applications. Just run them directly. Make sure you have Python installed on your system.

Open two terminal windows - one for the server and one for the client.

Run the Server:
Navigate to the directory containing server.py.
Execute the command: python server.py (or python3 server.py depending on your Python installation).

Run the Client:
In the other terminal, navigate to the directory containing client.py.
Execute the command: python client.py (or python3 client.py).


For the Rust Applications
Rust applications need to be compiled before they can be executed. Make sure you have Rust installed on your system, including Cargo, Rust's package manager and build system.

Create a new Rust project for each application (if not already done):
Use cargo new server and cargo new client to create new projects.
Replace the contents of the main.rs files in each project with the code from your server.rs and client.rs files, respectively.
Place any additional required files in the correct locations within each project structure.

Compile and Run the Server:
Navigate to the server project directory (where the Cargo.toml file is).
Compile and run the server using cargo run.

Compile and Run the Client:
Open a new terminal window.
Navigate to the client project directory.
Compile and run the client using cargo run.

Networking Considerations
Make sure the server is running before starting the client.
The Python and Rust applications might be using different ports (Python: 55555, Rust: 6000). Ensure they don't conflict with each other or with any other applications on your system.
If you are running both the Python and Rust applications simultaneously, they should be configured to use different ports to avoid conflicts.

