---
{"dg-publish":true,"permalink":"/precursor/running-haskell/"}
---


To run it, you do:

```powershell
ghci
```

This should open up a terminal that looks somewhat like:

```ghci
gchi> 
```

That's really all there is to running it in the terminal! Treat this like a scratchpad. Note the keyword `it`, which will remember the most recent output done within the `ghci` terminal, similar to `Ans` on a normal keyboard. To exit do `ctrl+D`.

To actually do anything interesting with it, we have to write programs, which look like `*.hs`. For the standard [[hello.h[fp_notes.pdf](https://drive.google.com/file/d/1O1Oq5g9DEug96MbidHu_iYOwaDCYYNa2/view?usp=sharing)], do:

```haskell
main = do

  putStrLn "Hello, everybody!"

  putStrLn ("Please look at my favorite odd numbers: " ++ show (filter odd [10..20]))
```

This goes ahead and tells you what a file should look like. You have a main function which is defined as the process of doing some prints. For some conventions, see [[convention[fp_notes.pdf](https://drive.google.com/file/d/1O1Oq5g9DEug96MbidHu_iYOwaDCYYNa2/view?usp=sharing)].

To run it (for some reason it doesn't run in vscode), open up your terminal, and do

```powershell
ghc hello.hs
```

This will generate 3 files, `hello.o`, `hello.hi`, `hello.exe`. However, the computer seems to think `hello.exe` is a virus, so instead do

```powershell
runghc hello.hs
```

You should get:

```text
Hello, everybody!
Please look at my favorite odd numbers: [11,13,15,17,19]
```

and now we know how to run programs!

If you want to use it within a scratchpad, do `ghci hello.hs`, and it will load in all relevant variables/functions into the scratchpad.
