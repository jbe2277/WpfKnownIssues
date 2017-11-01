# WPF ResourceDictionary.MergedDictionaries resolve issue

This sample shows that WPF is not able to resolve resources that are defined in another ResourceDictionary that was merged before the one that needs one of its resources.
   
App.xaml
- ModuleResources.xaml
-- BrushResources.xaml
-- ButtonResources.xaml
  
ButtonResources requires BrushResources. The WPF Designer of Visual Studio works correct and finds the Resources but at runtime a XamlParseException is thrown.
  
## Workarounds

**1. Register all ResourceDictionaries at Application level**

If the ResourceDictionaries are merged directly into the Application ResourceDictionary then WPF is able to resolve the dependencies right.

App.xaml
- BrushResources.xaml
- ButtonResources.xaml

**2. Use DynamicResource instead of StaticResource**

This would work as well. But consider the performance impact of using DynamicResource.