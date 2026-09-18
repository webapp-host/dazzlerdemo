# Project Dazzler — full single-page demo

A static GitHub Pages demo combining the project information sections with the latest custom ArcGIS 3D scene tour (v4). No build tools or server are required.

## Publish with GitHub Pages

1. Create a GitHub repository, for example `project-dazzler-demo`.
2. Unzip this package. Upload the **contents** of `project-dazzler-github-demo` to the repository root: `index.html`, `favicon.ico`, `assets/`, `.nojekyll`, and this README. Do not upload only the ZIP or put the website inside an extra nested folder. GitHub's web uploader can drag the assets folder; `.nojekyll` is optional for this plain HTML site if hidden files are omitted.
3. Open the repository **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, select **main** and **/(root)**, then Save.
5. GitHub will display the website address when deployment finishes, typically `https://YOUR-USERNAME.github.io/project-dazzler-demo/`.

For local testing, run `python3 -m http.server 8000` from the website folder and open `http://localhost:8000`. Avoid opening the HTML directly as a local file.

## Included sections

Project introduction and rendering; project overview and landscape; construction schedule (responsive graphic); custom 3D site tour and six viewpoint cards; twelve expandable FAQs; careers and jobs links; three playable traffic simulations; five project document links; demonstration contact form; footer with reference policy links.

## Tour behavior preserved

- Uses web scene `60e259c5520647bb89bbcce159a12778` and its existing location layer and 3D cone symbols. No duplicate point markers are created.
- The layer fields `Name` and `VideoLink` provide titles and Vimeo videos. Point attachments provide the viewpoint-card thumbnails.
- Selecting a point opens video on the right and moves the camera to the side away from `DZL1ASITELAYOUT_Polygon_ConstBoundary`, facing toward the boundary center.
- Camera setback is 350 meters, and elevation is approximately 300 feet (91.44 meters) above terrain at the camera position.
- The map fills the left pane height. There is no thumbnail below the selected video.
- Close/Escape clears the player and expands the scene. Reset restores the initial scene viewpoint.

Edit `CONFIG` in `index.html` to change the scene, layer, field names, camera setback, or camera height.

## Hosting and external services

GitHub hosts the HTML and the included image assets. ArcGIS hosts the scene, terrain, 3D layers, and location attachments; Vimeo hosts tour media. Traffic videos and PDF downloads remain linked to the original reference site's media service. Careers and legal links open their original sites. These services must remain available for the corresponding features to work. ArcGIS items must be shared for the intended audience; this demo does not supply an authentication flow.

Vimeo privacy settings must allow the GitHub Pages domain. Direct Vimeo playback URLs in the feature layer can expire; a stable Vimeo page/embed URL is preferable for long-term use. No ArcGIS account password or API key is embedded in the source; the remote scene manages its own dependencies.

The form is deliberately demo-only: no messages are sent or stored. GitHub Pages does not process form submissions. A client launch requires a chosen form service or backend, plus approved privacy content.

## Reference content and customization

Content and graphics were obtained from `https://www.projectdazzler.com/` for this requested demonstration. This is labeled as a demo, not the official project site. Change project copy, images, schedule, FAQs, document links, career links, footer, and scene settings when adapting it to a new client. Reference graphics and text are a snapshot, not automatically synchronized.

## Validation

Checked HTML structure, section anchors, unique IDs, required local assets, JavaScript syntax, and preservation of the v4 tour script. Live rendering and external video playback should be reviewed in a WebGL-capable browser after publishing. The deployment has not been made from this package.

## Green theme and favicon

The demo uses the reference website’s forest green (`#084434`) and secondary green (`#145f4b`) throughout its header, panels, buttons, and accents. `favicon.ico` is the reference website’s icon and is included at the repository root. Upload it along with the updated HTML and assets.
