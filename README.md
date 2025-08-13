# Reproduction

> NPM executable cannot be found at 'npm'

Run:
```zsh
quarkdown c quarkdown-repro.qd --pdf
```

> [!TIP]
> Remove the `.npmrc` file.

Output:
```zsh
quarkdown c quarkdown-repro.qd --pdf
<div class="page-margin-content page-margin-bottom-center"><span class="current-page-number">-</span></div><div class="page-break" data-hidden=""></div><h1 id="repro" data-location="1">repro</h1><p>Welcome to <a href="https://github.com/iamgio/quarkdown">Quarkdown</a>! This is the starting point of your document.</p><ul><li><p>To compile this document, please <span class="codespan-content"><code>cd</code></span> to this file&rsquo;s parent directory and run:<br /><span class="codespan-content"><code>quarkdown c quarkdown-repro.qd</code></span></p></li><li><p>To enable live preview, run:<br /><span class="codespan-content"><code>quarkdown c quarkdown-repro.qd -p -w</code></span></p></li></ul><p>For further information and guides, please check out the <a href="https://github.com/iamgio/quarkdown/wiki">official wiki</a>.</p><figure><img src="media/logo@-421390343.png" alt="Quarkdown" style="width: 50.0%;" /></figure>
Exception in thread "main" java.lang.IllegalStateException: NPM executable cannot be found at 'npm'
        at com.quarkdown.interaction.executable.NodeNpmHelper.checkWrapper(NodeNpmHelper.kt:20)
        at com.quarkdown.interaction.executable.NodeNpmHelper.launch(NodeNpmHelper.kt:55)
        at com.quarkdown.rendering.html.pdf.PuppeteerPdfGeneratorScript.launch(PuppeteerPdfGeneratorScript.kt:39)
        at com.quarkdown.rendering.html.pdf.HtmlPdfExporter.export(HtmlPdfExporter.kt:41)
        at com.quarkdown.rendering.html.pdf.PdfHtmlPostRendererDecorator.generateResources(PdfHtmlPostRendererDecorator.kt:34)
        at com.quarkdown.core.pipeline.Pipeline.executeUnwrapped(Pipeline.kt:213)
        at com.quarkdown.core.pipeline.Pipeline.execute(Pipeline.kt:225)
        at com.quarkdown.cli.exec.strategy.FileExecutionStrategy.execute(FileExecutionStrategy.kt:13)
        at com.quarkdown.cli.exec.ExecuteKt.runQuarkdown(Execute.kt:61)
        at com.quarkdown.cli.exec.ExecuteCommand.execute(ExecuteCommand.kt:231)
        at com.quarkdown.cli.exec.ExecuteCommand.run(ExecuteCommand.kt:219)
        at com.github.ajalt.clikt.core.CoreCliktCommandKt.parse(CoreCliktCommand.kt:107)
        at com.github.ajalt.clikt.core.CoreCliktCommandKt.main(CoreCliktCommand.kt:78)
        at com.github.ajalt.clikt.core.CoreCliktCommandKt.main(CoreCliktCommand.kt:90)
        at com.quarkdown.cli.QuarkdownCliKt.main(QuarkdownCli.kt:27)
```
# quarkdown-reproduction
