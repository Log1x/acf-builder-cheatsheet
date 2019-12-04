# ACF Builder Cheatsheet

This cheatsheet consists of ACF Field Type arguments for use with [ACF Builder](https://github.com/StoutLogic/acf-builder/) as well as the known (most of which are not documented) configuration methods to assist in building fields. While the below field types reveal all of the possible configuration passable in the field type config array, most have available chainable methods to assist in building out cleaner, more readable code.

If you are new to ACF Builder and would like to learn more, you can read my guide [here](https://roots.io/guides/using-acf-builder-with-sage/).

## Table of Contents

| [Basic](#basic)       | [Content](#content) | [Choice](#choice)            | [Relational](#relational)     | [jQuery](#jquery)                     | [Layout](#layout)                     | [Configuration](#configuration)   |
|:----------------------|:--------------------|:-----------------------------|:------------------------------|:--------------------------------------|:--------------------------------------|:----------------------------------|
| [Text](#text)         | [Wysiwyg](#wysiwyg) | [Select](#select)            | [Link](#link)                 | [Google Map](#google-map)             | [Message](#message)                   | [Composing](#composing-fields)    |
| [Textarea](#textarea) | [Oembed](#oembed)   | [Checkbox](#checkbox)        | [Post Object](#post-object)   | [Date Picker](#date-picker)           | [Accordion](#accordion)               | [Modifying](#modifying-fields)    |
| [Number](#number)     | [Image](#image)     | [Radio](#radio)              | [Page Link](#page-link)       | [Date Time Picker](#date-time-picker) | [Tab](#tab)                           | [Removing](#removing-fields)      |
| [Range](#range)       | [File](#file)       | [True / False](#true--false) | [Relationship](#relationship) | [Time Picker](#time-picker)           | [Group](#group)                       | [Choices](#field-choices)         |
| [URL](#url)           | [Gallery](#gallery) |                              | [Taxonomy](#taxonomy)         | [Color Picker](#color-picker)         | [Repeater](#repeater)                 | [Conditions](#field-conditions)   |
| [Password](#password) |                     |                              | [User](#user)                 |                                       | [Flexible Content](#flexible-content) | [Wrapper](#field-wrapper)         |
|                       |                     |                              |                               |                                       |                                       | [Location](#field-group-location) |

## Field Types

### Basic

#### Text
```php
$builder
    ->addText('text_field', [
        'label' => 'Text Field',
        'instructions' => '',
        'required' => 0,
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
        'placeholder' => '',
        'prepend' => '',
        'append' => '',
        'maxlength' => '',
  ]);
```
[Official Documentation]( https://www.advancedcustomfields.com/resources/text)

#### Textarea
```php
$builder
  ->addTextarea('textarea_field', [
      'label' => 'Textarea Field',
      'instructions' => '',
      'required' => 0,
      'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
      ],
      'default_value' => '',
      'placeholder' => '',
      'maxlength' => '',
      'rows' => '',
      'new_lines' => '',
  ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/textarea)

#### Number
```php
$builder
    ->addNumber('number_Field', [
        'label' => 'Number Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
        'placeholder' => '',
        'prepend' => '',
        'append' => '',
        'min' => '',
        'max' => '',
        'step' => '',
  ]);
```

#### Range
```php
$builder
    ->addRange('range_field', [
        'label' => 'Range Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'default_value' => '',
        'min' => '',
        'max' => '',
        'step' => '',
        'prepend' => '',
        'append' => '',
    ]);
```

#### Email
```php
$builder
    ->addEmail('email_field', [
        'label' => 'Email Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
        'placeholder' => '',
        'prepend' => '',
        'append' => '',
    ]);
```

#### URL
```php
$builder
    ->addUrl('url_field', [
        'label' => 'URL Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
        'placeholder' => '',
    ]);
```

#### Password
```php
$builder
    ->addPassword('password_field', [
        'label' => 'Password Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'placeholder' => '',
        'prepend' => '',
        'append' => '',
    ]);
```

### Content

#### Wysiwyg
```php
$builder
    ->addWysiwyg('wysiwyg_field', [
        'label' => 'WYSIWYG Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
        'tabs' => 'all',
        'toolbar' => 'full',
        'media_upload' => 1,
        'delay' => 0,
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/wysiwyg)

#### Oembed
```php
$builder
    ->addOembed('oembed_field', [
        'label' => 'Oembed Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'width' => '',
        'height' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/oembed)

#### Image
```php
$builder
    ->addImage('image_field', [
        'label' => 'Image FIeld',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'return_format' => 'array',
        'preview_size' => 'thumbnail',
        'library' => 'all',
        'min_width' => '',
        'min_height' => '',
        'min_size' => '',
        'max_width' => '',
        'max_height' => '',
        'max_size' => '',
        'mime_types' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/image)

#### File
```php
$builder
    ->addFile('file_Field', [
        'label' => 'File Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'return_format' => 'array',
        'library' => 'all',
        'min_size' => '',
        'max_size' => '',
        'mime_types' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/file)

#### Gallery
```php
$builder
    ->addGallery('gallery_field', [
        'label' => 'Gallery Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'min' => '',
        'max' => '',
        'insert' => 'append',
        'library' => 'all',
        'min_width' => '',
        'min_height' => '',
        'min_size' => '',
        'max_width' => '',
        'max_height' => '',
        'max_size' => '',
        'mime_types' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/gallery)

### Choice

#### Select
```php
$builder
    ->addSelect('select_field', [
        'label' => 'Select Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'choices' => [],
        'default_value' => [],
        'allow_null' => 0,
        'multiple' => 0,
        'ui' => 0,
        'ajax' => 0,
        'return_format' => 'value',
        'placeholder' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/select)

#### Checkbox
```php
$builder
    ->addCheckbox('checkbox_field', [
        'label' => 'Checkbox Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'choices' => [],
        'allow_custom' => 0,
        'save_custom' => 0,
        'default_value' => [],
        'layout' => 'vertical',
        'toggle' => 0,
        'return_format' => 'value',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/checkbox)

#### Radio
```php
$builder
    ->addRadio('radio_field', [
        'label' => 'Radio Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'choices' => [],
        'allow_null' => 0,
        'other_choice' => 0,
        'save_other_choice' => 0,
        'default_value' => '',
        'layout' => 'vertical',
        'return_format' => 'value',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/radio-button)

#### Button Group
```php
$builder
    ->addButtonGroup('button_group_field', [
        'label' => 'Button Group Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'choices' => [],
        'allow_null' => 0,
        'default_value' => '',
        'layout' => 'horizontal',
        'return_format' => 'value',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/button-group/)

#### True / False
```php
$builder
    ->addTrueFalse('truefalse_field', [
        'label' => 'True / False Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'message' => '',
        'default_value' => 0,
        'ui' => 0,
        'ui_on_text' => '',
        'ui_off_text' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/true-false)

### Relational

#### Link
```php
$builder
    ->addLink('link_field', [
        'label' => 'Link Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'return_format' => 'array',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/link)

#### Post Object
```php
$builder
    ->addPostObject('post_object_field', [
        'label' => 'Post Object Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'post_type' => [],
        'taxonomy' => [],
        'allow_null' => 0,
        'multiple' => 0,
        'return_format' => 'object',
        'ui' => 1,
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/post-object/)

#### Page Link
```php
$builder
    ->addPageLink('page_link_field', [
        'label' => 'Page Link Field',
        'type' => 'page_link',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'post_type' => [],
        'taxonomy' => [],
        'allow_null' => 0,
        'allow_archives' => 1,
        'multiple' => 0,
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/page-link)

#### Relationship
```php
$builder
    ->addRelationship('relationship_field', [
        'label' => 'Relationship Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'post_type' => [],
        'taxonomy' => [],
        'filters' => [
            0 => 'search',
            1 => 'post_type',
            2 => 'taxonomy',
        ],
        'elements' => '',
        'min' => '',
        'max' => '',
        'return_format' => 'object',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/relationship)

#### Taxonomy
```php
$builder
    ->addTaxonomy('taxonomy_field', [
        'label' => 'Taxonomy Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'taxonomy' => 'category',
        'field_type' => 'checkbox',
        'allow_null' => 0,
        'add_term' => 1,
        'save_terms' => 0,
        'load_terms' => 0,
        'return_format' => 'id',
        'multiple' => 0,
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/taxonomy)

#### User
```php
$builder
    ->addUser('user_field', [
        'label' => 'User Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'role' => '',
        'allow_null' => 0,
        'multiple' => 0,
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/user/)

### jQuery

#### Google Map
```php
$builder
    ->addGoogleMap('google_map_field', [
        'label' => 'Google Map Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'center_lat' => '',
        'center_lng' => '',
        'zoom' => '',
        'height' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/google-map)

#### Date Picker
```php
$builder
    ->addDatePicker('date_picker_field', [
        'label' => 'Date Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'display_format' => 'd/m/Y',
        'return_format' => 'd/m/Y',
        'first_day' => 1,
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/date-picker)

#### Date Time Picker
```php
$builder
    ->addDateTimePicker('date_time_picker_field', [
        'label' => 'Date Time Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/date-time-picker)

#### Time Picker
```php
$builder
    ->addTimePicker('time_picker_field', [
        'label' => 'Time Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'display_format' => 'g:i a',
        'return_format' => 'g:i a',
    ]);
```

#### Color Picker
```php
$builder
    ->addColorPicker('color_picker_field', [
        'label' => 'Color Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/color-picker/)

### Layout

#### Message
```php
$builder
    ->addMessage('message_field', [
        'label' => 'Message Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'message' => '',
        'new_lines' => 'wpautop',
        'esc_html' => 0,
    ]);
```

#### Accordion
```php
$builder
    ->addAccordion('accordion_field', [
        'label' => 'Accordion Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'open' => 0,
        'multi_expand' => 0,
        'endpoint' => 0,
    ]);

$builder
    ->addAccordion('accordion_field_end')->endpoint();
```
[Official Documentation](https://www.advancedcustomfields.com/resources/accordion/)

#### Tab
```php
$builder
    ->addTab('tab_field', [
        'label' => 'Tab Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'default_value' => '',
        'placeholder' => '',
        'prepend' => '',
        'append' => '',
        'maxlength' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/tab/)

#### Group
```php
$builder
    ->addGroup('group_field', [
        'label' => 'Group Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'layout' => 'block',
        'sub_fields' => [],
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/group/)

#### Repeater
```php
$builder
    ->addRepeater('repeater_field', [
        'label' => 'Repeater Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'collapsed' => '',
        'min' => 0,
        'max' => 0,
        'layout' => 'table',
        'button_label' => '',
        'sub_fields' => [],
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/repeater/)

#### Flexible Content
```php
$builder
    ->addFlexibleContent('flexible_content_field', [
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => [],
        'wrapper' => [
          'width' => '',
          'class' => '',
          'id' => '',
        ],
        'button_label' => 'Add Row',
        'min' => '',
        'max' => '',
    ]);

$builder
    ->addLayout('layout', [
        'label' => 'Layout',
        'display' => 'block',
        'sub_fields' => [],
        'min' => '',
        'max' => '',
    ]);

$builder
    ->addLayout(new FieldsBuilder());
```
[Official Documentation](https://www.advancedcustomfields.com/resources/flexible-content/)

## Configuration


### Composing Fields
```php
$builder
    ->addFields(new FieldsBuilder());

$builder
    ->addField('text', 'title')
        ->setKey('field_title')
        ->setDefaultValue('My Title')
        ->setInstructions('This is a title.')
        ->setRequired()
            ->setUnrequired()
        ->setConfig('placeholder' => 'Enter the title');
  ```

### Modifying Fields
```php
$builder
    ->modifyField('title', ['label' => 'Modified Title']);

$builder
    ->addFields(new FieldsBuilder())
        ->getField('title')
            ->modifyField('title', ['label' => 'Modified Title']);
```

### Removing Fields
```php
$builder
    ->removeField('title');
```

### Field Choices
```php
$builder
    ->addChoice('red')
    ->addChoice('blue')
    ->addChoice('green');

$builder
    ->addChoices(['red' => 'Red'], ['blue' => 'Blue'], ['green' => 'Green']);
```

### Field Conditions
```php
$builder
    ->conditional('true_false', '==', '0')
        ->and('true_false', '!=', '1')
        ->or('false_true', '==', '1');
```

### Field Wrapper
```php
$builder
    ->setWidth('30');

$builder
    ->setSelector('.field')
    ->setSelector('#field');

$builder
    ->setAttr('width', '30')
    ->setAttr('class', 'field')
    ->setAttr('id', 'field');

$builder
    ->setWrapper(['width' => '30', 'class' => 'field', 'id' => 'field']);
```

### Field Group Location

```php
$builder
    ->setLocation('post_type', '==', 'page')
        ->and('page_type', '==', 'front_page');
```
