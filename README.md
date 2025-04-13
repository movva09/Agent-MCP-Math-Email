# MCP Math Gmail Client

The Math Gmail Client (`talk2mcp_math_gmail_client.py`) is a Python application that integrates mathematical computations with Gmail functionality. It uses the Gemini AI model to process mathematical queries and can send results via email.

## Features
- Integration with Gemini AI for mathematical problem-solving
- Gmail integration for sending mathematical results
- Iterative problem-solving approach
- Support for various mathematical operations
- Automated email generation with mathematical results
- Secure Gmail authentication
- Multiple recipient support
- Customizable email templates
- Attachment support for complex results
- Scheduled email sending
- Email tracking and delivery confirmation
- Rich text formatting for mathematical expressions
- Batch processing capabilities

## Server Requirements
1. MCP Server Setup:
   - Python 3.x environment
   - MCP server package installed
   - Required server dependencies:
     - `mcp` package
     - `numpy` for mathematical operations
     - `pandas` for data processing
     - `matplotlib` for graph generation
     - `smtplib` for email handling

2. Server Configuration:
   - Port configuration (default: 8080)
   - Memory allocation for mathematical operations
   - Email queue management
   - Maximum concurrent connections
   - Timeout settings for operations
   - Email rate limiting

3. Server Tools:
   - Mathematical computation engine
   - Email queue manager
   - Attachment processor
   - Template renderer
   - Session manager
   - Error handling system

## Prerequisites
- Python 3.x
- Required Python packages:
  - `python-dotenv`
  - `google-generativeai`
  - `mcp` package
  - `google-auth`
  - `google-auth-oauthlib`
  - `google-auth-httplib2`
  - `google-api-python-client`

## Environment Setup
1. Create a `.env` file in the project root
2. Add your API keys:
   ```
   GEMINI_API_KEY=your_api_key_here
   GMAIL_CLIENT_ID=your_client_id_here
   GMAIL_CLIENT_SECRET=your_client_secret_here
   ```

## Server Setup
1. Install server dependencies:
   ```bash
   pip install mcp numpy pandas matplotlib
   ```

2. Configure server settings in `config.json`:
   ```json
   {
     "server": {
       "port": 8080,
       "max_connections": 10,
       "timeout": 30,
       "email": {
         "rate_limit": 100,
         "queue_size": 1000,
         "retry_attempts": 3
       }
     }
   }
   ```

3. Start the MCP server:
   ```bash
   python example2-3_server.py
   ```

## Available Tools

### Currently Implemented Tools

1. Mathematical Operations:
   - Basic arithmetic operations (add, subtract, multiply, divide)
   - Advanced mathematical functions (exponential, logarithmic)
   - ASCII value calculations
   - String manipulation and conversion
   - Array operations
   - Prime number calculations
   - Factorial computations
   - Fibonacci sequence generation

2. Email Tools:
   - Single recipient email sending
   - Basic email formatting
   - Simple attachment handling
   - Basic error handling
   - Gmail authentication
   - Email queue management
   - Basic delivery status tracking

### Planned Future Additions

1. Enhanced Mathematical Operations:
   - Matrix operations
   - Statistical calculations
   - Graph plotting and analysis
   - Equation solving
   - Complex number operations
   - Calculus functions
   - Data visualization tools

2. Advanced Email Features:
   - Multiple recipient support
   - HTML and rich text formatting
   - Advanced attachment handling
   - Email scheduling
   - Template management
   - Priority setting
   - Reply-to configuration
   - Email analytics
   - Bulk processing
   - Custom signatures
   - Email filtering
   - Auto-responders

3. Integration Features:
   - Google Calendar integration
   - Google Drive attachment handling
   - Google Sheets data export
   - Custom API integrations
   - Webhook support
   - Third-party service connections

## Installation
1. Clone the repository
2. Install required packages:
   ```bash
   pip install python-dotenv google-generativeai mcp google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client
   ```
