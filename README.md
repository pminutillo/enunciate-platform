enunciate-platform
==================
       *NOTE* Requires git to be available on command line path

        tldr: Run enunciate-platform meta-target to generate REST api docs for platform

        Enunciate is designed to work on a single project. It does support multiple
        modules in that project, but those modules need to be dependencies of
        the parent project you are running enunciate against. In this case, we will
        be running enunciate against extensions as the parent. Then we will add a jar
        from data-access to extensions' lib folder. We will point enunciate at the
        extensions src directory, but also make data-access' src available on the
        classpath.

        Steps:
            * Pull down source for each project concerned
            * Resolve and build each project
            * Copy generated artifacts to the lib of the "parent" (extensions)
            * Add projects' src to classpath for enunciate
            * Run enunciate target
