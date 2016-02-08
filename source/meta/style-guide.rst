===========================================
UPIQ QI TeamSpace Documentation Style Guide
===========================================

*This guide documents preferred styles for documenting QI TeamSpace in
reference and tutorial materials.*

.. contents:: Table of Contents
   :local:

Organization
------------

* Avoid long paragraphs.  Communicate ideas in few sentences,
  and emphasize key parts.

* Reserve paragraphs for explanatory writing
  (elaborating on concepts, purpose).

* Enumerate prescribed actions as numbered lists.

* Write descriptions of features and purposes using bulleted lists or tables,
  when possible.

* The "`Information Design <https://wiki.ubuntu.com/DocumentationTeam/StyleGuide/InformationDesign>`_"
  section of the Ubuntu style guide is helpful here.

* Use call-out boxes (ReStructuredText calls this a "topic")
  or side-bars to pair concepts with actions,
  or to point out related concepts or terminology.

* Use admonitions for warnings and hints, but do not overuse.
  See admonition types
  `supported <http://docutils.sourceforge.net/docs/ref/rst/directives.html#admonitions>`_.

* To link to external resources, use inline links.

* Use footnotes only if necessary:

  - When citing external material;

  - When a longer explanation (more than two sentences)
    is required for a concept,
    but such explanation would make scanning the body text too tedious.

  - Remember, since we are outputting to multiple formats
    (HTML, PDF, etc)
    foot notes may actually be end-notes.

  - Where footnotes are placed is subjective, since output is not always paged.
    In general, place footnotes near refering content early in authoring;
    we can and possibly will move them as we refine and edit documentation.

* TBD/TODO items:
  mark sections or chapters in progress with disclaimers
  at the beginning of the section or chapter:

  - *"The content for this section is in progress, and may be incomplete."*

  - *"Some documentation may not reflect recent changes in the software."*


Headings and titles
-------------------

1. Use "`title case <https://en.wikipedia.org/wiki/Letter_case#Case_styles>`_"
   in document, chapter, and section titles.

2. Use "`sentence case <https://en.wikipedia.org/wiki/Letter_case#Case_styles>`_"
   in all minor headings, such as the title of a call-out or topic box
   (e.g. *"Did you know?"* or *"See also"*).

3. Be brief, use descriptive phrases.

4. Attempt to use section and chapter headings
   that are brief enough to appear in a table of contents entry.

5. Generally avoid sentence-ending punctuation in titles,
   if you are not writing a full sentence.

6. Details of heading level formatting:
   see :ref:`Formatting Heading Levels <formatting-headings>`
   for details on proper re-use.

Screenshots
-----------

* **Jargon**: refer to screenshots as a single compound word "screenshot".

* **Crop:** to include relevant context, but only relevant context.

* **Mobile:**
  crop if relevant; you may need to place multiple screenshots
  in sequence to show all context.

* **Complexity:**
  If screen is complex, consider breaking into multiple screenshots.

* **Asset management:**
  Store both original and annotated screenshots;
  if a screenshot is annotated, keep the original in the repository with it.
  If original and annotated images are in different directories,
  use a file naming convention to clearly associate the images witheach other.
  Annotated screenshots should have a respective file-naming suffix.

  - e.g. ``this-thing-here.png`` vs. ``this-thing-here-annotated.png``

* **File format:**
  use PNG images unless screenshot includes a photo that warrants
  (for file size) using JPEG.

* **Annotation:**

  - If you use text overlay, use color and placement that are distinct
    and emphatic versus the image below.

  - If the image below lacks space to have high-contrast overlay text,
    consider using a background color for text-box,
    and place in least obtrusive location on image.
    If all else fails,
    use a clear out-of-image caption with emphasis of clear ideas.

  - Circle important areas of user-interface that are annotated
    with thick-lined ovals or rounded-rectangles.
    Use lines with arrows as necessary, but only if necessary.

  - Consider using iconic language when possible.  For example,
    tools like Skitch have iconographic marker/arrow elements
    that use succinct visual language.

  - Tools that may be helpful to edit or annotate screenshots:

    - Windows/Mac: `Skitch <https://evernote.com/skitch>`_

    - Linux: `Shutter <http://shutter-project.org>`_

* **Hoverable user-interface elements:**
  if you are taking screenshots of user-interface elements
  that change color or behavior (e.g. pop-down menu),
  make sure the action you are describing is highlighted or visible
  before taking a screenshot.

