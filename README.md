# Example of Single Directory Component

This folder represents an example of Single Directory Components (SDC) provided for educational purposes now that SDC is in Drupal Core (since D10).

The folder added to a theme folder and was tested as working sucessfully with defined custom Paragraphs. 

The end result is a phone screen that can show custom messages dynamically as either a part of rendered content or as a custom block thanks to leveraging the Paragraphs, sdc_display, paragraphs_viewmode, and nomarkup modules.

N.B. The CSS was taken from this public example: https://codepen.io/azoschke/pen/wvdbLLj

## Previewing Components in Storybook

You can also preview the components using  [Storybook](https://storybook.js.org/). To be able to do so, you will have to install an additional module ([CL Server](https://www.drupal.org/project/cl_server)) and other third-party tools using a JS package manager, such as npm or yarn.

For detailed, step-by-step instructions, visit the [documentation page for CL Server](https://git.drupalcode.org/project/cl_server/-/tree/2.x).

> Storybook v7.x
>
> According to the documentation, starting with Storybook v7.x the default value (defaultValue) has been [deprecated](https://storybook.js.org/docs/react/api/arg-types#defaultvalue). To declare the default values for arguments use the args object instead.

**Additional Considerations:**

Each component in this collection comes with a pair of Storybook config files in JSON and YAML format. It is up to you which format to use. The maintainers wanted to give you the freedom to choose your preferred format. However, ensure you select only one format when you provide the configuration in the ".storybook/main.js" file.

Review and adjust the values of the "stories" property accordingly. For example, instead of
``` js
stories : [
    "../web/themes/**/*.stories.@(json|yml)"
  ],
```
use
``` js
stories : [
    "../web/themes/**/*.stories.yml"
   ],
```

Otherwise, you may end up with a warning or an error stating that your components contain duplicate story declarations with the same name.

___

**Disclaimer**: Please be advised the code provided here may not be production-ready and is intended for educational purposes only. Use it at your discretion.


