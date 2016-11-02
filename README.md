# Exam: HTML & CSS

# Tasks

## 1. Build a design (~90 minutes) [10 points]
Build the following profile cards according to the design provided.   
Follow the design as closely as possible.   
Commit an HTML and a CSS file to this repository.

### Acceptance criteria
The task is accepted if:
  - The result follows design [2p]
  - The code follows style guide [1p]
  - The CSS & HTML are valid [1p]
  - The HTML considers semantic responsibilities [2p]
  - The code avoids code duplication [2p]
  - The CSS has meaningful and short selectors [2p]

Extra points for if:
  - the result is centered on the page [2p]


## 2. Understand code (~15 minutes) [2 points]
Read the following code snippet:   
What is the distance between the top-left corner of the document body and the yellow box?   
Give a detailed explanation below!   
Add your answer to this readme file, commit your changes to this repository.
```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        padding: 0px;
        margin: 0px;
      }
      .foo {
        top: 20px;
        left: 20px;
        width: 100px;
        height: 100px;
        position: absolute;
        background: blue;
      }
      .bar {
        top: 20px;
        left: 20px;
        width: 30px;
        height: 30px;
        position: absolute;
        background: yellow;
      }
    </style>
  </head>
  <body>
    <div class="foo">
      <div class="bar"></div>
    </div>
  </body>
</html>
```
#### Your answer: [2p]

The distance between the document body and the yellow box is 40px from the top and 40px from the left.
The position of the blue box is set 20px from the document body's top and left while the position of the yellow box is set 20px absolutely from the blue box's top and left.
Therefore the distance is 20px + 20px = 40px from both directions.


## 3. Explain concepts (~15 minutes) [4 points]
Add your answer to this readme file, commit your changes to this repository.


### Explain the difference between `display: block` and `display: inline` in CSS! What is `display: inline-block`?
#### Your answer: [2p]

HTML elements have a default display property value depending on element type and browser.
Block elements will start in a new line and take up all available space, therefore no other block level elements will be displayed in the same line. They can have margins and padding and can have set height and width.
Inline elements will not start new lines and take up only the necessary space, therefore a series of inline elements can be displayed without a line break which will only occur if all available space is taken up. Top and bottom margins cannot be set, nor the height and width.
Inline-block elements have a block element box with adjustable height and width. The flow of the surrounding elements, however, will behave like an inline box.


### What is the difference between a `<section>` and an `<article>` element? Name one good example of using an `<article>`.
#### Your answer: [2p]

The <article> element is a stand-alone, discrete piece of content (usual examples given: forum or blog post, news item, etc.). One of the most common test to see whether an element is article level is if it would make sense in an RSS feed stripped of its context.
The <section> element is instead used to break up a page into different thematic groupings, or an article into parts. It should be used for blocks of semantically related content.
Naturally, an article can be divided into multiple sections.
In some cases, eg. a page where articles about two topics are grouped, a section element can represent one of the groupings, and be the parent of several article elements with the actual content of the page.
A good use of an article would be a blogpost with comments. The comments themselves are seen as individual articles but are section off from the main blogpost. eg:

<article>
  <header>
    <h1>Title of blogpost</h1>
  </header>

  <p>content of blogpost</p>
  <p>content of blogpost</p>
  <p>content of blogpost</p>

  <section>
    <h2>Comments</h2>

      <article>
        <header>
          <h3>Author of comment</h3>
        </header>
        <p>comments about blogpost</p>
      </article>

      <article>
        <header>
          <h3>Author of comment2</h3>
        </header>
        <p>other comments about blogpost</p>
      </article>

  </section>
</article>
