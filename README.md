# Ultra Comprehensive LaTeX Conversion Test Document 
With a Second Line

*The Test Suite Crew 
Including Parker*

*September 15, April 12, 2025*

*This is the abstract. It spans multiple lines in the source LaTeX file. It should be converted to a single, italicized paragraph in Markdown. Let's include some escaped characters like %percent, &ampersand, #hash, and _underscore here too. Final line of abstract.*

## Introduction and Basic Text

Welcome to the comprehensive test. This paragraph has no special formatting.

This second paragraph is separated by a blank line. It contains **bold text**, *italic text*, and `monospaced text`. We also test *emphasized text*. Let's try ***nested bold and italic***. What about `**bold inside monospace**`? (Note: Nested formatting might simplify).

This line includes a manual break
right here.
The text continues after the break.

This paragraph has extra    whitespace at the end.
And this line has leading whitespace.
This line has both leading and trailing whitespace.

## Section Without Numbering

This section used `
section*`. It should appear as a regular `##` header in Markdown.

### Testing Links and Escaped Characters

Here's a plain URL: <https://github.com/user/repo>.
And another: <mailto:test@example.com>.
Here's a hyperlink using href: Google Search.
Let's test escaped characters again in regular text: 100% works, use & for 'and', # symbol, file_name.txt.
What about an escaped percent sign within a comment?

### Subsection Without Numbering

This subsection used `
subsection*`. It should appear as `###`.

#### Testing Lists Thoroughly

Here comes an itemized list:

- First item. Plain and simple.

- Second item contains **bold** and *italic* text. It also has a line break
within it.

- Third item: <https://example.com/list-item-url>.

- Fourth item includes `code style`.

- Let's test nesting (should be removed by the script):
\begin{itemize}

- This is a nested item. It should disappear.

- Another nested item. Also gone.

Text after nested list but before next item (might merge or disappear depending on exact regex).
\item Fifth item, appearing after the (removed) nested block.
\item Final item in the first list.
\end{itemize}

Now, some text separating the lists.

Here comes a numbered list:

1. First numbered item. Using *emphasis*.
2. Second item.
3. Third item with escaped chars: % & # _ and a link Example Org.
4. Fourth item with a
line break.
5. Testing nesting again (should be removed):
\begin{enumerate}
6. Nested numbered item 1. Should vanish.
7. Nested numbered item 2. Should vanish.

\item Sixth item, after the removed nested enumerate.
\end{enumerate}

#### Subsubsection Without Numbering

This used `
subsubsection*`. Should appear as `####`.

## Code Blocks and Verbatim

Testing the `verbatim` environment.

```

This is line 1 inside verbatim.
This line has leading spaces.
Special characters like $, #, %, &, {, }, \ should be preserved literally.

function example(x) {
return x * 100; % This percent sign should remain!
}

\command{argument} % Backslashes should remain.

Final line of verbatim.

```

Text immediately following the verbatim block to check spacing.

## Combinations and Edge Cases

This paragraph mixes **bold**, *italic*, `code`, *emphasis*, escaped chars (% & # _), a URL <https://edge.case/test?param=1&ok=true>, a link Another Link, and a line break
all together.

What happens with empty environments?

```

```

Text after empty environments.

Metadata commands appearing late (should have been processed/removed earlier or ignored now):

Final paragraph. Just checking spacing and the end of the document conversion.