* **Zoom and width:**
  remember that browsers support text zoom in/out;
  sometimes resizing browser window width to a narrower width
  can maximize information-per-pixel —
  for a more effective, efficient screenshot.

* **Window width / text zoom:**
  Use appropriate text size and browser width
  to best communicate the user interface element.


Image captions
--------------

* *Be brief:*
  if screenshot describes or prescribes an action taking place,
  explain in as succinct as language possible.

* *Explain what annotation cannot:*
  if an annotation is not possible or sufficient within the screenshot image,
  use a caption below the image to explain:

  - Context;

  - What is happening?

  - Actions user should take?

Punctuation, grammar, misc.
---------------------------

* Use serial/Oxford commas in lists of three items,
  but avoid comma and paragraph formatting of serial items
  when bulleted lists are more appropriate
  (lists of more than three items more often should be lists, not sentences).

* Use quotation marks around short words used explicitly in the user interface
  (e.g. the "Edit" tab).

* Introduce lists with a colon following the description of the list
  in sentence format.

* List items should have first word capitalized;
  list items that are full sentences should be punctuated
  with a period ending the sentence.
  List items that are not complete sentences may omit or use punctuation
  (e.g. semi-colon) at the writer's discretion.

* Use dash charaters when appropriate; if using hyphens in place of a dash,
  use ``--`` and preferably replace the double-hyphen with an em-dash
  at a later time (most editors have keyboard shortcuts for proper dashes).

Formatting
----------

* Emphasize conceptual highlights of content using italic text.

* Emphasize important (do not miss) content using bold text.

* Inside a sentence, you may use a "`literal <http://docutils.sourceforge.net/docs/ref/rst/roles.html#literal>`_"
  formatting in place of quotation marks for describing something like a 1-3
  word button or tab title.

* Large tables may be created in a spreadsheet, if desired,
  but must be exported to CSV format and have a title row for each column.

* We aim to write content appropriate for output to multiple formats:

  - Some may be paged (PDF).

  - Some may not be (HTML).

  - Some may be artificially paged at arbitrary boundaries (ePub).

* Try to keep plain-text (or reStructuredText) to <79 characters per line;
  this makes using preview easier in tools supporting it.

  - **When possible, use semantic line breaks**,
    as described
    `here <http://rhodesmill.org/brandon/2012/one-sentence-per-line/>`_.

  - There are exceptions to this rule, esp. for lines containing hyperlinks.

* *Italicize example text*, which may also be in quotation marks.

.. _formatting-headings:

* **Formatting Heading Levels:**

  - Restructured text supports multiple levels of headings,
    which should be used as follows,
    consistent with Plone.org documentation [1]_:

    .. code-block:: rst

        ===============================
        Heading 1: Document Title, etc.
        ===============================
        ...

        Heading 2: Section Heading
        --------------------------
        ...

        Heading 3
        ^^^^^^^^^
        ...

        Heading 4
        `````````
        ...


.. [1] Underlining style borrowed from Plone.org
   `Documentation Style Guide <http://docs.plone.org/about/rst-styleguide.html>`_



Source formats, file formats, and character sets
------------------------------------------------

* If writing original copy in a word processor,
  please save files as plain text, preferably in Unicode UTF-8 encoding.

* Text-based symbols/glyphs may be used if they are defined in Unicode 5.0
  and supported for display by all major web browsers.

  - This may include symbols, mathematical operators, shapes.

* Tool-chain:
  We can use `pandoc <http://pandoc.org>`_
  to transform an original word processing document from MSWord .docx or RTF,
  into the reStructuredText format we plan to use for typesetting
  and general maintenance of existing documents;
  however, please edit reStructuredText documents in place,
  once they are the canonical source for a section, chapter, or topic.

* Text-editor: use a text editor capable of saving UTF-8 encoded text
  (e.g. Atom, GEdit).

* Restructured text editing or preview — tools:

  - An `online live preview <http://rst.ninjs.org/>`_

  - `Atom <https://atom.io/>`_ using
    `language-restructuredtext <https://atom.io/packages/language-restructuredtext>`_
    for syntax hightlghting, and
    `rst-preview-pandoc <https://atom.io/packages/rst-preview-pandoc>`_
    for HTML preview.

Diagrams
--------

* Diagrams may describe function or action.  Please attempt to be succinct
  with what you aim to communicate.

* Use arrows to communicate sequence.  Block arrows may be easier to see.

* May be created in any tool, but please save both original editable source
  and PNG output into repository.

