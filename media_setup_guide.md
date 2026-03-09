# Add Media (Logo, Favicon, Screenshots)

You can easily customize the visual identity of your VesselIQ documentation by following these steps.

## 1. Application Logo

The logos are managed in the `logo/` directory and configured in `docs.json`.

- **To update**: Replace the following files in your folder:
  - `logo/light.svg` (for light mode)
  - `logo/dark.svg` (for dark mode)
- **If you use different file types (PNG, JPG)**:
  1. Save your files (e.g., `logo/my-logo.png`)
  2. Open `docs.json` and update the `logo` section:
     ```json
     "logo": {
       "light": "/logo/my-logo-light.png",
       "dark": "/logo/my-logo-dark.png"
     }
     ```

## 2. Favicon (The icon in the browser tab)

The favicon is located at the root of your project.

- **To update**: Replace the file `favicon.svg` at the root of your project with your own icon.
- **If you use another type (PNG, ICO)**:
  1. Save your file (e.g., `favicon.png`)
  2. Open `docs.json` and update the `favicon` field:
     ```json
     "favicon": "/favicon.png"
     ```

## 3. Application Screenshots

It is highly recommended to add screenshots for each tab to help users understand the interface.

### Step 1: Capture and Save
1. Take a screenshot of the desired tab in your application.
2. Save the image in the `images/` directory. Use descriptive names like `images/consultation-tab.png`.

### Step 2: Add to Documentation
Use the following markdown syntax in your MDX files (`guide/your-page.mdx`):

```md
![Description of what is shown in the image](/images/consultation-tab.png)
```

> [!TIP]
> You can also use Mintlify's `<Frame>` component for a better look with a border:
> ```md
> <Frame>
>   ![Description](/images/consultation-tab.png)
> </Frame>
> ```

---

## 4. Best Practices

- **Image Formats**: Use SVG for logos if possible for perfect sharpness. Use PNG or WEBP for screenshots.
- **File size**: Optimize your images (e.g., using TinyPNG) to keep the documentation loading fast.
- **Consistency**: Try to take screenshots with the same window size for a consistent look.
