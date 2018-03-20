# Nested Category Browser Contentful UI Extension

This extension lets you display a nested tree of categories with checkboxes to display and edit which categories are selected.

![image](https://user-images.githubusercontent.com/6521666/36640958-3fde764a-1a7c-11e8-929b-56574bb6bec0.png)

## Requirements

1. A `category` content type with a bare minimum of a `name` short text/symbol field and a `subcategories` multi-reference field; you certainly can have any other fields you want.
1. One `category` entry with the name `Root` which serves as the entry point into your category tree. You probably also want to make other categories which will be the actual categories shown.
1. One or more other content types with a multi-reference field called `categories` (that name is not strictly necessary, but makes the most sense to me :-P ).
1. The `contentful-cli` tool. If you don't have it, install it by running `yarn global add contentful-cli` or `npm -g install contentful-cli`. After installation run `contentful login` to authorize the `contentful-cli` tool to use your Contentful account.

## Instructions for use

1. Open your terminal, clone this repo (`git clone https://github.com/cachrisman/nested-category-browser`), and change into the directory created (`cd nested-category-browser`)
1. Fill in the space ID and delivery token of the space you are using on lines 31 and 32 of `nested-category-browser.html`.
1. run `contentful extension create --space-id SPACE_ID` replacing `SPACE_ID` with the ID of the space in which you want to install this extension
1. In the Contentful webapp, edit your content model and change the appearance of a `categories` multi-reference field to the `Nested Category Browser Extension` which you have just uploaded.