3. Set up your environment variables as described above
4. Set up Gmail API credentials:
   - Go to Google Cloud Console
   - Create a new project
   - Enable Gmail API
   - Create OAuth 2.0 credentials
   - Download the credentials file

## Usage
1. Start the MCP server (see Server Setup section)
2. Ensure the server is running and accessible
3. Run the client:
   ```bash
   python talk2mcp_math_gmail_client.py
   ```

## Server-Client Communication
1. Connection Protocol:
   - Client establishes connection with server
   - Authentication handshake
   - Tool list synchronization
   - Session initialization
   - Email service verification

2. Data Flow:
   - Client sends mathematical queries
   - Server processes requests
   - Results are formatted for email
   - Email queue is managed
   - Delivery status is tracked
   - Notifications are sent

3. Error Handling:
   - Connection retry mechanism
   - Session recovery
   - Email queue recovery
   - Rate limit handling
   - Resource cleanup

## Example Queries
1. Basic Mathematical Email:
```
Calculate the factorial of 10 and send the result to user@example.com with the subject "Factorial Calculation Result".
```

2. Complex Mathematical Analysis:
```
Find the first 50 Fibonacci numbers, calculate their sum, and send the detailed analysis to team@example.com with a graph attachment.
```

3. Multiple Operations with Formatting:
```
Calculate the roots of the quadratic equation x² + 5x + 6 = 0, format the solution in LaTeX, and send it to professor@example.com with proper mathematical notation.
```

4. Scheduled Mathematical Report:
```
Generate a report of prime numbers between 1 and 1000, create a histogram of their distribution, and schedule it to be sent to research@example.com tomorrow at 9:00 AM.
```

## How It Works
1. The client connects to the MCP server
2. It processes mathematical queries using the Gemini AI model
3. Results are formatted for email
4. The system uses an iterative approach to solve complex problems
5. Results are sent via Gmail to specified recipients

## Error Handling
The client includes robust error handling for:
- API timeouts
- Invalid inputs
- Connection issues
- Tool execution errors
- Gmail authentication and sending errors

## Security
- Uses OAuth 2.0 for Gmail authentication
- Secure storage of API keys and credentials
- Encrypted communication with Gmail API

## Contributing
Feel free to submit issues and enhancement requests.

## License
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Additional Features
- Email template customization
- Automated report generation
- Integration with other Google services
- Email analytics and tracking
- Custom email signatures
- Bulk email processing
- Email filtering and organization
- Attachment compression
- Email encryption options
- Custom notification settings

## Advanced Server Configuration
4. Performance Optimization:
   - Email queue optimization
   - Attachment processing optimization
   - Memory management for large datasets
   - Connection pooling
   - Rate limiting configuration

5. Security Features:
   - End-to-end encryption
   - Two-factor authentication
   - IP whitelisting
   - Activity monitoring
   - Data retention policies

## Advanced Usage
4. Command Line Options:
   ```bash
   python talk2mcp_math_gmail_client.py --port 8080 --debug --log-level INFO --batch-size 100
   ```

5. Environment Variables:
   ```
   MCP_SERVER_HOST=localhost
   MCP_SERVER_PORT=8080
   DEBUG_MODE=true
   LOG_LEVEL=INFO
   BATCH_SIZE=100
   EMAIL_RATE_LIMIT=100
   ```

## Troubleshooting
1. Common Issues:
   - Email delivery failures
   - Attachment size limits
   - Authentication problems
   - Rate limiting issues
   - Connection timeouts

2. Solutions:
   - Check email server status
   - Verify API quotas
   - Review error logs
   - Check network connectivity
   - Validate credentials

## Performance Tips
1. Optimization:
   - Batch processing for large emails
   - Attachment compression
   - Connection pooling
   - Cache management
   - Resource monitoring

2. Best Practices:
   - Regular backup of email templates
   - Monitor API usage
   - Implement retry mechanisms
   - Use efficient data structures
   - Regular system maintenance
