# WPF Ribbon Window: Visual issues

The WPF Ribbon implementation comes with various visual issues:
 
- The window content (client area) is cropped when the window is in Maximized mode.
- The window border is too thin.
  - Windows 10: The border is thin at top and bottom but thick at left and right.
- QuickAccessToolbar does not have enough “margin” to the top.
- The window title is blurry and does not have enough “margin” to the top.
- The application icon is not centered.

## Links

- [Reported at Microsoft Connect](https://connect.microsoft.com/VisualStudio/feedback/details/775972/wpf-ribbon-window-the-border-is-too-thin)
- [WPF Blog that mentions this bug (2014)](http://blogs.msdn.com/b/dotnet/archive/2014/11/12/the-roadmap-for-wpf.aspx)
