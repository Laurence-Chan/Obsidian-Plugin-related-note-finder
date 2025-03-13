# AI Tag Generator and Topic Clustering

A powerful Obsidian plugin that uses artificial intelligence to automatically generate tags for notes and organizes notes into topic clusters based on content similarity, helping you better manage and discover knowledge connections.

## ✨ Main Features

### 🏷️ AI Tag Generation
- **Automatically Tag All Notes**: One-click generation of relevant tags for all notes in your vault
- **Tag Current Note**: Quickly generate tags for the currently open note
- **Customize Tag Count**: Flexibly set the maximum number of tags per note (1-20)
- **Custom Prompt Template**: Adjust the prompt for tag generation according to your needs

### 📊 Topic Clustering Analysis
- **Note Topic Analysis**: Automatically analyze all notes in your vault to discover potential topic clusters
- **Topic Browser**: Intuitively view all topics and their contained notes
- **Related Notes Discovery**: Easily find all notes related to a specific topic
- **Customizable Cluster Count**: Adjust the number of topic clusters based on the scale and diversity of your vault

### 🔍 Smart Search and Filtering
- **Search Within Topics**: Search for specific notes or keywords in the topic browser
- **Tag Filtering**: Quickly filter related notes by tags

## 🛠️ Installation Method

### Manual Installation
1. Download the latest release package
2. Extract the downloaded zip file
3. Copy the extracted folder to your Obsidian vault's `.obsidian/plugins/` directory
4. Enable the plugin in Obsidian settings

## ⚙️ Configuration Guide

### AI Tag Generator Settings
1. **API Key**: Enter your API key (e.g., DeepSeek API key)
2. **API Endpoint**: Set the endpoint URL for the LLM API
   - OpenAI: `https://api.openai.com/v1/chat/completions`
   - DeepSeek: `https://api.deepseek.com/v1/chat/completions`
3. **API Model**: Choose the LLM model to use (e.g., `gpt-3.5-turbo` or `deepseek-chat`)
4. **Maximum Tag Count**: Set the maximum number of tags to generate for each note (1-20)
5. **Prompt**: Customize the prompt template sent to the AI

### Topic Clustering Settings
1. **Embedding API Key**: API key for generating text vectors (can be shared with the tag generator)
2. **Embedding API Endpoint**: API endpoint URL for generating text vectors
3. **Embedding Model**: Model for generating text vectors (e.g., `text-embedding-ada-002`)
4. **Cluster Count**: Set how many topic clusters to divide notes into (2-20)

### About API Support
This plugin supports various LLM API services, including:
- OpenAI API
- DeepSeek API
- Other API services compatible with OpenAI format

## 📝 User Guide

### AI Tag Generation

#### Tag Current Note
1. Open a note
2. Use the command palette (Ctrl+P) to execute the "Tag Current Note" command
3. Wait a few seconds, and the newly generated tags will appear at the top of the note

#### Tag All Notes
1. Click the "Tag All Notes" button on the settings page, or execute the corresponding command from the command palette
2. Wait for the process to complete; status will be displayed on the interface
3. Processing a large number of notes may take some time, please be patient

### Topic Clustering Analysis

#### Analyze Note Topics
1. Click the "Analyze Note Topics" button on the settings page, or execute the corresponding command from the command palette
2. Wait for the analysis to complete; status will be displayed on the interface
3. **Note**: For better clustering results, it's recommended to complete tag generation for all notes first

#### Using the Topic Browser
1. Click the topic browser icon in the left sidebar, or open the topic browser using the command palette
2. In the topic browser, you can:
   - View all automatically discovered topics and their keywords
   - Click a topic title to expand/collapse and view included notes
   - Use the search box to search for specific notes or keywords
   - Click a note title to jump directly to the corresponding note

## 🔧 How It Works

### AI Tag Generation
1. The plugin extracts note content
2. It uses the configured LLM API to generate relevant tags
3. Tags use Obsidian's standard "#tag" format
4. Generated tags are placed at the beginning of the note

### Topic Clustering
1. The plugin uses the Embedding API to generate vector representations for each note
2. It enhances vector representations by combining note content and existing tag information
3. It uses the K-means clustering algorithm to group similar notes
4. It uses LLM to generate descriptive labels for each cluster
5. Clustering results are saved and displayed in the topic browser

## 📋 Notes

- Tags will be added at the top of the note
- Before tagging, the plugin will automatically remove existing tags
- Using the API will consume API tokens, please be mindful of usage
- Topic clustering results are automatically saved and can be viewed after restarting Obsidian
- For best results, it's recommended to complete tag generation before performing topic clustering

## 📈 Best Practices

1. **Generate tags first, then cluster**: Tag information enriches clustering and improves topic identification accuracy
2. **Adjust cluster count appropriately**: Adjust based on the size of your note vault; use a smaller cluster count when you have fewer notes
3. **Update clustering regularly**: Re-run topic analysis after adding a significant number of new notes
4. **Discover knowledge connections using the topic browser**: Explore similar notes through the topic browser to discover new knowledge associations

## 🔒 Privacy Statement

- All processing is done locally; only API requests send note content to the configured API service
- No user data is collected or uploaded
- Clustering results are saved in your local Obsidian vault

## 📄 License

MIT

## 🙏 Acknowledgements

- Thanks to the Obsidian team for providing the plugin development framework
- Thanks to the LLM API providers
- Thanks to all users who provided feedback and suggestions 