// src/App.js
import React from "react";
import "./App.css";

function App() {
  return (
    <div className="app-container">
      {/* Chat Section */}
      <div className="chat-section">
        <header className="chat-header">
          <h2>🤖 I am Prudence - Your DSP chatbot!</h2>
          <span className="status">🟢 Assistant On</span>
        </header>

        {/* Chat Bubbles */}
        <div className="chat-messages">
          {/* Assistant Message */}
          <div className="message assistant">
            <div className="message-content">
              <p>Welcome to the chatbot! How can I assist you today?</p>
            </div>
            <span className="timestamp">09:32 AM</span>
          </div>

          {/* User Message */}
          <div className="message user">
            <div className="message-content">
              <p>What is DSP?</p>
            </div>
            <span className="timestamp">09:35 AM</span>
            <div className="user-initials">AR</div>
          </div>

          {/* Another Assistant Message */}
          <div className="message assistant">
            <div className="message-content">
              <p>DSP is a Data Science Platform that enables advanced analytics.</p>
            </div>
            <span className="timestamp">09:36 AM</span>
          </div>
        </div>
      </div>

      {/* Sidebar Section */}
      <div className="sidebar">
        <div className="sidebar-header">
          <h3>Get assistance from me!</h3>
          <p>I found some helpful resources for you...</p>
        </div>

        {/* Suggested Resources */}
        <div className="resources">
          <div className="resource-item">
            <h4>Data Science Platform</h4>
            <p>Short description about DSP here...</p>
          </div>
          <div className="resource-item">
            <h4>Find Your Data Science Platform</h4>
            <p>Another short description...</p>
          </div>
          <div className="resource-item">
            <h4>Additional DSP Resources</h4>
            <p>Further details on DSP...</p>
          </div>
        </div>

        {/* Related Questions */}
        <div className="related-questions">
          <h4>Related questions</h4>
          <ul>
            <li>What are the capabilities of DSP?</li>
            <li>How can I use DSP?</li>
          </ul>
        </div>
      </div>
    </div>
  );
}

export default App;



csss
/* src/App.css */
.app-container {
  display: flex;
  height: 100vh;
  font-family: Arial, sans-serif;
}

.chat-section {
  width: 65%;
  padding: 20px;
  border-right: 1px solid #ddd;
  display: flex;
  flex-direction: column;
}

.chat-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 10px;
  border-bottom: 1px solid #ddd;
}

.chat-header h2 {
  font-size: 18px;
  margin: 0;
}

.status {
  font-size: 14px;
  color: green;
}

.chat-messages {
  flex: 1;
  padding: 10px 0;
  overflow-y: auto;
}

.message {
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
  max-width: 80%;
}

.message.assistant {
  align-self: flex-start;
}

.message.user {
  align-self: flex-end;
  text-align: right;
  position: relative;
}

.message-content {
  background-color: #f1f1f1;
  padding: 10px;
  border-radius: 10px;
  display: inline-block;
}

.message.user .message-content {
  background-color: #d1eaff;
}

.timestamp {
  font-size: 12px;
  color: #999;
  margin-top: 5px;
}

.user-initials {
  position: absolute;
  bottom: 5px;
  right: -30px;
  background-color: #007bff;
  color: white;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  font-weight: bold;
}

.sidebar {
  width: 35%;
  padding: 20px;
  background-color: #f9f9f9;
}

.sidebar-header h3 {
  font-size: 18px;
  margin: 0 0 10px 0;
}

.resources {
  margin-top: 20px;
}

.resource-item {
  padding: 10px;
  border-bottom: 1px solid #ddd;
  margin-bottom: 10px;
}

.resource-item h4 {
  font-size: 16px;
  margin: 0;
}

.related-questions {
  margin-top: 20px;
}

.related-questions h4 {
  font-size: 16px;
  margin-bottom: 10px;
}

.related-questions ul {
  list-style: none;
  padding: 0;
}

.related-questions li {
  margin-bottom: 5px;
}
