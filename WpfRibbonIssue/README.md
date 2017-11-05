# WPF Ribbon Window: Visual issues

This sample shows that the WPF Ribbon implementation comes with various visual issues:
 
- The window content (client area) is cropped when the window is in Maximized mode.
- The window border is too thin.
  - Windows 10: The border is thin at top and bottom but thick at left and right.
- QuickAccessToolbar does not have enough “margin” to the top.
- The window title is blurry and does not have enough “margin” to the top.
- The application icon is not centered.

**Screenshot on Windows 7:**
![WPF Ribbon Window visual issue on Windows 7](https://github.com/jbe2277/WpfKnownIssues/raw/master/WpfRibbonIssue/ScreenshotWindows7.png "WPF Ribbon Window visual issue on Windows 7")

## Workarounds

**1. Inherit from Window class instead of RibbonWindow**

> Note: The sample application [Waf Writer](https://github.com/jbe2277/waf/tree/master/src/System.Waf/Samples/Writer) shows the techniques described here.

The WPF Ribbon can be used without using the RibbonWindow class. The Window class does not have these visual issues. But this comes with some limitations:
* The QuickAccessToolBar is not supported.
* Contextual Ribbon Tabs cannot be used.

**2. Use another 3rd party WPF Ribbon implementation**

Another 3rd party WPF Ribbon implementation might not have these visual issues.

## Links

- [Reported at Microsoft Connect](https://connect.microsoft.com/VisualStudio/feedback/details/775972/wpf-ribbon-window-the-border-is-too-thin)
- [WPF Blog that mentions this bug (2014)](http://blogs.msdn.com/b/dotnet/archive/2014/11/12/the-roadmap-for-wpf.aspx)
