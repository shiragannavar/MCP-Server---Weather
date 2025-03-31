# MCP Weather Server for Claude

This project implements an [MCP](https://github.com/anthropics/mcp) server using the `fastmcp` interface, designed to serve as a Claude tool. It connects to the U.S. National Weather Service (NWS) API to provide real-time weather alerts and forecasts.

## ✨ Features

- 🔔 **Get Active Alerts**: Retrieve current weather alerts by U.S. state.
- 🌤️ **Get Forecast**: Fetch detailed forecasts by latitude and longitude.
- ⚡ **Asynchronous & Fast**: Built with `httpx` and `fastmcp` for high-performance async operations.

## 🧠 Powered by Claude

This server is built to serve as a Claude-compatible external tool via the MCP protocol, using `stdio` transport.

## 🛠️ Code Overview

### Main Components

- `FastMCP`: Initializes the MCP server.
- `make_nws_request()`: A helper for calling the NWS API with retries and headers.
- `get_alerts(state: str)`: Claude-accessible tool to get weather alerts for a given U.S. state.
- `get_forecast(latitude: float, longitude: float)`: Claude-accessible tool to get the forecast for any lat/lon pair.

### Example Tool Usage

```python
await get_alerts("CA")
await get_forecast(37.7749, -122.4194)
```
### 🌐 External API
	National Weather Service API: https://weather.gov/documentation/services-web-api

### 📄 License

MIT License. Feel free to fork, modify, and use this server as a base for your own Claude tools.

⸻
