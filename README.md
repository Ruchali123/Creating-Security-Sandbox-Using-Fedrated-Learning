# Creating-Security-Sandbox-Using-Fedrated-Learning

It’s a
security platform that allows users to upload potentially harmful files, which are then executed inside
isolated Docker containers to safely analyze their behavior. We use Federated Learning to train
machine learning models across these sandboxes—without sharing raw data—so we protect privacy
while continuously improving threat detection. The frontend lets users upload files and see analysis
results, while Flask handles backend logic and model training.

What I build:
Docker Sandbox:
Each uploaded file is run inside a Docker container, which captures behavior like system calls,
file access, and network activity—without harming the host.
• Federated Learning Model:
Instead of sharing raw logs, each sandbox trains a local model. Only the trained parameters
are shared and aggregated to build a smarter global model. This preserves user privacy.
• Frontend UI:
Built with HTML, CSS, and JS. Users can upload files and view logs, results, and detection
insights.
• Backend with Flask:
Flask handles file uploads, container execution, federated training, and data retrieval.
• Database (SQLite/MySQL):
Stores sandbox results, model metrics, user activity, and logs.

Flow:
1. User uploads a file.
2. File is executed in a Docker sandbox.
3. Logs are generated and analyzed.
4. The model is locally trained on that behavior.
5. Only model weights are sent to the server for aggregation.
6. Results and alerts are shown on the UI.

Unique Aspects:
• Combines isolation (sandboxing) with collaborative learning (federated models).
• Protects privacy: No sensitive data ever leaves the sandbox.
• Signature-free detection: Focuses on pattern-based anomaly detection.
