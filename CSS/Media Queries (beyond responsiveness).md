Media queries are a feature in CSS that allow developers to apply different styles to a webpage based on various characteristics of the user's device or environment. While media queries are commonly used for creating responsive designs that adapt to different screen sizes and orientations, they can also be used for other purposes beyond screen responsiveness. Here are some alternative uses for media queries:

1. **Print Styles**: Media queries can be used to define styles specifically for printed documents. By using `@media print`, developers can specify how the content should be formatted and styled when it is printed. This includes hiding non-essential elements, adjusting layout, and optimizing typography for print.
    
```css
@media print {
  /* Print-specific styles */
  body {
    font-size: 12pt;
    line-height: 1.5;
  }
  .hide-on-print {
    display: none;
  }
}
```
    
2. **Dark Mode**: With the increasing popularity of dark mode interfaces, media queries can be used to detect if the user's device has dark mode enabled and adjust the styles accordingly. By using `@media (prefers-color-scheme: dark)`, developers can apply dark mode styles to their web pages for users who prefer it.
    
```css
@media (prefers-color-scheme: dark) {
  /* Dark mode styles */
  body {
    background-color: #333;
    color: #fff;
  }
}
```
    
3. **High Contrast Mode**: Some users may rely on high contrast mode to improve readability or accessibility. Media queries can be used to detect if the user's device has high contrast mode enabled and adjust the styles accordingly.
    
```css
@media screen and (-ms-high-contrast: active), (-ms-high-contrast: none) {
  /* High contrast mode styles */
  body {
    background-color: #fff;
    color: #000;
  }
}
```
    
4. **Viewport and Device Information**: Media queries can access various viewport and device information, such as width, height, aspect ratio, resolution, and orientation. This information can be used to create device-specific layouts or adjust styles based on the device's capabilities.
    
```css
@media (min-width: 1024px) {
  /* Styles for devices with a minimum width of 1024px */
  /* For example, desktop or tablet landscape */
}
```
    
5. **Accessibility Enhancements**: Media queries can be used to enhance accessibility by adjusting styles based on user preferences or needs. For example, developers can use media queries to increase font sizes, adjust contrast ratios, or provide alternative navigation options for users with disabilities.
    
```css
@media (prefers-reduced-motion: reduce) {
  /* Reduce motion styles */
  .animated-element {
    animation: none !important;
  }
}
```
    

Overall, media queries are a powerful feature in CSS that enable developers to create flexible and adaptive web designs that cater to a wide range of devices, user preferences, and environmental conditions. They can be used not only for screen responsiveness but also for enhancing print styles, supporting dark mode, accommodating high contrast mode, accessing device information, and improving accessibility.