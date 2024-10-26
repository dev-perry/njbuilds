# Tutorial Reflection

The following are some thoughts and ideas that occurred to me as I was following the Catala tutorial and worked my way through the first line of the building code.

- Why are there different file extensions for different languages? I understand the need to support multilingual syntax given legislation comes in many languages. Would having a project-level configuration file in which a developer can set the language they are using provide a cleaner DX?
- Are enumeration values that don’t have a “content” atttribute null by default? Or is there something special about prefixing the name of an enum's value with “No-“?
- Cool that Catala automatically handles rounding for money operations!
- I like how when I have a question about something usually the next section in the tutorial answers it 😂.
- When two conflicting exceptions to a given rule yield the same result is a warning raised?
- There seems to be missing example code for declaring a module in Annex B
- I had to look at the catala-examples Github repository to properly understand how to setup my directory for modules to work.
- In the English tutorial the TaxCredit enumeration is declared and then never used. I assumed that accessing values was done by dot notation and got confirmation by checking code in the catala-examples/NSW_community_gaming repository. Maybe there could be in an “Enumerations” section in the Catala Types section of the English tutorial.
- The Syntax Cheatsheet is a wonderful resource!
- The way the master file works once again makes me think there could be a role for a project-level configuration file where a developer can set what language they are going to use, thereby making different file extensions unnecessary. In my opinion, there is something a bit cleaner about having a `project.catala` file rather than `project.catala_en` or `project.catala_fr`.
- Nitpick: Typo in the following error: `Unused varible: uniform_units does not contribute to computing any of scope…Did you forget something?”` I only noticed it because I saw triggered it so many times 🙃.
- So is the `[RESULT]` keyword in testing primarily for correlating tests with test outputs when using the CLI?
- Do any of the list operations besides folding provide access to the current index of an element?
- There’s this ninja error I don't quite understand whenever I run `clerk test`:
    ```bash
    [9/9] <test> 'njbuilds@test'
    FAILED: njbuilds@test
    out='njbuilds@test' ; success=$( tr -cd 0 < '_build/njbuilds@test' | wc -c ) ; total=$( wc -c < '_build/njbuilds@test' ) ; pass=$( ) ; if test "$success" -eq "$total" ; then printf "\n[\033[32mPASS\033[m] \033[1m%s\033[m: \033[32m%3d\033[m/\033[32m%d\033[m\n" ${out%@test} $success $total ; else printf "\n[\033[31mFAIL\033[m] \033[1m%s\033[m: \033[31m%3d\033[m/\033[32m%d\033[m\n" ${out%@test} $success $total ; return 1 ; fi

    [FAIL] njbuilds:   0/5
    /bin/sh: line 0: return: can only `return' from a function or sourced script
    ninja: build stopped: cannot make progress due to previous errors.
    ```