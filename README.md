# WooCommerce MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/woocommerce)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect WooCommerce to AI assistants: products, orders, customers, coupons and sales reports.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — use WooCommerce from Claude, ChatGPT, Cursor, and other AI assistants through the Model Context Protocol (MCP).

<img src="images/woocommerce-icon.svg" alt="WooCommerce MCP Server" width="64" height="64">

## MCP Server URL

```
https://woocommerce.insightfulmcp.com/
```

## What is WooCommerce MCP?

WooCommerce MCP is a **remote Model Context Protocol server** hosted by InsightfulPipe. Access products, orders, customers, coupons, and sales analytics from your WooCommerce store.

## Installation

### Claude

1. Copy the MCP Server URL: `https://woocommerce.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://woocommerce.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http woocommerce https://woocommerce.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "woocommerce": {
      "url": "https://woocommerce.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

58 actions: 33 read, 25 write.

### Read Actions (33)

<details>
<summary>Show all 33 read actions</summary>

| Action | Description |
|--------|-------------|
| `get_attribute_term` | Get a specific attribute term by ID |
| `get_attribute_terms` | List all terms for a product attribute |
| `get_coupon` | Get a specific coupon by ID |
| `get_coupons` | List all coupons with filters and pagination |
| `get_customer` | Get a specific customer by ID |
| `get_customers` | List all customers with filters and pagination |
| `get_customers_report` | Get customers totals report |
| `get_order` | Get a specific order by ID |
| `get_order_notes` | List all notes for a specific order |
| `get_order_refunds` | List all refunds for a specific order |
| `get_orders` | List all orders with filters and pagination |
| `get_orders_report` | Get orders totals report |
| `get_product` | Get a specific product by ID |
| `get_product_attribute` | Get a specific product attribute by ID |
| `get_product_attributes` | List all product attributes |
| `get_product_categories` | List all product categories with pagination |
| `get_product_category` | Get a specific product category by ID |
| `get_product_review` | Get a specific product review by ID |
| `get_product_reviews` | List all product reviews with pagination |
| `get_product_tag` | Get a specific product tag by ID |
| `get_product_tags` | List all product tags with pagination |
| `get_product_variation` | Get a specific product variation by ID |
| `get_product_variations` | List all variations for a variable product |
| `get_products` | List all products with filters and pagination |
| `get_products_report` | Get top sellers report |
| `get_sales_report` | Get sales report with totals |
| `get_shipping_zone` | Get a specific shipping zone by ID |
| `get_shipping_zone_methods` | List all shipping methods for a zone |
| `get_shipping_zones` | List all shipping zones |
| `get_system_status` | Get WooCommerce system status (environment, database, plugins, etc.) |
| `get_tax_classes` | List all tax classes |
| `get_tax_rate` | Get a specific tax rate by ID |
| `get_tax_rates` | List all tax rates with pagination |

</details>

### Write Actions (25)

| Action | Description |
|--------|-------------|
| `create_attribute_term` | Create a new term for a product attribute |
| `create_coupon` | Create a new coupon |
| `create_customer` | Create a new customer |
| `create_order` | Create a new order |
| `create_order_note` | Create a note on an order |
| `create_order_refund` | Create a refund for an order |
| `create_product` | Create a new product |
| `create_product_attribute` | Create a new product attribute |
| `create_product_category` | Create a new product category |
| `create_product_review` | Create a new product review |
| `create_product_tag` | Create a new product tag |
| `create_product_variation` | Create a new variation for a variable product |
| `delete_order` | Delete an order by ID |
| `delete_product` | Delete a product by ID |
| `delete_product_review` | Delete a product review by ID |
| `update_attribute_term` | Update an existing attribute term |
| `update_coupon` | Update an existing coupon by ID |
| `update_customer` | Update an existing customer by ID |
| `update_order` | Update an existing order by ID |
| `update_product` | Update an existing product by ID |
| `update_product_attribute` | Update an existing product attribute |
| `update_product_category` | Update an existing product category |
| `update_product_review` | Update an existing product review |
| `update_product_tag` | Update an existing product tag |
| `update_product_variation` | Update an existing product variation |

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

```
"Show this month's sales report"
```

```
"Which products have the most reviews?"
```

```
"Create a 15% coupon code SPRING15"
```

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers.

- [Shopify MCP](https://insightfulpipe.com/mcp-servers/shopify)
- [Magento MCP](https://insightfulpipe.com/mcp-servers/magento)
- [Google Merchant Center MCP](https://insightfulpipe.com/mcp-servers/google-merchant-center)

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-woocommerce)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
