# VRChat Profile Embed

Easily embed your VRChat profile card on any website using the embed that is hosted at droot.me.

## Usage Options

### Full Page Embed
```html
<iframe 
    src="https://www.droot.me/home/vrc/embed?username=YourName" 
    style="width: 100%; height: 100vh; border: none; position: fixed; top: 0; left: 0;" 
    frameborder="0">
</iframe>
```

### Widget Embed
```html
<iframe 
    src="https://www.droot.me/home/vrc/embed?username=YourName" 
    width="400" 
    height="600" 
    frameborder="0">
</iframe>
```

## Configuration

## How to Customize

The base URL is `https://www.droot.me/home/vrc/embed`

To customize, add your parameters after `?` like this:

1. Start with the base URL:
```
https://www.droot.me/home/vrc/embed
```

2. Add your first parameter with `?`:
```
https://www.droot.me/home/vrc/embed?username=YourName
```

3. Add more parameters with `&`:
```
https://www.droot.me/home/vrc/embed?username=YourName&vrchatId=usr_123456789
```

4. Add complex parameters like social links or theme:
```
https://www.droot.me/home/vrc/embed?username=YourName&socials[discord]=123456789&theme[headerBg]=%23461685
```

### Required Parameters
| Parameter | Description | Example |
|-----------|-------------|---------|
| `username` | Your VRChat display name | `username=CoolUser` |
| `vrchatId` | Your VRChat user ID | `vrchatId=usr_123456789` |
| `profilePic` | Your VRChat profile image | `profilePic=https://url.com` |

### Social Media Links
```
?socials[discord]=123456789
&socials[bluesky]=username.bsky.social
&socials[twitter]=twitterhandle
&socials[twitch]=twitchusername
&socials[github]=githubuser
```

### Theme Colors (Use %23 for #)
```
?theme[headerBg]=%23ff0000          // Header background
&theme[headerBorder]=%23cc0000      // Header border
&theme[buttonBg]=%230000ff          // Button background
&theme[buttonBorder]=%230000cc      // Button border
&theme[buttonHoverBg]=%230000dd     // Button hover background
&theme[buttonHoverBorder]=%230000aa // Button hover border
```

### Navigation Buttons
In order to disable them or enable them using true/false
```
?showGallery=true
&showAvatars=true
&showWorlds=true
```

### Navigation Buttons
The buttons are enabled by default and will link to VRChat's default pages. To customize the URLs:
```
?&galleryUrl=https://your-domain.com/img
&avatarsUrl=https://your-domain.com/avatars
&worldsUrl=https://your-domain.com/worlds
```

## Full Example
```html
<iframe 
    src="https://www.droot.me/home/vrc/embed?username=CoolUser&vrchatId=usr_123456789&socials[discord]=123456789&theme[headerBg]=%23461685&theme[headerBorder]=%236929c4&theme[buttonBg]=%23461685&theme[buttonBorder]=%236929c4&theme[buttonHoverBg]=%236929c4&theme[buttonHoverBorder]=%238a3ddb" 
    style="width: 100%; height: 100vh; border: none; position: fixed; top: 0; left: 0;" 
    frameborder="0">
</iframe>
```

### Purple Theme Colors Used:
```
headerBg: #461685       // Deep purple
headerBorder: #6929c4   // Medium purple
buttonBg: #461685      // Deep purple (same as header)
buttonBorder: #6929c4  // Medium purple
buttonHoverBg: #6929c4    // Medium purple
buttonHoverBorder: #8a3ddb // Light purple
```

### Note on URL Formatting
⚠️ **Important**: The URL must be on a single line without breaks or spaces. For example:

❌ Incorrect (will cause 404):
```
https://www.droot.me/home/vrc/embed
    ?username=CoolUser
    &vrchatId=usr_123456789
```

✅ Correct:
```
https://www.droot.me/home/vrc/embed?username=CoolUser&vrchatId=usr_123456789
```

## Best Practices

- **Full Page Embed**: 
  - Great for dedicated profile pages
  - Uses entire viewport
  - No additional styling needed

- **Widget Embed**:
  - Minimum width: 400px
  - Recommended height: 600px
  - Good for sidebars or profile sections

- Use HTTPS for secure embedding
- Test configuration before deploying
- Only enable navigation buttons if you have the corresponding pages ready

## Quick Start Template
Download my [example HTML file](example.html) to get started quickly. This template includes:
- Proper HTML structure
- Meta tags for SEO
- Viewport settings for mobile
- Purple theme preset
- Full-page embed setup

Simply download, replace "YourName" and "usr_xxxx" with your details, and you're ready to go!

## Support
For issues or questions, click [here](https://github.com/dRootDev/vrchat-profile-embed/issues)
