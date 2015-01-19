MopaComposerBridge
==================

This Bridge allows usage of Composer classes through the composer.phar available on a lot of systems recently.
I was originally designed for providing a way to hook into the composeres knowledge about things installed in a project, but can be used for a lot of other composer related tasks too.


You can either let the Bridge find your composer / composer.phar installation, or install composer in your project.

You could get a composer like this:
```
// with 
// Symfony\Component\Console\Input\InputInterface $input
// Symfony\Component\Console\Output\OutputInterface $output

if(false !== $composer = ComposerAdapter::getComposer($input, $output)) {
    // $composer is now a fully setup instance of composer
}
```

Mac users using the composer homebrew version, might have to install composer.phar in the project directory to be able to e.g. use the symlink command in https://github.com/phiamo/MopaBootstrapBundle/
