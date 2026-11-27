# Beacon by Zelkc — MCP Server

Send push notifications to your phone, car dashboard, and browser from any AI assistant.

## Setup

1. Create a free account at [beacon.zelkc.com](https://beacon.zelkc.com)
2. 2. Go to **Connect > Developer Tools** and create a Sender Key
   3. 3. Add the MCP server to your AI client:
     
      4. ### Claude Desktop / Claude Code
     
      5. Add to your MCP config:
     
      6. ```json
         {
           "mcpServers": {
             "beacon": {
               "url": "https://api.beacon.zelkc.com/mcp",
               "headers": {
                 "X-Sender-Key": "YOUR_SENDER_KEY"
               }
             }
           }
         }
         ```

         ### Any MCP-compatible client

         - **Server URL:** `https://api.beacon.zelkc.com/mcp`
         - - **Auth:** Header `X-Sender-Key: YOUR_SENDER_KEY`
           - - **Protocol:** Streamable HTTP (JSON-RPC over HTTP with optional SSE)
            
             - ## Available Tools
            
             - ### `send_notification`
            
             - Send a push notification to all your registered devices.
            
             - | Parameter  | Type   | Required | Description                        |
             - |-----------|--------|----------|------------------------------------||
             - | title     | string | Yes      | Notification title (max 250 chars) |
             - | body      | string | Yes      | Notification body (max 1024 chars) |
             - | priority  | string | No       | quiet, low, normal, high, urgent   |
             - | channel   | string | No       | Channel name to file under         |
             - | url       | string | No       | URL to open when tapped            |
            
             - ## Also Available
            
             - - **OpenAPI spec:** `https://api.beacon.zelkc.com/openapi.json` (for ChatGPT Actions, Gemini, Copilot)
               - - **Quick-send URL:** `https://api.beacon.zelkc.com/v1/quick-send/YOUR_KEY?title=Hello&body=World` (for Shortcuts, Home Assistant, webhooks)
                 - - **Pushover-compatible API:** Drop-in replacement for Pushover
                  
                   - ## Pricing
                  
                   - - **Free:** 100 messages/month, 2 devices
                     - - **Plus ($14.99/year):** 10,000 messages/month, unlimited devices
                       - - **Developer ($19.99/year):** 20,000 messages/month, unlimited devices, overage at $0.001/msg
                        
                         - ## Links
                        
                         - - Website: [beacon.zelkc.com](https://beacon.zelkc.com)
                           - - Privacy: [api.beacon.zelkc.com/privacy](https://api.beacon.zelkc.com/privacy)
