# ControlExtensions Attached Properties
Provides various attached properties for common controls.

## Properties
Property|Type|Description
-|-|-
Command|ICommand|Sets the command to execute for: <br>- `TextBox`/`PasswordBox` enter key press\*<br>- `ListView` item click\*<br>- `NavigationView` item click
CommandParameter|ICommand|Sets the parameter to pass to the Command property.

Command on `TextBox`/`PasswordBox`\*: Having this set will also cause the keyboard dismiss on enter.
Command on `ListView`\*: [`IsItemClickEnabled`](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.controls.listviewbase.isitemclickenabled) must also be set to true for this to work.

### Remarks
- For Command, the relevant parameter is also provided for the `CanExecute` and `Execute` call:
  > Unless CommandParameter is set, which replaces the following.
  - `TextBox.Text`
  - `PasswordBox.Password`
  - `ItemClickEventArgs.ClickedItem` from `ListView.ItemClick`
  - `NavigationViewItemInvokedEventArgs.InvokedItem` from `NavigationView.ItemInvoked`

## Usage
```xml
<!-- Execute command on enter -->
<PasswordBox utu:ControlExtensions.Command="{Binding Login}" />

<!-- ListView item click-->
<ListView ItemsSource="123"
		  IsItemClickEnabled="True"
		  utu:ControlExtensions.Command="{Binding UpdateSelection}" />

<!-- NavigationView item invoke -->
<NavigationView utu:ControlExtensions.Command="{Binding Navigate}">
	<NavigationView.MenuItems>
		<NavigationViewItem Content="Apple" />
		<NavigationViewItem Content="Banana" />
		<NavigationViewItem Content="Cactus" />
	</NavigationView.MenuItems>
</NavigationView>
```
