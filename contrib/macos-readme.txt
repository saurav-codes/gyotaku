gyotaku for macOS (Apple Silicon)
=================================

Search every screenshot you have taken by the text inside it.

Getting started
---------------

The easiest way is the one-line install in a terminal, which downloads the
release, checks it and puts the programs in ~/.local/bin:

    curl -fsSL https://raw.githubusercontent.com/xevrion/gyotaku/main/install.sh | sh

By hand, keep the files together in one folder you won't delete:

    gyotaku-app                 the search window
    gyotaku                     the background reader and command line
    libonnxruntime.1.28.2.dylib Microsoft's ONNX Runtime, used to read text

Run gyotaku-app. The first time, it asks which folders to read (the Desktop
is where macOS saves screenshots taken with Cmd+Shift+3) and whether to
keep reading new ones in the background. Saying yes installs a launchd
agent that starts the reader when you sign in; the toggle is in the
settings (Ctrl+,).

Press Alt+Shift+S anywhere to open the search window. The app registers
this key itself, and pressing it again closes the window.

The first run downloads the OCR models once (about 22 MB). After that
everything happens on this computer, nothing is uploaded.

Deleting a screenshot from gyotaku moves it to the Finder trash, so Put
Back works.

To remove it: turn off background reading in settings, quit, and delete the
programs. The index and settings live in
~/Library/Application Support/gyotaku, the thumbnails in
~/Library/Caches/gyotaku.

Problems and ideas: https://github.com/xevrion/gyotaku/issues
