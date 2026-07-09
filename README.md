# How to Compare SfMaskedEntry vs Entry Control in .NET MAUI

Both `SfMaskedEntry` and `Entry` controls can be used to collect user input in .NET MAUI applications. However, each control is designed for different input scenarios.

* `Entry` is suitable for general-purpose text input without any predefined formatting requirements.
* `SfMaskedEntry` is designed for structured data entry and supports input masking to ensure users enter data in a specific format.

Choosing the appropriate control depends on your application's input requirements and validation needs.

### Benefits of Using SfMaskedEntry

* Enforces predefined input formats.
* Reduces invalid user input.
* Improves data consistency and accuracy.
* Provides built-in masking and validation.
* Enhances the user experience for structured data entry.

## Example Scenario

Consider a form that requires users to enter a phone number.

**MainPage.xaml**
```
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:editors="clr-namespace:Syncfusion.Maui.Inputs;assembly=Syncfusion.Maui.Inputs"
             x:Class="MaskedEntrySample.MainPage">
    <VerticalStackLayout WidthRequest="350" Spacing="30" Padding="30">
        <!-- Standard Entry -->
        <Entry Placeholder="Enter phone number"  ClearButtonVisibility="WhileEditing"/>
        <!-- SfMaskedEntry -->
        <editors:SfMaskedEntry ClearButtonVisibility="WhileEditing"
                        MaskType="Simple"
                        Mask="(000) 000-0000"
                        Placeholder="Enter phone number"/>
    </VerticalStackLayout>
</ContentPage>
```

