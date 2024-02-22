# SpurContextAPI Integration for Cortex XSOAR

This integration allows Cortex XSOAR users to enrich indicators, specifically IP addresses, using the Spur Context API. It provides detailed context around the reputation, behavior, and characteristics of IP addresses, helping security analysts to quickly assess threats and make informed decisions.

## Configuration

Before you start, make sure you have received your API Token from Spur. This token is required to authenticate and interact with the Spur Context API.

### Standard Integration Setup

1. Navigate to **Settings** > **Integrations** > **Instances**.
2. Search for `SpurContextAPI` in the marketplace.
3. Click **Add instance** to create and configure a new integration instance.
   - **Name**: A meaningful name for the integration instance.
   - **API Token**: Your Spur Context API Token.
4. Click **Test** to validate the URLs, token, and connection.

### Adding SpurContextAPI as a BYOI (Bring Your Own Integration)

If the SpurContextAPI integration is not available in the marketplace, you can add it as a custom integration:

1. Navigate to **Settings** > **Integrations** > **Instance**.
2. At the top right, click on the cloud icon (Upload Integration).
3. Upload the integration code by selecting the SpurContextAPI.yml in the file upload window.
4. Click **Save Version** in the top right corner.
5. Configure the instance as described in the Standard Integration Setup section.
6. Click **Save** to add the integration.
7. Test the integration by selecting it and clicking on **Test** to validate the URLs, token, and connection.

## Commands

This integration provides the following command:

### spur-context-api-enrich

**Description**: Enriches an IP address with detailed context from the Spur Context API.

**Input**:

- **ip**: The IP address to enrich.

**Output**:

- IP address details including associated autonomous system (AS), organization, infrastructure type, location, services, tunnels, risks, and client-specific data such as concentration, countries, spread, proxies, count, behaviors, and types.

**Example**:
\`\`\`
!spur-context-api-enrich ip=8.8.8.8
\`\`\`

## Use Cases

- Enriching IP addresses to identify potential security threats.
- Investigating suspicious IP addresses for malicious activities.
- Enhancing alerts with detailed IP context for better decision-making.

## Troubleshooting

If you encounter any issues with the integration, please ensure the following:

- The API Token is correctly entered and valid.
- The integration instance is properly configured with the correct settings.
- If using a proxy, ensure the proxy settings are correctly configured.
- For connectivity issues, verify network rules and permissions allow traffic from Cortex XSOAR to the Spur Context API endpoints.

For further assistance, contact Spur support or refer to the [Spur Context API documentation](https://docs.spur.us/context-api?id=context-api).
