# Localizable.strings

This repo was created to demo to SourceTree that their tool ignores the textconv setting in git when diffing commits.

See issue 4210: [diff textconv is ignored when diffing commits](https://jira.atlassian.com/browse/SRCTREE-4210)

# Setup

To setup your git environment, run the following 2 commands:

    git config diff.localizablestrings.textconv "iconv -f utf-16 -t utf-8"
    git config diff.localizablestrings.binary false
    
# Demo
    
Now if you type:

    git show c64354
    
You should be able to see Localizable.strings changes

    commit c64354f1d4945ed4325443923f937450dc45510a
    Date:   Tue Nov 22 14:43:22 2016 -0800

        Update Localizable.strings with Spanish translation

    diff --git a/Localizable.strings b/Localizable.strings
    index dabed4a..5c7a718 100644
    --- a/Localizable.strings
    +++ b/Localizable.strings
    @@ -1 +1 @@
    -"Hello World" = "Hello World"
    +"Hello World" = "Hola Mundo"
