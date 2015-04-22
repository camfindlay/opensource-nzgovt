# 7. The process of sharing code
## 7.1 The addons ecosystem
One thing that can be confusing when first getting into working with SilverStripe CMS addons (including modules and themes) is the set of open source tools, social coding platforms and code package packages used in conjunction with addon code. Once you learn the basic flow through the ecosystem of tools, they are quite logical and easy to use. An addon in SilverStripe CMS is defined as anything that extends the functionality of the SilverStripe CMS core. That could be a package of code we refer to as a 'module' or a set of 'theme' templates and supporting images, css and javascript. Addons is the all inclusive term for both modules and themes for SilverStripe CMS.

## 7.2 Finding addons
Once a default installation of SilverStripe CMS is installed to start a project, it is likely that additional functionality will be required to complete the project. It is important to first ensure an environment scan of available addons is made to find any already shared and  reusable code. If none is found meeting the requirements this will give a good case to extend an existing module or building a new one. The scanning for reusable code is an important step to complete otherwise duplication of effort and costs may occur. With this in mind, many SilverStripe CMS developers that share code do so in particular locations that can be easily searched. Firstly, the SilverStripe CMS addons catalogue should be searched. This contains a listing of all registered modules including a description of the modules functionality, screenshot, authors, available versions and other useful information. These can then be installed using the composer code management tool to trial suitability. The catalogue is itself created with shared open source code and is open to improvements from the community to make finding code even easier.

![addons screenshot](/assets/images/image_0.png)

There are two further catalogue locations that should be considered in an environment scan for reusable code. Firstly, Packagist.org - this is the catalogue of all PHP code packages that can be managed using the composer code management tool. It includes a wider pool of shared PHP code libraries than SilverStripe CMS specific addons. Some of these PHP packages can be used on the CWP as long as they use supported PHP extensions on the CWP. This includes packages such as API wrappers and other utility code classes. Any SilverStripe CMS code found here will also be automatically added on the addons catalogue as Packagist.org is used as the source of data. 

![packagist screenshot](/assets/images/image_1.png)

Next, searches should consider social coding platforms such as GitHub directly. Although it must be noted that as SilverStripe CMS code will exist in these spaces alongside thousands of other unrelated projects. It is also likely to come across "forks" of modules which as mentioned are copies taken by other developers from an original source repository of code. In this case tracing back to the original repository should occur rather than using the fork of the code if possible.

![GitHub screenshot](/assets/images/image_2.png)

Lastly, discussing functionality needs with other community members via digital communication channels or at in person meetups could help to get recommendations for useful code. If after a reasonable environment scan is carried out suitable reusable code is not available then the options are:

1. Fork the module that is similar in features to those required and contribute improvements to that module so it does do what is required.

2. Develop a new module to the requirements and share this through open source licenses. 

## 7.3 Contributing to existing code: Forking and pull requests

The following is a high level walkthrough the process of forking, improving and raising a pull request with a module maintainer in order to contribute to existing shared code.

1. Find a module on the SilverStripe addons catalogue that contains most of the functionality required and would need additional work to add a new feature and fit the project needs exactly.

2. Trace the module back to it's publically accessible source code, this is usually on GitHub. 

3. Raise a GitHub issue outlining the feature you intend to work on. A back and forth dialogue may occur to work out the details of the new feature. Once there is some agreement work can begin. 

4. Using the 'fork' feature of GitHub take a copy of the code repository.

5. Checkout this copy of the code locally using git into the project (rather than installing it via Composer). You should also begin a git branch relating to your new feature.

6. Edit the module code locally, building (and writing tests for) the new features required. Commit in the work as logical units of work are completed.

7. Once work is complete, push the branch of code to the 'fork'. 

8. Raise a 'pull request', a proposal of code changes which makes a public request to the maintainer of the original module to pull changes from the fork. 

9. There may be further online discussion while the code is peer reviewed. If improvements are suggested these will need to be made locally and your fork updated, the pull request will automatically update with the changes.

10. Once reviewed, the maintainer will accept the pull request to merge the forked code and the new feature will now be available in the module, ready for a release and to be installed using Composer as is the standard for managing new modules in projects.

![fork and contribution diagram](image_3.png)

## 7.4 Packaging and submitting new shared modules
The next walkthrough outlines the process that an agency sharing new module code might take to make it discoverable by others and able to be installed via the Composer.

1. Modules are created as subfolders in the SilverStripe CMS project. They are named using lower case letters and hyphens (the naming convention in use in the community for module). For example: '*silverstripe-blog*'. 

2. There is a set folder structure for the module code which should be followed, this is [documented in the official SilverStripe CMS documentation](http://doc.silverstripe.org/en/developer_guides/extending/modules).

3. A readme document should be written and included in the module folder. This includes information about the features, installation and configuration of the module and likely the text of the FOSS license it has been released under. This readme file is also displayed on the addons module catalogue to help other discover modules for use in their projects.

4. A composer code manager meta data file should also be included in the module directory and should include meta data describing the module for the addons catalogue to later make searchable. A [full example of a composer.json](http://docs.silverstripe.org/en/developer_guides/extending/how_tos/publish_a_module/) file can be seen in the official SilverStripe CMS documentation. For modules created specifically for CWP the tag 'cwp' can be included in the keyword metadata to help other CWP users find specific modules.

5. Next the code must be moved to an online and public code repository. For openly shared public code, GitHub is recommended though any publically available git repository will work. This includes module code on the CWP GitLab as long as the code repository has been marked as public.

6. It is also good practice to tag your module using semantic versioning, if this is the first release of a new module you will likely tag it as the 0.1.0 version until it is deemed more stable.

7. In order for modules to be installed via Composer, it needs to be submitted to Packagist.org. This is the directory of software that is able to be used via the Composer package management tool. Sign up for an account and follow the instructions to complete the registration of your module.

8. The module can now be referenced in a project's composer metadata file and installed like any other SilverStripe CMS module.

9. Lastly, the module will now automatically appear on the [SilverStripe CMS addons catalogue](http://addons.silverstripe.org)  for other users to discover and reuse. If the process has been correctly followed then in the addons catalogue:

    * The module is listed and can be found under the 'cwp' tag.

    * A list of available versions will show when drilled down into the module listing (based on your release version tags from your git repository).

    * The readme file content displays and provides details about the module's features and how to install it in a project via Composer.

    * The module can be installed by copying the Composer quick command listed with the module.

10. As further work is completed on the shared module code and new versions are released the data held in the addons catalogue will automatically update provided the documentation in the readme file, new release tags and the composer metadata files are updated.

![govt.nz GitHub account screenshot](/assets/images/image_4.png)