* **Graphics tools** — Examples of reasonable tools for creating diagrams:

  - Inkscape

  - Adobe Illustrator

  - Microsoft PowerPoint

    -  *If you lack a more serious alternative... please save single-slide.*

  - LucidChart

  - Evolus Pencil

  - Visio

  - OmniGraffle

* If you are using a vector graphics tool that is not accessible to others
  on the documentation team, please consider exporting a neutral format,
  in addition (e.g. SVG, EPS).

* **Color:**
  use a color tool or theme or your choice that leverages complementary colors,
  but also be mindful of how your diagram looks in black and white
  on a printout or screen (e-Ink).

* Typography:

  - Use a consistent title font (of medium weight or stronger).

  - Please use a sans-serif body text font,
    but choose (same or different) title/heading font that does not conflict
    with that body type face.

* Diagrams take significant effort to create: do not overuse.
  When an existing diagram exists,
  prefer it if sufficient to creating a new diagram,
  even if the existing asset does not match style guidelines.

.. _attribution-section:

Attribution
-----------

* If we use an instrument such as a form definition or measure
  from a project not of UPIQ's own creation, we will do so with both:

  1. Permission;
  2. Attribution of original author and/or organization.

* If we re-purpose upstream documentation (e.g. from Plone),
  it should be licensed in such a way to allow this
  (e.g. open-source, from Plone.org),
  and attributed in a footnote for a section.

  - Please see terms of license for documentation re-purposed from
    `Plone Documentation <http://docs.plone.org>`_.  These are licenesed
    under the `Creative Commons Attribution 4.0 International <http://creativecommons.org/licenses/by/4.0/>`_
    license.  You should generally prefix any attribution footnote with:

      Portions of content in this chapter modified from
      `Plone.org Documentation <http://docs.plone.org/>`_.

  - You are encouraged to deep-link to the specific chapter in any large
    body of upstream documentation attributed in a footnote.

Copyright
---------

* Individual chapters need not have a copyright notice; whole guides should.

* Copyright notices in books need not spell out a full license
  for use and distribution, but should specify the name of the license
  and a link to a stable version.

* The source repository of the documentation will contain in a file
  the full text of the license.

* End matter for documentation should include a succinct copyright statment:

    .. code-block:: rst

        Copyright 2016, The University of Utah.

        Licensed for free use and re-distribution under an MIT-style license,
        which can be found here:

        `<https://teamspace.upiq.org/trac/wiki/Copyright>`_

* All documentation should be licensed under an MIT-style license, which can
  be referenced at a stable URL.

Mock content
------------

* **Identifying information:**
  do not include content in documentation screenshots that identifies
  an existing TeamSpace user or their organization
  (e.g. medical practice name).

  - Exceptions: you may include content identifying UPIQ or University of Utah
    Department of Pediatrics staff and clinics.

  - We do not include organizational logos other than UPIQ's
    in any published screenshots of non-UPIQ sites.

* **Images and documents:**
  stock images and documents displayed within screenshots
  should have permissive copyright licensing,
  e.g. creative commons or public domain.
  While we should have fair use rights to any image incidentally included
  in screenshots, regardless of copyright holder,
  it is sensible to be careful in this area.

* **Mock content and names for things**:

  - **Team/practice names**:

    - "Alpha Team" / "Beta Team"

    - "ACME Practice"

  - **Surnames:** if using multiple (2+) surnames in example content,
    vary ethnicities of those surnames to reflect real-world diversity.

  - **Mock copy** *(names of things, descriptions, body text)*:

    - Feel free to use "lorem ipsum" text in long copy.

    - Use brief titles, when possible.  **Be succinct**.

    - When writing "description" field copy for a screenshot, just elaborate
      on the content chosen for title.
      *Do not exceed two sentences or three lines in mock description copy.*


* **De-identification tools:**
  you can use the use the "DOM inspector" tool
  of your web browser to modify any HTML element text,
  prior to taking screenshots.
  For example, in a screenshot of a plot with a legend item
  reading "University Pediatric Clinic", you can visually select the element,
  using the inspector and edit its text to read something like "ACME Clinic".

User interface element glossary
-------------------------------

