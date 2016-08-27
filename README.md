# In-game Debug Console for Unity 3D

![screenshot](https://yasirkula.files.wordpress.com/2016/08/consolepreview.png)

**Forum Thread:** http://forum.unity3d.com/threads/in-game-debug-console-with-ugui-free.411323/

### A. ABOUT

This asset is a means to see debug messages (logs, warnings, errors, exceptions) in-game in a build (also assertions in editor). It also has a built-in console that allows you to enter commands and execute pre-defined functions in-game. It is super easy to configure a new command; the only restriction is that the parameter types should match one of the supported types: int, float, bool, string, Vector2, Vector3 and Vector4. See *README.pdf* for more information and example code snippets...

User interface is created with **uGUI** and costs 1 SetPass call (and 6 to 10 batches). It is possible to drag, resize and hide the console window during the game. Once the console is hidden, a small popup will take its place (which is also draggable).

![popup](https://yasirkula.files.wordpress.com/2016/06/ingamedebugconsolepopuppng.png)

Console window is optimized using a customized recycled list view that calls Instantiate and Destroy functions sparingly. 

### B. HOW TO

Simply drag & drop **DebugLogCanvas** prefab to the first scene of the game. If you don't need the console on every scene, you can deselect the *Singleton* property of the canvas so that it will be destroyed when scene changes.

### C. NOTES

- If **2D Rect Mask** component does not exist in your version of Unity (*pre 5.2*), replace it with **Mask** component (search for *Viewport* objects). Then change the color alpha value of the attached **Image** components to 1. Unfortunately, DebugLogCanvas will now cost more draw calls.

### D. LIMITATIONS

- This asset uses **2D Rect Mask** and thus the DebugLogCanvas can not be rendered in World Space but **only in Screen Space**.

### E. EXTRAS

- Looking for a more flat and modern style? Check out this amazing retouch by EnricoMonese: https://github.com/EnricoMonese/UnityIngameDebugConsole

<img src="https://cloud.githubusercontent.com/assets/19847464/18023979/ebcc5f02-6c00-11e6-9b14-d369e524cb45.png" height=389>
