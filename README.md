
# Anonymous Feedback Smart Contract

## Project Mission
The mission of this project is to provide a simple and efficient way to send and retrieve anonymous feedback using a smart contract built on the Soroban SDK. The contract ensures that feedback is stored securely and can be fetched using unique feedback IDs.

## Project Structure

### Contract Files
- **src/lib.rs**: This file contains the core logic of the smart contract, including the definitions for sending and fetching feedback.

### Code Explanation
- **Constants**:
  - `COUNT_FB`: A constant symbol used to track the number of feedback entries.
  
- **Enums**:
  - `FBbook`: An enumeration that defines the feedback type.

- **Structs**:
  - `Feedback`: A struct that represents a feedback entry with an ID and message.

- **Contract**:
  - `AnonymousFeedback`: The main contract struct.

- **Implementations**:
  - `impl AnonymousFeedback`: Implementation block containing the contract methods.
    - `send_feedback`: Method to send feedback. Increments the feedback count, creates a feedback entry, and stores it.
    - `fetch_feedback`: Method to fetch feedback by ID. Retrieves the feedback entry from storage.

## How to Use
1. **Send Feedback**:
   - Call the `send_feedback` method with the feedback message as a parameter. This method returns a unique feedback ID.
   
2. **Fetch Feedback**:
   - Call the `fetch_feedback` method with the feedback ID to retrieve the stored feedback message.

## Requirements
- **Rust**: Ensure you have Rust installed.
- **Soroban SDK**: Install the Soroban SDK to build and deploy the contract.

## Build and Deploy
1. **Build**:
   - Use the following command to build the contract:
     ```
     cargo build --target wasm32-unknown-unknown --release
     ```

2. **Deploy**:
   - Follow the Soroban SDK documentation for deploying the contract to your blockchain environment.

## Contributing
Feel free to contribute to this project by submitting issues or pull requests. We welcome improvements and new features.

## License
This project is licensed under the MIT License.
