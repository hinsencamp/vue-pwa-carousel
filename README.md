# vue-pwa-carousel
A tutorial about how to build a carousel component in VueJS. It's used to shows the benefits of using a Service Worker. 

### Add ```vue-config.js``` to root folder 

```module.exports = {
  publicPath: process.env.NODE_ENV === "production" ? "/vue-pwa-carousel/" : "/"
};
```
### Modify ```.gitignore```

Out comment ``` #/dist/```

### Build and Modify

```yarn build```

Go to ```dist``` folder, select all ```/dist``` and remove the ```/```

### Commit & deploy! 

```git add dist```

```git commit -m "new dist"```

```git subtree push --prefix dist origin gh-pages```
