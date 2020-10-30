# VKYD Main Webapp
> Wick3d ( _/ˈwɪkɪd/_ )

**🌐 VKYD's main webapp built on Svelte.JS and Snipcart**

![DUB](https://img.shields.io/dub/l/vibe-d?label=License)

Check out this badboy at **[vkyd.in](https://vkyd.in)**.

## Vote of thanks and resources used
- [Neuphormism Design Maker](https://neumorphism.io/#1D2022)

### License
Licensed under the MIT License.

### Note to self and to-do
- Implement close if clicked outside on sidenav

- Icons needed - 
    1. Cross
    2. Mail
    3. Share
    4. Hyperlink chain of some sort
    5. Shopping cart or bag
    - Add these to `cdn/icons/website` and the mail icon to `cdn/icons/social-media`

- SEO and meta for better Lighthouse performance
    1. Add `meta description`, `title` and `keywords`
    5. Add `aria-label` and `placeholder` attribute to all links to make them more discernible
    6. Use lazy loading with https://github.com/leafOfTree/svelte-lazy
    7. Add `sitemap.xml`