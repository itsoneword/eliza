# AI Character Configuration Parameters

## Core Parameters

### 1. Name [done]
- **Purpose**: Display name for your AI agent
- **Example**: "name": "SpaceExplorerAI"
- **Description**: Functions like a gamer tag, instantly identifying your AI agent

### 2. Clients [done]
- **Purpose**: Defines platforms where your agent operates
- **Options**: discord, twitter, direct console
- **Example**: "clients": ["discord", "direct"]
- **Note**: Platform selection affects agent's interaction capabilities

### 3. Model Provider 
- **Purpose**: Specifies the AI system powering your agent
- **Options**: OpenAI, Anthropic, local Llama models
- **Example**: "modelProvider": "openai"
- **Selection Criteria**: Based on cost, performance, availability

### 4. Settings
- **Purpose**: Stores configuration details in nested objects
- **Common Fields**:
  - voice: text-to-speech model configuration
  - secrets: API keys and sensitive information
  - model: override default model settings
- **Example**:
  "settings": {
    "voice": {
      "model": "en_US-female-medium"
    },
    "model": "gpt-3.5-turbo"
  }

## Character Definition

### 5. Plugins
- **Purpose**: Lists extra functionalities
- **Example**: "plugins": ["image-generation"]
- **Usage**: Enables specialized actions or external service integrations

### 6. Bio
- **Purpose**: Short statements about character background
- **Format**: Array of concise biographical statements
- **Example**:
  "bio": [
    "Expert in space exploration",
    "Trained in astrophysics research"
  ]

### 7. Lore
- **Purpose**: Extended backstory elements
- **Content**: Fictional details, motivations, special qualities
- **Example**:
  "lore": [
    "Legend says it was born on a colony orbiting Jupiter",
    "Shares universal knowledge across galaxies"
  ]

### 8. Knowledge
- **Purpose**: Default knowledge base
- **Content**: Facts and information the character knows
- **Example**:
  "knowledge": [
    "Knows rocket propulsion theory",
    "Understands cosmic radiation effects"
  ]

## Interaction Configuration

### 9. Message Examples
- **Purpose**: Sample chat interactions
- **Format**: Conversation snippets showing typical responses
- **Example**:
  "messageExamples": [
    {
      "user": "{{user1}}",
      "content": { "text": "How do rockets launch?" }
    },
    {
      "user": "SpaceExplorerAI",
      "content": { "text": "Rockets launch by igniting fuel to produce thrust that overcomes gravity." }
    }
  ]

### 10. Post Examples
- **Purpose**: Social media post templates
- **Content**: Example posts for platforms like Twitter
- **Example**: "postExamples": ["Today's cosmic thought: Jupiter could hold 1,300 Earths!"]

## Character Personality

### 11. Topics
- **Purpose**: Defines areas of expertise
- **Format**: Array of themes and subjects
- **Example**: "topics": ["interplanetary travel", "quantum physics", "stellar formation"]

### 12. Style
- **Purpose**: Defines behavior patterns
- **Scope**: Global and context-specific guidelines
- **Example**:
  "style": {
    "all": ["Keep responses friendly and informative"]
  }

### 13. Adjectives
- **Purpose**: Defines character personality traits
- **Format**: Array of descriptive words
- **Example**: "adjectives": ["enthusiastic", "compassionate"]

### 14. Relationships (Optional)
- **Purpose**: Defines connections with other characters
- **Usage**: Required only for multi-character setups
- **Content**: Character relationships and interactions

---

## Implementation Notes
Think of this configuration as creating a character in a game:
- Each field represents a different aspect of the character
- Bio, lore, and knowledge form the character's background
- Message examples and style guide their behavior
- Topics and adjectives shape their personality
- All elements work together to create a consistent, engaging AI agent