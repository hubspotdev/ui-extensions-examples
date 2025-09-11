# HubSpot UI Extensions Examples

A collection of example projects showcasing app cards built with [HubSpot's UI Extensions](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview). These examples demonstrate how to build customized experiences that integrate seamlessly into the HubSpot CRM interface.

## About HubSpot UI Extensions

HubSpot UI Extensions enable developers to create custom app cards that display directly within HubSpot's interface. These cards can:

- Display data from third-party systems
- Allow users to perform actions without leaving HubSpot
- Provide customized experiences tailored to specific workflows
- Integrate with CRM records, preview panels, help desk, and sales workspaces

App cards are built using React and HubSpot's UI Extensions SDK, giving you access to HubSpot's design system and data components while maintaining a native user experience.

## Example Projects

This repository contains four distinct projects that showcase different aspects of UI Extensions:

### 📊 [Charts](./charts/)
Build customized data visualizations by fetching data from third-party systems and displaying them as interactive charts within HubSpot records.

### 📚 [Deal Generator](./deal-generator/)
A comprehensive example featuring both frontend and backend components that integrates with the Open Library API to search for books, manage a shopping cart, and generate HubSpot deals.

### 🏭 [Samples by Industry](./samples-by-industry/)
Industry-specific app card examples including Education, Manufacturing, and Healthcare use cases, demonstrating real-world applications across different sectors.

### 🖼️ [Tabbed Photo Carousel](./tabbed-photo-carousel/)
An interactive product showcase combining image carousels with tabbed interfaces to display detailed product specifications and information.

## Getting Started

### Prerequisites

- Active HubSpot account
- [HubSpot CLI](https://developers.hubspot.com/docs/developer-tooling/local-development/hubspot-cli/install-the-cli#install-the-hubspot-cli) installed globally
- Basic knowledge of React and TypeScript

### Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/hubspotdev/ui-extensions-examples
   cd ui-extensions-examples
   ```

2. **Choose a project**
   Navigate to any of the example directories and follow the individual README instructions.

3. **Set up HubSpot CLI**
   ```bash
   npm install -g @hubspot/cli@latest
   hs account auth
   ```

4. **Install and deploy**
   From within any project directory:
   ```bash
   hs project install-deps
   hs project upload
   hs project dev
   ```

## Resources & Documentation

### 📖 Official Documentation
- [App Cards Overview](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/app-cards/overview) - Comprehensive guide to building app cards
- [UI Extensions SDK](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/ui-extensions-sdk) - Technical documentation for the SDK
- [UI Components](https://developers.hubspot.com/docs/apps/developer-platform/add-features/ui-extensibility/ui-components) - Available components and design system
- [Building with React](https://developers.hubspot.com/react-on-hubspot-hubspot-developers?hs_preview=hUvmllQN-180619360655) - Landing page for React-based app development

### 🎥 Video Resources
- [HubSpot Developers YouTube Channel](https://www.youtube.com/@HubSpotDevelopers) - Tutorials, demos, and developer content
- [HubSpot Developer Community](https://developers.hubspot.com/community) - Interact and engage with other HubSpot developers

### 🛠️ Developer Tools
- [HubSpot CLI Documentation](https://developers.hubspot.com/docs/apps/developer-platform/developer-tooling/hubspot-cli) - Command-line tools for development
- [Developer Account Setup](https://developers.hubspot.com/docs/getting-started/quickstart) - Get started with HubSpot development

## Contributing

These examples are maintained by the HubSpot Developer Relations team. Each project includes detailed setup instructions and code comments to help you understand the implementation patterns.

## Support

- [HubSpot Developer Forums](https://community.hubspot.com/t5/HubSpot-Developers/ct-p/developers) - Community support and discussions
- [HubSpot Developer Documentation](https://developers.hubspot.com/) - Complete developer resources

---

*Ready to build your own app cards? Start with one of the examples above and customize it for your specific use case!*
