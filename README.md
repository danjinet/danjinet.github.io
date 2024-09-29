# dnaj.track
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      

I need to highlight these <mark>very important words</mark>.

> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.

<font color="red">This text is red!</font>

> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.

<details open>
<summary>I automatically open</summary>
<br>
Waaa, you see me. I thought I would be hidden ;p .
</details>

<details>
<summary>Heading</summary>
    + markdown list 1
        + nested list 1
        + nested list 2
    + markdown list 2
</details>

<details>
<summary>Heading</summary>
<ul>
<li> markdown list 1</li>
<ul>
<li> nested list 1</li>
<li> nested list 2</li>
</ul>
<li> markdown list 2</li>
</ul>
</details>

:::{dropdown} Dropdown Title
:open:
Dropdown content
:::


%% Mermaid Syntax: Basic to Super Advanced

%% 1. Simple Flowchart
graph TD;
    A[Start] --> B[Process]
    B --> C[End]

%% 2. Decision in Flowchart
    B -->|Yes| D[Condition Met]
    B -->|No| E[Condition Not Met]

%% 3. Loop and Styling
    D --> F[Repeat Process]
    F -->|End Loop| B
    E --> G[Alternative Process]
    G --> H{Is the process complete?}
    H -->|Yes| I[Finish]
    H -->|No| G

%% 4. Adding Subgraphs (Groups)
    subgraph Group 1
        A
        B
    end

    subgraph Group 2
        E
        F
    end

%% 5. Sequence Diagram
    sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, how are you?
    Bob-->>Alice: I am good thanks!

%% 6. Class Diagram
    classDiagram
    class Animal {
        +String species
        +String name
        +run()
    }
    class Dog {
        +bark()
    }
    class Cat {
        +meow()
    }
    Animal <|-- Dog
    Animal <|-- Cat

%% 7. Gantt Chart
    gantt
        dateFormat  YYYY-MM-DD
        title Project Timeline
        section Project Initiation
        Task A      :a1, 2024-09-29, 1d
        Task B      :after a1, 2d
        section Development
        Develop A   :2024-10-01, 3d
        Develop B   :2024-10-04, 2d
        Testing     :2024-10-06, 1d

%% 8. ER Diagram
    erDiagram
        CUSTOMER ||--o{ ORDER : places
        ORDER ||--|{ LINE-ITEM : includes
        PRODUCT ||--o{ LINE-ITEM : "contains"

%% 9. Pie Chart
    pie
        title Sales Distribution 2023
        "Product A" : 40
        "Product B" : 30
        "Product C" : 20
        "Others" : 10


```mermaid
graph TD;
    A[Start] --> B[Process]
    B --> C[End]

### 3. **Using Mermaid with Markdown Renderers**
If you're rendering Markdown using **Static Site Generators** like **Jekyll** or **Hugo**, you may need plugins:
- **Hugo**: Use the [Hugo Mermaid Shortcode](https://gohugo.io/hugo-modules/) or [Hugo Charts.js](https://gohugo.io/content-management/diagrams/).
- **Jekyll**: You can use the [Jekyll Mermaid Plugin](https://github.com/jekyll/jekyll).

### 4. **Browser Support**
If you're viewing your `.md` file in a browser, you can use Mermaid.js directly by including a script in your HTML file that loads Mermaid:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mermaid Diagrams</title>
  <script type="module">
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
    mermaid.initialize({ startOnLoad: true });
  </script>
</head>
<body>
  <pre class="mermaid">
  graph TD;
      A[Start] --> B[Process]
      B --> C[End]
  </pre>
</body>
</html>