# Uno Toolkit Controls
The `Uno.Toolkit.UI` library adds the following controls:
- `AutoLayout`: A custom panel used by the [Figma plugin](https://platform.uno/unofigma/) to bridge the gap between Figma and UWP layout implementation.
- [`Card` and `CardContentControl`](controls\CardAndCardContentControl.md): \[Material control\] Cards contain content and actions that relate information about a subject.
- [`Chip` and `ChipGroup`](controls\ChipAndChipGroup.md): \[Material control\] Chips are compact elements that represent an input, attribute, or action.
- `Divider`: \[Material control\] A divider is a thin line that groups content in lists and layouts.
- [`DrawerControl`](controls\DrawerControl.md): A container to display additional content, in a hidden pane that can be revealed using a swipe gesture, like a drawer.
- [`TabBar` and `TabBarItem`](controls\TabBarAndTabBarItem.md): A list of selectable items that can be used to facilitate lateral navigation within an application.
- [`NavigationBar`](controls\NavigationBar.md): A custom control that helps implement navigation logic for your application.  

## Helpers
The `Uno.Toolkit.UI` library adds the following helper classes:
- `SystemThemeHelper`: Provides a set of helper methods to check the current operating system theme, and manipulate the application dark/light theme.

## Control Styles
Control|Style Key|Implicit Style*|
-|-|-
AppBarButton|MainCommandStyle|implicit
AppBarButton|ModalMainCommandStyle|
utu:Chip|AssistChipStyle|
utu:Chip|ElevatedAssistChipStyle|
utu:Chip|InputChipStyle|
utu:Chip|FilterChipStyle|
utu:Chip|ElevatedFilterChipStyle|
utu:Chip|SuggestionChipStyle|
utu:Chip|ElevatedSuggestionChipStyle|
utu:ChipGroup|InputChipGroupStyle|
utu:ChipGroup|ElevatedSuggestionChipGroupStyle|
utu:ChipGroup|SuggestionChipGroupStyle|
utu:ChipGroup|ElevatedFilterChipGroupStyle|
utu:ChipGroup|FilterChipGroupStyle|
utu:ChipGroup|ElevatedAssistChipGroupStyle|
utu:ChipGroup|AssistChipGroupStyle|
utu:Divider|DividerStyle|implicit
utu:NavigationBar|NavigationBarStyle|implicit
utu:NavigationBar|ModalNavigationBarStyle|
utu:TabBar|TopTabBarStyle|
utu:TabBar|ColoredTopTabBarStyle|

Implicit Style*: Styles marked with `implicit` can be made into the default implicit styles by setting the `WithImplicitStyles` flag to `True`:
```xml
<MaterialToolkitResources xmlns="using:Uno.Toolkit.UI.Material" WithImplicitStyles="True" />
```