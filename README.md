# weissdigital.xamarin.addins.mvxcontentpage
Creates a Forms MVVMCross MvxContentPage with a CodeBehind class that extends MvxViewModel.

![Add File Dialog](screenshot.png)

### The files that are created are as follows:

##### Xaml File:
```xml
<?xml version="1.0" encoding="utf-8"?>
<Mvx:MvxContentPage 
    x:TypeArguments="ViewModels:PageViewModel" 
    xmlns="http://xamarin.com/schemas/2014/forms" 
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" 
    xmlns:Mvx="clr-namespace:MvvmCross.Forms.Views;assembly=MvvmCross.Forms" 
    xmlns:ViewModels="clr-namespace:MyFormsApp.ViewModels;assembly=MyFormsApp" 
    x:Class="MyFormsApp.PageView">
</Mvx:MvxContentPage>
```

##### Xaml Code Behind File:
```C#
using MvvmCross.Forms.Views;
using MyFormsApp.ViewModels;

namespace MyFormsApp
{
    public partial class PageView : MvxContentPage<PageViewModel>
    {
        public PageView()
        {
            InitializeComponent();
        }
    }
}
```

##### ViewModel File:
```C#
using MvvmCross.ViewModels;

namespace TipCalc.ViewModels
{
    public partial class PageViewModel : MvxViewModel
    {
        public PageViewModel()
        {
        }
    }
}
```

### Notes

Nuget Packages Required in your Core Project:

- [Xamarin.Forms](https://www.nuget.org/packages/Xamarin.Forms)
- [MvvmCross](https://www.nuget.org/packages/MvvmCross)
- [MvvmCross.Forms](https://www.nuget.org/packages/MvvmCross.Forms)
- 
