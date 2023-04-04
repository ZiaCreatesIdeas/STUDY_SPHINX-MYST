
(learn-myst)=
## Learn Myst Markdown
This is a list of the minimum specifications required to create useful documention.

- Carriage return / Line Break
- Horizontal Rule
- Multiple size headers
- Codeblocks (copy code button)
- Comments
- Embedded Images
- Admonition
- Note
- Embedded Video (Onedrive)
- Links [Section, Page, External]
- Escape Special Characters
- Theme Variations (dark)

#### Carriage Return / Line Break

In Myst, line breaks can be accomplished by adding two spaces at the end or backslash.

    '  '
    \

This is a line break  
as we typically get in code using \'\n'.  
But here instead we end the line with two spaces.  
Or we can use\
a backslash.

#### Horizontal Rule / Line across page)
Consists of three dashes. Sphinx calls these 'transitions'.

    ---

--- 
#### Code Blocks
Code Block are created by indenting four spaces.

    Indent (four spaces gives us an code block.
    A space above to separate the block from any preceding text may be required.
---

#### Comments
Comments use the '%' to precede the comment.

    %
    [//]: # (This is a comment.)
    [//]: # (This is a
    multiline comment.
    It can span multiple lines.)
    
```{note} 
:class: warning

Spaces must be included around ': # ('

``` 

% comment
[\\]: # (why all this for
 a comment)
---

#### Embedded Images
Embedded images use:

    ![alt](src "title")
    ![A cute cat](https://example.com/cat.jpg "A cute cat")
    
![cartoon fish](./_static/fun-fish.png "fun fish graphic")

---


Using the HTML tag \'img' we can align and ajust the size of an image.

    <img src="image_file_path" alt="alternate_text">
    <img src="./_static/fun-fish.png" alt="cartoon fish" align="left" width="100">
    XHTML tags should be closed, HTML5 do not.
<p>  
<br>    
<img src="./_static/fun-fish.png" alt="cartoon fish" align="left" width="100">
<br>
</p>

Without using 'div' statements, we have a problem.  

    <div style="display:block; text-align:center;">
    <img src="./_static/fun-fish.png" alt="cartoon fish" align="center" width="100">
    </div>
   
<div style="display:block; text-align:center;">
  <img src="./_static/fun-fish.png" alt="cartoon fish" align="center" width="125">
</div>

Alternately we use margin:auto to center:

    <div style="display:block; text-align:center;">
    <img src="./_static/fun-fish.png" alt="cartoon fish" width="100" style="margin:auto;">
    </div>

<div style="display:block; text-align:center;">
  <img src="./_static/fun-fish.png" alt="cartoon fish" width="125" style="margin:auto;">
</div>

---

Image right align:

    <div style="text-align: right;">
    <img src="./_static/fun-fish.png" alt="alt text" style="float: right; margin-left: 10px; display: block; clear: right;">
    <img src="./_static/fun-fish.png" alt="alt text" style="float: right; margin-left: 10px; display: block; clear: right;">
    </div>

<div style="display:block; text-align: center;">
  <img src="./_static/fun-fish.png" alt="alt text" width="150" style="float: right; margin-left: 10px; display: block; clear: right;">
  <img src="./_static/fun-fish.png" alt="alt text" width="150" style="float: right; margin-left: 10px; display: block; clear: right;">
</div>

<div style="display:block; text-align: right;">
  <img src="./_static/fun-fish.png" alt="cartoon fish" width="150" style="float: right;">
</div>

```
<div style="text-align:right;">
  <img src="./_static/fun-fish.png" alt="alt text" width="150" style="display:block;">
</div>

```
---
We can flop an image using:

    <div style="display:block; text-align:center; transform: scaleX(-1);">
    <img src="./_static/fun-fish.png" alt="cartoon fish" align="right" width="150">
    </div>   

<div style ="display:block">
   <div style="display:block; text-align:center; transform: scaleX(-1);">
     <img src="./_static/fun-fish.png" alt="cartoon fish" width="125" style="margin:auto;">
   </div>
</div>

---

#### Admonition!

Here is how to add Admonition.

    ```{admonition} Here's my title
    :class: warning

    Here's my admonition content
    ```  

```{admonition} Here's my title
:class: warning

Here's my admonition content
```

[Admonition vis Code Fence (Myst)](https://myst-parser.readthedocs.io/en/v0.17.1/syntax/optional.html#syntax-header-anchors)

    ::::{important}
    :::{note}
    This text is **standard** _Markdown_
    :::
    :::: 

::::{important}
:::{note}
This text is **standard** _Markdown_
:::
::::

Notes done with Code Fences can be bolded.\
We can also use 'div' statements to alter the background. 

    <div class="admonition note" name="html-admonition" style="background: lightgreen; padding: 10px">
    <p class="title">This is the **title**</p>
    This is the *content*
    </div>


<div class="admonition note" name="html-admonition" style="background: lightgreen; padding: 10px">
<p class="title">This is the **title**</p>
This is the *content*
</div>

---
#### Note!

Here is how to add a Note.

    ```{note} Here's my title
    :class: warning

    Here's my note content
    ```    

```{note} Here's my title
:class: warning

Here's note content

``` 
---
#### Grids
Grids!

    ::::{grid} 1 2 3 4
    :outline:
    
    :::{grid-item}
    A
    :::
    :::{grid-item}
    B
    :::
    :::{grid-item}
    C
    :::
    :::{grid-item}
    D
    :::
    ::::
          

::::{grid} 1 2 3 4
:outline:

:::{grid-item}
A
:::
:::{grid-item}
B
:::
:::{grid-item}
C
:::
:::{grid-item}
D
:::
::::

---
#### Cards

:::{card} Card Title

Card content
:::

---
:::{card} Card Title
Header
^^^
Card content
+++
Footer
:::

---
**Cards in a Grid**

    ::::{grid} 2
    :::{grid-item-card}  Title 1
    A
    :::
    :::{grid-item-card}  Title 2
    B
    :::
    ::::

::::{grid} 2
:::{grid-item-card}  Title 1
<iframe width="280" height="145" src="https://www.youtube.com/embed/t9xd0hBC_v8?start=14" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
:::
:::{grid-item-card}  Title 2
<iframe width="280" height="145" src="https://www.youtube.com/embed/t9xd0hBC_v8?start=14" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
:::
::::

%<script src="https://cdnapisec.kaltura.com/p/3200283/embedPlaykitJs/uiconf_id/47254103"></script>
---
#### Embed Video

---

000
<div data-test="embeddedWebinarWithQ&amp;A-component" class="rf-attribute embeddedWebinarWithQ&amp;A-component"><div class="rf-webinar-content rf-flex-frame with-qanda"><div class="rf-video-player rf-kaltura-player"><script src="https://cdnapisec.kaltura.com/p/3200283/embedPlaykitJs/uiconf_id/47254103"></script><div id="djJ8MzIwMDI4M3zALh59e31Ad91DNE_aYIFPNlAKTgdQYec2MNkEw76zXvK83X94nQQp1xcMgvxplwfRgYpXIQLl4fl97rVf-iSrAkFK0zDHZJyudu_-uE4n9DUfQsO9bYsRSasL3_Ck2LzHH83v-sJVXRnCSBJ7UQ-S0RSBT-kG-Wv-zfnfVDHJOWyrDxqiraMnc1XrLbG_dBSavoIFHxbVM32lckwgpiallH0gREGBSH-IXkVq7JzDEezog-ANMh-wXQWGANq-3FwDrHZeNKptzMRwW0zMsNP4Y4i1zfyKt8ui-9B1Pdmh_mjRErjxLpGajCrSllFrFTg=" class="rf-player-inner"><div id="_68fid" class="kaltura-player-container" tabindex="-1"><div tabindex="0" aria-label="Video Player" class="playkit-player  playkit-Mac-OS playkit-Firefox playkit-hover playkit-metadata-loaded playkit-state-paused playkit-size-lg notranslate"><span></span><div id="_68fid-video" class="playkit-video-player" style="position: absolute; inset: 0px;"><div class="playkit-container" id="_k04f3" tabindex="-1"><video id="_proy4" class="playkit-engine playkit-engine-html5" playsinline="" src="blob:https://register.nvidia.com/d7eb5b47-8d5e-0149-8d28-0e959b6eb0ec"></video><div class="playkit-black-cover" style="visibility: hidden;"></div><div id="_epqca" tabindex="-1" class="playkit-poster" style="background-image: url(&quot;https://cfvod.kaltura.com/p/3200283/sp/320028300/thumbnail/entry_id/1_q1aqr1af/version/100011/height/488/width/868&quot;); display: none;"></div><div class="playkit-subtitles"><div style="position: absolute; inset: 0px; margin: 1.5%;"></div></div><div id="playkit-bumper-container_k04f3" class="playkit-bumper-container" style="visibility: hidden;"><video></video><div class="playkit-bumper-cover"></div><a class="playkit-bumper-click-through" target="_blank"></a></div></div></div><div><div class="playkit-player-gui" id="player-gui"><div style="position: absolute; inset: 0px;" class="playkit-overlay-action "></div><div style="position: absolute; inset: 0px;" class="playkit-video-area"><div style="pointer-events: auto;"><div aria-live="polite" tabindex="-1" class="offline-slate__slate-wrapper___pobqn "></div></div></div><div style="position: absolute; inset: 0px;" class="playkit-gui-area"><div style="pointer-events: auto;"><div class="overlay-portal" aria-live="polite"></div><div class="playkit-playback-controls playkit-center-playback-controls"><div class="playkit-control-button-container playkit-control-play-pause"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Play" class="playkit-control-button"><div><i class="playkit-icon playkit-icon-play"></i><i class="playkit-icon playkit-icon-pause"></i></div></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Play</span></div></div></div></div><div class="playkit-top-bar"><div class="playkit-top-bar-area"></div><div class="playkit-left-controls"></div><div class="playkit-right-controls"></div></div><div class="playkit-interactive-area"><div style="pointer-events: auto;"></div></div><div class="playkit-bottom-bar playkit-line-break"><div class="playkit-bottom-bar-area"><div tabindex="0" class="playkit-seek-bar" role="slider" aria-label="Seek slider" aria-valuemin="0" aria-valuemax="2376" aria-valuenow="404" aria-valuetext="06:43 of 39:36"><div class="playkit-progress-bar"><div class="playkit-frame-preview" style="left: 778.499px;"><div style="height: 96px; width: 168px;" class="playkit-frame-preview-img-container playkit-non-sticky"><div class="playkit-frame-preview-img" style="background: rgba(0, 0, 0, 0) url(&quot;https://cfvod.kaltura.com/p/3200283/sp/320028300/thumbnail/entry_id/1_q1aqr1af/version/100011/width/164/vid_slices/100&quot;) repeat scroll -15252px 0px;"></div></div></div><div class="playkit-time-preview" style="left: 778.499px;">36:52</div><div class="playkit-buffered" style="width: 0%;"></div><div class="playkit-progress" style="width: 16.9918%;"><a class="playkit-scrubber"></a></div><div class="playkit-virtual-progress" style="width: 93.1219%;"><div class="playkit-virtual-progress-indicator"></div></div></div></div></div><div class="playkit-left-controls"><div class="playkit-playback-controls "><div class="playkit-control-button-container playkit-control-play-pause"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Play" class="playkit-control-button"><div><i class="playkit-icon playkit-icon-play"></i><i class="playkit-icon playkit-icon-pause"></i></div></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-right playkit-hide">Play</span></div></div></div><div class="playkit-control-button-container playkit-control-rewind playkit-no-idle-control"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Seek backwards" class="playkit-control-button"><i class="playkit-icon playkit-icon-rewind-10"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Seek backwards</span></div></div><div class="playkit-control-button-container playkit-control-forward playkit-no-idle-control"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Seek forward" class="playkit-control-button"><i class="playkit-icon playkit-icon-forward-10"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Seek forward</span></div></div><div class="playkit-time-display"><span>06:43 / 39:36</span></div></div><div class="playkit-right-controls"><div class="playkit-control-button-container playkit-control-volume playkit-volume-control" role="application"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-live="polite" aria-label="100% volume. Click to mute" class="playkit-control-button"><i class="playkit-icon playkit-icon-volume-base"></i><i class="playkit-icon playkit-icon-volume-waves"></i><i class="playkit-icon playkit-icon-volume-mute"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-left playkit-hide">Mute</span></div><div class="playkit-volume-control-bar" role="slider" aria-valuemin="0" aria-valuemax="100" aria-valuenow="100" aria-valuetext="100% volume "><div class="playkit-bar"><div class="playkit-progress" style="height: 100%;"></div></div></div></div><div class="playkit-control-button-container playkit-control-language"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-haspopup="true" aria-label="Language" class="playkit-control-button"><i class="playkit-icon playkit-icon-language"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Language</span></div><div></div></div><div class="playkit-control-button-container playkit-control-settings"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Settings" class="playkit-control-button playkit-button-badge playkit-badge-icon playkit-icon-quality-hd-active "><i class="playkit-icon playkit-icon-settings"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Settings</span></div></div><div class="playkit-control-button-container playkit-control-fullscreen"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Fullscreen" class="playkit-control-button"><i class="playkit-icon playkit-icon-maximize"></i><i class="playkit-icon playkit-icon-minimize"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Fullscreen</span></div></div></div></div></div></div></div><div style="width: 286.44px; right: -286.44px; opacity: 0;" class="playkit-side-panel playkit-vertical-side-panel"><div class="playkit-side-panel-content"></div></div><div style="width: 286.44px; left: -286.44px; opacity: 0;" class="playkit-side-panel playkit-vertical-side-panel"><div class="playkit-side-panel-content"></div></div><div style="height: 161.123px; top: -161.123px; opacity: 0;" class="playkit-side-panel playkit-horizontal-side-panel"><div class="playkit-side-panel-content"></div></div><div style="height: 161.123px; bottom: -161.123px; opacity: 0;" class="playkit-side-panel playkit-horizontal-side-panel"><div class="playkit-side-panel-content"></div></div></div></div></div><script type="text/javascript">var kalturaPlayer = KalturaPlayer.setup({
        targetId: 'djJ8MzIwMDI4M3zALh59e31Ad91DNE_aYIFPNlAKTgdQYec2MNkEw76zXvK83X94nQQp1xcMgvxplwfRgYpXIQLl4fl97rVf-iSrAkFK0zDHZJyudu_-uE4n9DUfQsO9bYsRSasL3_Ck2LzHH83v-sJVXRnCSBJ7UQ-S0RSBT-kG-Wv-zfnfVDHJOWyrDxqiraMnc1XrLbG_dBSavoIFHxbVM32lckwgpiallH0gREGBSH-IXkVq7JzDEezog-ANMh-wXQWGANq-3FwDrHZeNKptzMRwW0zMsNP4Y4i1zfyKt8ui-9B1Pdmh_mjRErjxLpGajCrSllFrFTg=',
        provider: {
          partnerId: '3200283',
          uiConfId: '47254103',
          ks: 'djJ8MzIwMDI4M3zALh59e31Ad91DNE_aYIFPNlAKTgdQYec2MNkEw76zXvK83X94nQQp1xcMgvxplwfRgYpXIQLl4fl97rVf-iSrAkFK0zDHZJyudu_-uE4n9DUfQsO9bYsRSasL3_Ck2LzHH83v-sJVXRnCSBJ7UQ-S0RSBT-kG-Wv-zfnfVDHJOWyrDxqiraMnc1XrLbG_dBSavoIFHxbVM32lckwgpiallH0gREGBSH-IXkVq7JzDEezog-ANMh-wXQWGANq-3FwDrHZeNKptzMRwW0zMsNP4Y4i1zfyKt8ui-9B1Pdmh_mjRErjxLpGajCrSllFrFTg='
        },
        playback: {
          preload: 'auto',
        },
        session: {
          userId: '1677186177669001vvYa'
        },
        ui: {
          debug: true
        },
        plugins: {
          undefined,
          'kaltura-live': {
            checkLiveWithKs: false,
            isLiveInterval: 10
          }
        }
      });
      kalturaPlayer.loadMedia({entryId: '1_q1aqr1af'})</script></div><iframe data-test="pigeonhole-iframe" title="pigeonhole-iframe" class="pigeonhole-qanda" src="https://pigeonhole.at/C6TY9H-1677186177669001vvYa/i/4409514?disablebackbutton"></iframe></div></div>
<div class="rf-video-player rf-kaltura-player"><script src="https://cdnapisec.kaltura.com/p/3200283/embedPlaykitJs/uiconf_id/47254103"></script><div id="djJ8MzIwMDI4M3zALh59e31Ad91DNE_aYIFPNlAKTgdQYec2MNkEw76zXvK83X94nQQp1xcMgvxplwfRgYpXIQLl4fl97rVf-iSrAkFK0zDHZJyudu_-uE4n9DUfQsO9bYsRSasL3_Ck2LzHH83v-sJVXRnCSBJ7UQ-S0RSBT-kG-Wv-zfnfVDHJOWyrDxqiraMnc1XrLbG_dBSavoIFHxbVM32lckwgpiallH0gREGBSH-IXkVq7JzDEezog-ANMh-wXQWGANq-3FwDrHZeNKptzMRwW0zMsNP4Y4i1zfyKt8ui-9B1Pdmh_mjRErjxLpGajCrSllFrFTg=" class="rf-player-inner"><div id="_68fid" class="kaltura-player-container" tabindex="-1"><div tabindex="0" aria-label="Video Player" class="playkit-player  playkit-Mac-OS playkit-Firefox playkit-hover playkit-metadata-loaded playkit-state-paused playkit-size-lg notranslate"><span></span><div id="_68fid-video" class="playkit-video-player" style="position: absolute; inset: 0px;"><div class="playkit-container" id="_k04f3" tabindex="-1"><video id="_proy4" class="playkit-engine playkit-engine-html5" playsinline="" src="blob:https://register.nvidia.com/d7eb5b47-8d5e-0149-8d28-0e959b6eb0ec"></video><div class="playkit-black-cover" style="visibility: hidden;"></div><div id="_epqca" tabindex="-1" class="playkit-poster" style="background-image: url(&quot;https://cfvod.kaltura.com/p/3200283/sp/320028300/thumbnail/entry_id/1_q1aqr1af/version/100011/height/488/width/868&quot;); display: none;"></div><div class="playkit-subtitles"><div style="position: absolute; inset: 0px; margin: 1.5%;"></div></div><div id="playkit-bumper-container_k04f3" class="playkit-bumper-container" style="visibility: hidden;"><video></video><div class="playkit-bumper-cover"></div><a class="playkit-bumper-click-through" target="_blank"></a></div></div></div><div><div class="playkit-player-gui" id="player-gui"><div style="position: absolute; inset: 0px;" class="playkit-overlay-action "></div><div style="position: absolute; inset: 0px;" class="playkit-video-area"><div style="pointer-events: auto;"><div aria-live="polite" tabindex="-1" class="offline-slate__slate-wrapper___pobqn "></div></div></div><div style="position: absolute; inset: 0px;" class="playkit-gui-area"><div style="pointer-events: auto;"><div class="overlay-portal" aria-live="polite"></div><div class="playkit-playback-controls playkit-center-playback-controls"><div class="playkit-control-button-container playkit-control-play-pause"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Play" class="playkit-control-button"><div><i class="playkit-icon playkit-icon-play"></i><i class="playkit-icon playkit-icon-pause"></i></div></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Play</span></div></div></div></div><div class="playkit-top-bar"><div class="playkit-top-bar-area"></div><div class="playkit-left-controls"></div><div class="playkit-right-controls"></div></div><div class="playkit-interactive-area"><div style="pointer-events: auto;"></div></div><div class="playkit-bottom-bar playkit-line-break"><div class="playkit-bottom-bar-area"><div tabindex="0" class="playkit-seek-bar" role="slider" aria-label="Seek slider" aria-valuemin="0" aria-valuemax="2376" aria-valuenow="404" aria-valuetext="06:43 of 39:36"><div class="playkit-progress-bar"><div class="playkit-frame-preview" style="left: 778.499px;"><div style="height: 96px; width: 168px;" class="playkit-frame-preview-img-container playkit-non-sticky"><div class="playkit-frame-preview-img" style="background: rgba(0, 0, 0, 0) url(&quot;https://cfvod.kaltura.com/p/3200283/sp/320028300/thumbnail/entry_id/1_q1aqr1af/version/100011/width/164/vid_slices/100&quot;) repeat scroll -15252px 0px;"></div></div></div><div class="playkit-time-preview" style="left: 778.499px;">36:52</div><div class="playkit-buffered" style="width: 0%;"></div><div class="playkit-progress" style="width: 16.9918%;"><a class="playkit-scrubber"></a></div><div class="playkit-virtual-progress" style="width: 93.1219%;"><div class="playkit-virtual-progress-indicator"></div></div></div></div></div><div class="playkit-left-controls"><div class="playkit-playback-controls "><div class="playkit-control-button-container playkit-control-play-pause"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Play" class="playkit-control-button"><div><i class="playkit-icon playkit-icon-play"></i><i class="playkit-icon playkit-icon-pause"></i></div></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-right playkit-hide">Play</span></div></div></div><div class="playkit-control-button-container playkit-control-rewind playkit-no-idle-control"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Seek backwards" class="playkit-control-button"><i class="playkit-icon playkit-icon-rewind-10"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Seek backwards</span></div></div><div class="playkit-control-button-container playkit-control-forward playkit-no-idle-control"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Seek forward" class="playkit-control-button"><i class="playkit-icon playkit-icon-forward-10"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Seek forward</span></div></div><div class="playkit-time-display"><span>06:43 / 39:36</span></div></div><div class="playkit-right-controls"><div class="playkit-control-button-container playkit-control-volume playkit-volume-control" role="application"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-live="polite" aria-label="100% volume. Click to mute" class="playkit-control-button"><i class="playkit-icon playkit-icon-volume-base"></i><i class="playkit-icon playkit-icon-volume-waves"></i><i class="playkit-icon playkit-icon-volume-mute"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-left playkit-hide">Mute</span></div><div class="playkit-volume-control-bar" role="slider" aria-valuemin="0" aria-valuemax="100" aria-valuenow="100" aria-valuetext="100% volume "><div class="playkit-bar"><div class="playkit-progress" style="height: 100%;"></div></div></div></div><div class="playkit-control-button-container playkit-control-language"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-haspopup="true" aria-label="Language" class="playkit-control-button"><i class="playkit-icon playkit-icon-language"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Language</span></div><div></div></div><div class="playkit-control-button-container playkit-control-settings"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Settings" class="playkit-control-button playkit-button-badge playkit-badge-icon playkit-icon-quality-hd-active "><i class="playkit-icon playkit-icon-settings"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Settings</span></div></div><div class="playkit-control-button-container playkit-control-fullscreen"><div class="playkit-tooltip"><button type="button" tabindex="0" aria-label="Fullscreen" class="playkit-control-button"><i class="playkit-icon playkit-icon-maximize"></i><i class="playkit-icon playkit-icon-minimize"></i></button><span style="max-width: 240px;" class="playkit-tooltip-label playkit-tooltip-top playkit-hide">Fullscreen</span></div></div></div></div></div></div></div><div style="width: 286.44px; right: -286.44px; opacity: 0;" class="playkit-side-panel playkit-vertical-side-panel"><div class="playkit-side-panel-content"></div></div><div style="width: 286.44px; left: -286.44px; opacity: 0;" class="playkit-side-panel playkit-vertical-side-panel"><div class="playkit-side-panel-content"></div></div><div style="height: 161.123px; top: -161.123px; opacity: 0;" class="playkit-side-panel playkit-horizontal-side-panel"><div class="playkit-side-panel-content"></div></div><div style="height: 161.123px; bottom: -161.123px; opacity: 0;" class="playkit-side-panel playkit-horizontal-side-panel"><div class="playkit-side-panel-content"></div></div></div></div></div><script type="text/javascript">var kalturaPlayer = KalturaPlayer.setup({
        targetId: 'djJ8MzIwMDI4M3zALh59e31Ad91DNE_aYIFPNlAKTgdQYec2MNkEw76zXvK83X94nQQp1xcMgvxplwfRgYpXIQLl4fl97rVf-iSrAkFK0zDHZJyudu_-uE4n9DUfQsO9bYsRSasL3_Ck2LzHH83v-sJVXRnCSBJ7UQ-S0RSBT-kG-Wv-zfnfVDHJOWyrDxqiraMnc1XrLbG_dBSavoIFHxbVM32lckwgpiallH0gREGBSH-IXkVq7JzDEezog-ANMh-wXQWGANq-3FwDrHZeNKptzMRwW0zMsNP4Y4i1zfyKt8ui-9B1Pdmh_mjRErjxLpGajCrSllFrFTg=',
        provider: {
          partnerId: '3200283',
          uiConfId: '47254103',
          ks: 'djJ8MzIwMDI4M3zALh59e31Ad91DNE_aYIFPNlAKTgdQYec2MNkEw76zXvK83X94nQQp1xcMgvxplwfRgYpXIQLl4fl97rVf-iSrAkFK0zDHZJyudu_-uE4n9DUfQsO9bYsRSasL3_Ck2LzHH83v-sJVXRnCSBJ7UQ-S0RSBT-kG-Wv-zfnfVDHJOWyrDxqiraMnc1XrLbG_dBSavoIFHxbVM32lckwgpiallH0gREGBSH-IXkVq7JzDEezog-ANMh-wXQWGANq-3FwDrHZeNKptzMRwW0zMsNP4Y4i1zfyKt8ui-9B1Pdmh_mjRErjxLpGajCrSllFrFTg='
        },
        playback: {
          preload: 'auto',
        },
        session: {
          userId: '1677186177669001vvYa'
        },
        ui: {
          debug: true
        },
        plugins: {
          undefined,
          'kaltura-live': {
            checkLiveWithKs: false,
            isLiveInterval: 10
          }
        }
      });
      kalturaPlayer.loadMedia({entryId: '1_q1aqr1af'})</script></div>
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/t9xd0hBC_v8?start=14" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---

<iframe data-test="pigeonhole-iframe" title="pigeonhole-iframe" class="pigeonhole-qanda" src="https://pigeonhole.at/C6TY9H-1677186177669001vvYa/i/4409514?disablebackbutton"></iframe>

---

<iframe width="560" height="315" src="https://cdnapisec.kaltura.com/p/3200283/embedPlaykitJs/uiconf_id/47254103" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---

---

% <iframe src="https://onedrive.live.com/embed?cid=63413B86A87DF2B1&resid=63413B86A87DF2B1%218219&authkey=AMRFU0zq7UaCW90" width="320" height="261" frameborder="0" scrolling="no" allowfullscreen></iframe>

---

Here we remove the height tag.

<div style ="display:block">
<iframe src="https://onedrive.live.com/embed?cid=63413B86A87DF2B1&resid=63413B86A87DF2B1%218219&authkey=AMRFU0zq7UaCW90" width="320"frameborder="0" scrolling="no" allowfullscreen></iframe>
</div>

---

Here we remove the height tag.

<div style ="display:block">
<iframe src="https://onedrive.live.com/embed?cid=63413B86A87DF2B1&resid=63413B86A87DF2B1%218219&authkey=AMRFU0zq7UaCW90" width="640" height="522" frameborder="0" scrolling="no" allowfullscreen></iframe>
</div>

---

:::{card} Skycaptain vs. Emulsion

<iframe width="280" height="145" src="https://www.youtube.com/embed/t9xd0hBC_v8?start=14" title="YouTube video player" frameborder="2" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
:::

---

```{admonition} Horizontal Rule post video embed
:class: warning

Be sure to add a Horizontal Rule after the '/div' for a video embed.

```

```{note} Video Sizing
:class: warning

From Onedrive, the video can be doubled in size and over written by the height and width parameters.

```   
---
#### Links

##### External Url.

    [alt-text](url address)
    [myst-parser](https://myst-parser.readthedocs.io/en/v0.17.1/syntax/optional.html#syntax-header-anchors)
    
We have installed myst-parser via documentation directions 
[myst-parser](https://myst-parser.readthedocs.io/en/v0.17.1/syntax/optional.html#syntax-header-anchors)

This allows us to use:

    [some header](header-label)
    

Clicking on the [link will take us to the Note Header](Note!)

 Another page [credit.rst](credit.rst) 
 
---
#### Table
 
:::{note}
This text is **standard** _Markdown_
:::

    :::{table} This is a **standard** _Markdown_ title
    :align: center
    :widths: grid
    
    abc | mnp | xyz
    --- | --- | ---
    123 | 456 | 789
    :::
    
   

:::{table} This is a **standard** _Markdown_ title
:align: center
:widths: grid

abc | mnp | xyz
--- | --- | ---
123 | 456 | 789
:::

---
#### Multiple Size Headings
These are examples of different size headings.

    h1: #, h2: ##, h3: ###, h4: ####, h5: #####, h6: ######

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6






