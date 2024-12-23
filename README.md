---
license: apache-2.0
task_categories:
- graph-ml
- token-classification
- table-question-answering
pretty_name: docbank-layout
---


## Dataset Summary

DocBank is a large-scale dataset tailored for Document AI tasks, focusing on integrating textual and layout information. It comprises 500,000 document pages, divided into 400,000 for training, 50,000 for validation, and 50,000 for testing. The dataset is generated using a weak supervision approach, enabling efficient annotation of document structures without extensive manual labeling.
Supported Tasks and Leaderboards

    Document Layout Analysis: Identifying and classifying different layout elements within documents based on text and spatial information.
    Token Classification: Assigning layout type classes to individual tokens within the document.

## Languages

    English

## Dataset Structure
### Data Instances

Each instance represents a single document page with the following fields:

    filename: Unique identifier for the document page (MD5 hash of the original filename).
    page_bounding_box: Coordinates defining the overall bounding box of the page ([min_x, min_y, max_x, max_y]).
    lines: A list of tokens present on the page, each with:
        token: The textual content of the token.
        bounding_box: Coordinates defining the position of the token on the page ([x1, y1, x2, y2]).
        label: Layout type class indicating the role of the token (e.g., title, paragraph, table).

### Data Fields

    filename (string): MD5 hash of the original filename, serving as a unique identifier.
    page_bounding_box (list of int): [min_x, min_y, max_x, max_y] coordinates of the entire document page.
    lines (list of dict):
        token (string): Text content of the token.
        bounding_box (list of int): [x1, y1, x2, y2] coordinates of the token's position.
        label (string): Layout type class for the token.

## Additional Information
Dataset Curators

Minghao Li, Yiheng Xu, Lei Cui, Shaohan Huang, Furu Wei, Zhoujun Li, Ming Zhou
Licensing Information

DocBank is licensed under the Apache 2.0 License.
Citation Information

```bibtex
@article{   li2020docbank,
  title          =   { DocBank: A Benchmark Dataset for Document Layout Analysis },
  author         =   { Minghao Li and Yiheng Xu and Lei Cui and Shaohan Huang and Furu Wei and Zhoujun Li and Ming Zhou },
  year           =   { 2020 },
  eprint         =   { 2006.01038 },
  archivePrefix  =   { arXiv },
  primaryClass   =   { cs.CL }
}
```

For more details or inquiries, please refer to the DocBank [https://doc-analysis.github.io/docbank-page/] repository or contact the dataset curators.