* Referring to tabs and actions:

  * In current TeamSpace versions, all content (forms, folders, reports, etc)
    have clickable actions that are either:

    - In (drop-down) ``"action menus"``;

    - Displayed as a ``"tab"``.

  * **Plone 5 (future TeamSpace)** will replace both of the above
    (tabs, drop-down menus) with "toolbar" buttons or menus.
    Drop-down action menus become ``"toolbar menu"``
    and content tabs become ``"toolbar buttons"``.

  * We want to be able to use search/replace on upgrade in describing
    these user-interface metaphors,
    and in identifying pages with outdated screenshots.
    **For example, the following sentences would be before/after:**

    - **Plone 4:**

        *From the "View" tab of the form,
        select the "Actions" menu from the top-bar;
        in the menu, select the "Download Workbook" option
        to download an Excel worksheet containing your form.*


    - **Plone 5:**

        *In the main toolbar,
        select the "View" button for the form;
        from the "Actions" menu in the toolbar,
        select the "Download Workbook" option
        to download an Excel worksheet containing your form.*

  * We should use consistent language when describing all of the following
    in Plone 4 / current TeamSpace,
    to make it easier to identify near-future updates for Plone 5.
    While much of the terminology for menus stays the same,
    where the menus are located will change eventually in Plone 5.
    Consideration/care should include all of the following UI elements:

    - Content tabs
    - "Actions" menu (content)
    - "Add new" menu (content)
    - "Display" menu (content)
    - Workflow state menu (content)
    - Other elements including "personal menu" and links to "manage portlets"
      on content.

UI Element Diagram
------------------

* A **visual diagram/map** of user interface elements will be created by UPIQ
  (**TBD/TODO**).

  **This should include all of the following:**

  - Content tabs
  - Drop-down menus (content)
    - Actions
    - Add new
    - Display
    - (workflow) State
  - Global tabs (usually disabled in TeamSpace site)
  - Left navigation (or "left navigation portlet" or "navigation portlet").
  - Left portlet column;
  - Right portlet column;
  - Main content area;
  - Document/content byline;
  - Document/content history;
  - Search box;
  - Project/site main navigation buttons (home, top).
  - Content title, description.
  - (Pop-up) "overlay" boxes.
  - Edit tab: field set (tab vs. menu).
  - "Contents tab" elements.


Upstream documentation
----------------------

* `Plone 4 Documentation: Working with Content <http://docs.plone.org/4/en/working-with-content/index.html>`_

  - See the :ref:`Attribution section <attribution-section>` for details on proper re-use.

* `*A Users Guide to Plone 4* <http://www.enfoldsystems.com/support/a-users-guide-to-plone.html>`_ (book)

* Note: some items in upstream documentation may be out-of-date versus upgrades
  or customizations made to the core platform by UPIQ.
  For example, after February 2016, we will be using a newer "visual editor"
  widget (TinyMCE 4), where stock Plone 4.3 uses an older version of TinyMCE.
  For documentation of visual editing of HTML page content, the
  `TinyMCE material for Plone 5 <http://docs.plone.org/working-with-content/using-tinymce-as-visual-editor/index.html>`_
  is more relevant.

Notes on our problem domain
---------------------------

* **Problem domain:**
  QI TeamSpace is a tool that aims to facilitate organizations working together
  toward improvement of healthcare quality on one or more topics.
  Below is a short list of resources on common ideas or jargon used
  in the problem domain we operate in:

  - `Quality improvement (QI) <http://www.who.int/patientsafety/education/curriculum/who_mc_topic-7.pdf>`_

  - `PDSA cycle <http://patientsafetyed.duhs.duke.edu/module_a/methods/pdsa.html>`_

  - Chart Review (also known as "Chart audit", but "Chart Review" is preferred):
    - `Basics <http://patientsafetyed.duhs.duke.edu/module_b/quaility_improvement.html>`_
    - `Examples <http://www.aafp.org/fpm/2008/0700/pa3.html>`_ (from AAFP).

  - *"Measures"* in quality improvement often refer to things we can assess
    continually at some frequency to assess quantiative evidence
    of improvement to some goal.
    In TeamSpace, measures are based on form data,
    whether from detailed chart review or simple numbers in aggregate form.

  * Forms in quality improvement: often collected in both worksheet
    (paper or spreadsheet), and then entered into a tool like TeamSpace.
    Some forms are qualitative in nature,
    while others collect detailed or aggregate quantitative data.

  * **Protected health information (PHI):**
    we do not store protected health information in TeamSpace.
    Documentation should make clear to users in sections related to data-entry
    that this is the case.
    We maintain this restriction to avoid regulatory burden.
    At some future date, this may change, but not for foreseeable future.

  * Some documentation of features will describe the functions of the software
    in the language and through examples within this problem domain.

