# single-file-application

This is an example application which is made up of a single file, `hello.php`. 
It prints `phpinfo()` to show some data.

# Usage

Build and push to use it:

```sh
$ docker build . -t nickcharlton/php-k8s-single-file:1.0.0
$ docker push nickcharlton/php-k8s-single-file:1.0.0
```
