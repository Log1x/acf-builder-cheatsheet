# Field Types 

## Basic 

### Text 
```php
$fields
    ->addText('text_field' [
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

### Textarea 
```php
$fields 
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

### Number 
```php
$fields 
    ->addNumber('number_Field', [
        'label' => 'Number Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Email 
```php
$fields 
    ->addEmail('email_field', [
        'label' => 'Email Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### URL 
```php 
$fields
    ->addUrl('url_field', [
        'label' => 'URL Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
        'placeholder' => '',
    ]);
```

### Password 
```php 
$fields 
    ->addPassword('password_field', [
        'label' => 'Password Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

## Content 

### Wysiwyg 
```php
$fields 
    ->addWysiwyg('wysiwyg_field', [
        'label' => 'WYSIWYG Field'
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Oembed
```php
$fields 
    ->addOembed('oembed_field', [
        'label' => 'Oembed Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Image 
```php 
$fields
    ->addImage('image_field', [
        'label' => 'Image FIeld',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### File 
```php
$fields 
    ->addFile('file_Field', [
        'label' => 'File Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Gallery 
```php
$fields 
    ->addGallery('gallery_field', [
        'label' => 'Gallery Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

## Choice 

### Select
```php 
$fields 
    ->addSelect('select_field', [
        'label' => 'Select Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Checkbox
```php
$fields
    ->addCheckbox('checkbox_field', [
        'label' => 'Checkbox Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Radio 
```php
$fields 
    ->addRadio('radio_field', [
        'label' => 'Radio Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### True / False 
```php
$fields 
    ->addTrueFalse('truefalse_field', [
        'label' => 'True / False Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

## Relational 

### Link 
```php 
$fields 
    ->addLink('link_field', [
        'label' => 'Link Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'return_format' => 'array',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/link)

### Post Object 
```php
$fields 
    ->addPostObject('post_object_field', [
        'label' => 'Post Object Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Page Link 
```php
$fields 
    ->addPageLink('page_link_field', [
        'label' => 'Page Link Field',
        'type' => 'page_link',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Relationship 
```php
$fields 
    ->addRelationship('relationship_field', [
        'label' => 'Relationship Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Taxonomy 
```php
$fields 
    ->addTaxonomy('taxonomy_field', [
        'label' => 'Taxonomy Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### User 
```php
$fields 
    ->addUser('user_field', [
        'label' => 'User Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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
[Official Documentation](https://www.advancedcustomfields.com/resources/textarea)

## Miscellaneous

### Google Map
```php
$fields 
    ->addGoogleMap('google_map_field', [
        'label' => 'Google Map Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Date Picker 
```php
$fields 
    ->addDatePicker('date_picker_field', [
        'label' => 'Date Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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

### Date Time Picker
```php
$fields
    ->addDateTimePicker('date_time_picker_field', [
        'label' => 'Date Time Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/date-time-picker)

### Time Picker 
```php
$fields
    ->addTimePicker('time_picker_field', [
        'label' => 'Time Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'display_format' => 'g:i a',
        'return_format' => 'g:i a',
    ]);
```

### Color Picker 
```php
$fields 
    ->addColorPicker('color_picker_field', [
        'label' => 'Color Picker Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
        'wrapper' => [
            'width' => '',
            'class' => '',
            'id' => '',
        ],
        'default_value' => '',
    ]);
```
[Official Documentation](https://www.advancedcustomfields.com/resources/textarea)

### Message 
```php 
$fields 
    ->addMessage('message_field', [
        'label' => 'Message Field',
        'instructions' => '',
        'required' => 0,
        'conditional_logic' => 0,
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
