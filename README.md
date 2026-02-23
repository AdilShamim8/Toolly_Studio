# ✨ Toolly Studio

A powerful Streamlit app for generating professional product ads using Bria AI's advanced image generation and manipulation APIs.

## 🌟 Features

- 🖼️ Generate HD product images from text prompts
- 🎯 Remove backgrounds with custom colors
- 🌅 Add realistic shadows
- 🏠 Create lifestyle shots with text or reference images
- ✨ AI-powered prompt enhancement
- 📝 Optional CTA text overlay
- 🎮 Intuitive UI controls
- 💾 Easy image download

```mermaid
graph LR
    %% Custom Styling
    classDef root fill:#7c3aed,stroke:#fff,stroke-width:3px,color:#fff,font-weight:bold
    classDef folder fill:#3b82f6,stroke:#fff,stroke-width:2px,color:#fff
    classDef file fill:#f3f4f6,stroke:#cbd5e1,stroke-width:1px,color:#334155
    classDef feature fill:#10b981,stroke:#fff,stroke-width:2px,color:#fff
    classDef note fill:#fef08a,stroke:#eab308,stroke-width:1px,color:#854d0e

    %% Project Root
    Root["✨ Toolly_Studio<br/>(Streamlit + Bria AI)"]:::root

    %% Directories
    subgraph Architecture ["📂 Project Architecture"]
        direction TB
        Components[/"📁 components/"/]:::folder
        Services[/"📁 services/"/]:::folder
        Workflows[/"📁 workflows/"/]:::folder
    end

    %% Root Files
    subgraph RootFiles ["📄 Root Files"]
        App["app.py<br/>(Main Entry Point)"]:::file
        Env[".env<br/>(BRIA_API_KEY)"]:::note
        Readme["README.md"]:::file
        License["LICENSE"]:::file
    end

    %% Features Mapping
    subgraph Features ["🌟 App Features"]
        direction TB
        F1("🖼️ HD Image Gen"):::feature
        F2("🎯 BG Removal"):::feature
        F3("🌅 Real Shadows"):::feature
        F4("🏠 Lifestyle Shots"):::feature
        F5("✨ AI Prompts"):::feature
    end

    %% Tree Connections
    Root --> RootFiles
    Root --> Architecture

    %% Directory Contents
    Components --> C1("image_preview.py"):::file
    Components --> C2("sidebar.py"):::file
    Components --> C3("uploader.py"):::file

    Services --> S1("__init__.py"):::file
    Services --> S2("background_service.py"):::file
    Services --> S3("erase_foreground.py"):::file
    Services --> S4("generative_fill.py"):::file
    Services --> S5("hd_image_generation.py"):::file
    Services --> S6("lifestyle_shot.py"):::file
    Services --> S7("packshot.py"):::file
    Services --> S8("prompt_enhancement.py"):::file
    Services --> S9("shadow.py"):::file

    Workflows --> W1("generate_ad_set.py"):::file

    %% Logic / Data Flow
    App -.->|"Renders UI"| Components
    App -.->|"Executes"| Workflows
    Workflows -.->|"Consumes APIs"| Services
    
    %% Mapping Services to Features
    S5 -.-> F1
    S2 -.-> F2
    S9 -.-> F3
    S6 -.-> F4
    S8 -.-> F5
```

## 🚀 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/AdilShamim8/Toolly_Studio.git
cd adsnap-studio
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the root directory:
```bash
BRIA_API_KEY=your_api_key_here
```

4. Run the app:
```bash
streamlit run app.py
```

## 💡 Usage

1. Enter a product description or upload an image
2. Configure generation options in the sidebar:
   - Enhance prompt with AI
   - Remove background
   - Add shadows
   - Generate lifestyle shots
3. Adjust advanced settings like background color and shadow intensity
4. Click "Generate Ad" to create your images
5. Download the results

## 🔧 Configuration

The app supports various configuration options through the UI:

- **Prompt Enhancement**: Improve your text prompts with AI
- **Background Removal**: Remove backgrounds with custom colors
- **Shadow Effects**: Add realistic shadows with adjustable intensity
- **Lifestyle Shots**: Place products in context using text or reference images
- **CTA Text**: Add optional call-to-action text overlays

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Bria AI](https://bria.ai) for their powerful image generation APIs
- [Streamlit](https://streamlit.io) for the amazing web framework 
