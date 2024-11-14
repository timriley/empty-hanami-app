# Empty Hanami app for Richard

```
pack build empty-hanami-app --path .
docker run -it --rm --env PORT=9292 --env DATABASE_URL=sqlite://db/site.sqlite -p 9292:9292 empty-hanami-app
docker run -it --rm --env PORT=9292 --env DATABASE_URL=sqlite://db/site.sqlite -p 9292:9292 --entrypoint /cnb/lifecycle/launcher empty-hanami-app bash
```

See [this gist](https://gist.github.com/timriley/97fb57fc9ace630ed15cdffb89bfb519) for the error we had when building.

I also need to fix Hanami’s `rake assets:precompile` so that it returns a non-zero exit code for a legitimate failure of the asset compilation.
