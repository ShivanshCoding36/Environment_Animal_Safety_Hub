# Pull Request: Add Text-to-Speech Button (#702)

## Description
This PR implements a **Text-to-Speech (TTS)** feature for community posts, allowing users to listen to post descriptions instead of reading them. This enhances accessibility and provides an alternative way to consume content.

## Changes Made

### Modified Files:
1. **`frontend/js/pages/community/post.js`**
   - Added TTS button to post actions in both loaded posts and newly created posts
   - Implemented Web Speech API integration with speech synthesis
   - Added toggle functionality: click to start reading, click again to stop
   - Button changes icon from volume (▶) to stop (⏹) when speaking
   - Handles both `onend` and `onerror` events for proper state management

2. **`frontend/css/pages/community.css`**
   - Added styling for `.tts-btn` class
   - Implemented smooth hover effects with scale transformation
   - Added pulsing animation when TTS is active
   - Maintained consistent color scheme with the rest of the UI

## Features
✅ **Accessibility**: Users can listen to posts instead of reading  
✅ **Toggle Control**: Click to play, click again to stop  
✅ **Visual Feedback**: Icon changes and pulses during speech  
✅ **Error Handling**: Gracefully handles speech synthesis errors  
✅ **Consistent UI**: Matches existing design patterns  

## Technical Details
- Uses browser's native **Web Speech API** (SpeechSynthesisUtterance)
- Speech rate: 1.0 (normal speed)
- Language: English (en-US)
- No external dependencies required

## Testing
- [x] TTS button appears on all posts
- [x] Clicking button reads post description aloud
- [x] Icon toggles between volume and stop
- [x] Animation plays while speaking
- [x] Speech stops when clicking stop button
- [x] Works on newly created posts
- [x] Compatible with existing features (likes, comments, reactions)

## Screenshots
The TTS button (🔊) appears in the post actions bar alongside like, comment, and bookmark buttons. When active, it displays a pulsing blue stop icon.

---

**Closes #702**
