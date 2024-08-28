# Waterium.ColorTemplate

[![Waterium.ColorTemplate](https://img.shields.io/badge/Waterium.ColorTemplate-%40lWaterLite-blue)](https://github.com/lWaterLite) [![.Net](https://img.shields.io/badge/.NET-8.0-green)](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)

Waterium.ColorTemplate is a color and theme library for WPF desktop application.

## Install

- Install as the external library with `.dll` file.
  1. Open the [Latest release](https://github.com/lWaterLite/Waterium.Iconfont/release) and download the file end with `.dll.7z` . Unzip it at any directory you like.
  2. Open your own project, and add reference to the `.dll` file.
  3. References should be solved by your using IDE.


- Install as common ResourceDictionary with `.xaml` file.
  1. Open the [Latest release](https://github.com/lWaterLite/Waterium.Iconfont/release) and download the file end with `.xaml.7z`. Unzip it at any directory you like.
  2. In your using IDE, chose `add existing item` to your project.
  3. File index should be solved by your using IDE.

> [!TIP]
>
> What's the difference?
>
> - `.dll` file is easy for distribution.
> - `.xaml` file can provide with better IDE autocomplete.
>
> If you don't know what to use, just use `.xaml` as any other ResourceDictionary file that be used in your own project.



## Usage

In your `App.xaml` file, add a resource as following

```xaml
<Application.Resource>
    <ResourceDictionary>
        <ResourceDictionary.MergeDictionaries>
            <ResourceDictionary Source="<DictionayLocation>" />
        </ResourceDictionary.MergeDictionaries>
    </ResourceDictionary>
</Application.Resource>
```

Notice that `<DictionayLocation>` in the `Source` should be replaced by the correct ResourceDictionary Uri you are using.

- As `.dll` reference, replace it by `/Waterium.ColorTemplate;component/BasicTheme.xaml`. `BasicTheme.xaml` can be replaced by other dictionary you want to use.
- As `.xaml`, replace it by the relative path of the file. It can looks like `/Themes/BasicTheme.xaml`.

Then in your window, you can use it as `StaticResource`. e.g.

```xaml
<TextBlock Text="Waterium" FontSize="64" Foreground="{StaticResource Main-100}" />
```

## Resource

The available resource dictionaries are as following:

- BasicTheme.xaml
- GradiantPanel.xaml

## License

[MIT](LICENSE) @ 2024 lWaterLite