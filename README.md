# 📚 e_book – Flutter Application

e_book is a modern e‑book reader designed to deliver a smooth and interactive reading experience. It’s built with Flutter, following clean architecture principles, and demonstrates advanced skills in UI/UX, state management, and Firebase integration.

---

## ✨ Features
📖 Read PDF books with zoom, highlighting, and note‑taking.

🔄 Flexible navigation: horizontal, vertical, or page‑by‑page.

✍ Notes management: add and organize your thoughts directly inside the book.

🔐 Secure authentication with Firebase and Google Sign‑In.

🌍 Multi‑language support using localization.

🎨 Modern UI/UX with responsive layouts, Lottie animations, and skeleton loaders.

📲 Real‑time notifications powered by Firebase Messaging.

⚡ Scalable architecture using BLoC and Dependency Injection.

---
## 📸 Demo Preview

![image alt](https://github.com/AMFathyDev/e_book/blob/1ae419aa574f47bb7db15708b41141a6def6fecd/e_book_demo_screens.png.png)

> A modern platform to explore, read, and save your favorite books.  
> Search titles, track your reading, and build your personal library—all in one place.

## 🎥 Demo Video
You can watch a demo of the *e_book app* here:  
[▶ Watch Demo](https://drive.google.com/file/d/1F5d_E5D4BA7l7aTUY3kCbPR1GBlX8Ju2/view?usp=drive_link)

---

## 📦 Download APK
Try out the app by downloading the APK:  
[⬇ Download APK](https://drive.google.com/file/d/1yO0ZLpP3SMsZt0toevwkWT0gDpSGGIb5/view?usp=drive_link)


## 🛠 Tech Stack & Packages
- *UI & Icons*  
  - cupertino_icons: ^1.0.8 – iOS-style icons  
  - flutter_screenutil: ^5.9.3 – Responsive UI design  
  - iconly: ^1.0.1 – Modern icon pack  
  - lottie: ^3.1.0 – Lottie animations  
  - skeletonizer: ^2.1.0+1 – Skeleton loading placeholders  
  - confetti: ^0.7.0 – Celebration animations  

- *PDF & Media*  
  - syncfusion_flutter_pdfviewer: ^29.1.33 – PDF viewer with zoom & annotations  
  - flutter_colorpicker: ^1.1.0 – Color picker widget  
  - flutter_svg: ^2.2.0 – Render SVG images  
  - cached_network_image: ^3.4.1 – Load & cache network images  

- *State Management & Utilities*  
  - flutter_bloc: ^9.1.1 – BLoC pattern for state management  
  - equatable: ^2.0.5 – Simplifies value comparison  
  - dartz: ^0.10.1 – Functional programming utilities  
  - get_it: ^8.2.0 – Dependency injection & service locator  

- *Networking & APIs*  
  - dio: ^5.9.0 – Powerful HTTP client  

- *Localization*  
  - easy_localization – Internationalization & multi-language support  

- *Firebase Services*  
  - firebase_core: ^4.0.0 – Core Firebase SDK  
  - firebase_auth: ^6.0.1 – Authentication  
  - cloud_firestore – Real-time NoSQL database  
  - firebase_storage: ^13.0.1 – Store & retrieve files  
  - firebase_messaging: ^16.0.1 – Push notifications  

- *Other*  
  - google_sign_in: ^6.2.1 – Google authentication  
  - file_picker: ^10.3.2 – Pick files from device storage  

---
##   Structure
```text
lib/
├── app/
│   ├── drawer/
│   │   ├── custom_drawer.dart
│   │   ├── drawer_animation_wrapper.dart
│   │   ├── drawer_background.dart
│   │   ├── drawer_content.dart
│   │   ├── icon_text_row.dart
│   │   └── language_switcher.dart
│   └── mainlayout/
│       ├── active_indicator.dart
│       ├── bottom_nav_btn.dart
│       ├── bottom_navigation.dart
│       ├── clipper.dart
│       ├── constants.dart
│       ├── final_view.dart
│       ├── nav_button.dart
│       ├── page_view_widget.dart
│       └── size_config.dart
├── core/
│   ├── di/
│   │   └── service_locator.dart
│   ├── helpers/
│   │   ├── fade_navigator.dart
│   │   ├── spacing.dart
│   │   └── trans_parent_status_bar.dart
│   ├── network/
│   │   ├── api_service.dart
│   │   ├── auth_service.dart
│   │   ├── favorites_service.dart
│   │   └── errors/
│   │       ├── failures.dart
│   │       └── firebase_notification.dart
│   ├── theming/
│   │   ├── colors_manager.dart
│   │   └── styles.dart
│   └── widgets/
│       ├── book_detail_card/
│       │   ├── author_name.dart
│       │   ├── book_card_with_title.dart
│       │   ├── book_detail_card.dart
│       │   ├── book_title.dart
│       │   ├── price_text.dart
│       │   ├── rating_count.dart
│       │   ├── rating_score.dart
│       │   ├── rating_section.dart
│       │   └── rating_star.dart
│       ├── app_description.dart
│       ├── app_logo.dart
│       ├── app_title.dart
│       ├── back_button.dart
│       ├── custom_appbar.dart
│       ├── custom_book_card.dart
│       ├── custom_button.dart
│       ├── custom_error_widget.dart
│       ├── lotti_animation.dart
│       ├── menu_icon.dart
│       └── user_avatar.dart
├── features/
│   ├── account/
│   │   ├── data/
│   │   │   └── models/
│   │   │       └── favorite_book.dart
│   │   ├── logic/
│   │   │   ├── favorite_cubit.dart
│   │   │   └── favorite_state.dart
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── account_screen.dart
│   │       └── widgets/
│   │           ├── account_body.dart
│   │           ├── books_header.dart
│   │           ├── content_account_section.dart
│   │           ├── favorite_card.dart
│   │           ├── favorite_list.dart
│   │           └── favorite_skeleton_loader.dart
│   ├── details_book/
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── details_book_screen.dart
│   │       └── widgets/
│   │           ├── about_book_section.dart
│   │           ├── action_buttons.dart
│   │           ├── add_favorite.dart
│   │           ├── appbar_details_book.dart
│   │           ├── book_author.dart
│   │           ├── book_cover.dart
│   │           ├── book_description.dart
│   │           ├── book_meta_data.dart
│   │           ├── book_option.dart
│   │           ├── book_title.dart
│   │           ├── content_details_book_section.dart
│   │           ├── details_book_body.dart
│   │           ├── header_details_book_section.dart
│   │           ├── label_and_value_text.dart
│   │           ├── title_with_description.dart
│   │           └── vertical_divider.dart
│   ├── home/
│   │   ├── data/
│   │   │   ├── models/
│   │   │   │   ├── access_info.dart
│   │   │   │   ├── book_model.dart
│   │   │   │   ├── epub.dart
│   │   │   │   ├── image_links.dart
│   │   │   │   ├── industry_identifier.dart
│   │   │   │   ├── panelization_summary.dart
│   │   │   │   ├── pdf.dart
│   │   │   │   ├── reading_modes.dart
│   │   │   │   ├── sale_info.dart
│   │   │   │   └── volume_info.dart
│   │   │   └── repos/
│   │   │       ├── home_repo.dart
│   │   │       └── home_repo_impl.dart
│   │   ├── logic/
│   │   │   ├── interests_books/
│   │   │   │   ├── interests_books_cubit.dart
│   │   │   │   └── interests_books_state.dart
│   │   │   └── trending_books/
│   │   │       ├── trending_books_cubit.dart
│   │   │       └── trending_books_state.dart
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── home_screen.dart
│   │       └── widgets/
│   │           ├── app_home_title.dart
│   │           ├── content_home_section.dart
│   │           ├── greeting_section.dart
│   │           ├── greeting_text.dart
│   │           ├── header_home_section.dart
│   │           ├── home_body.dart
│   │           ├── interests_section.dart
│   │           ├── motivational_text.dart
│   │           ├── section_title.dart
│   │           ├── trending_books_list.dart
│   │           ├── trending_books_skeleton_loader.dart
│   │           ├── trending_section.dart
│   │           ├── your_interests_books_list.dart
│   │           └── your_interests_skeleton_loader.dart
│   ├── notification/
│   │   ├── logic/
│   │   │   ├── notification_cubit.dart
│   │   │   └── notification_state.dart
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── notification_screen.dart
│   │       └── widgets/
│   │           ├── notification_body.dart
│   │           └── notification_card.dart
│   ├── read_book/
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── read_book_screen.dart
│   │       └── widgets/
│   │           ├── pdf_search/
│   │           │   ├── pdf_search_toast.dart
│   │           │   ├── pdf_search_toolbar.dart
│   │           │   ├── search_cancel_button.dart
│   │           │   ├── search_result_counter.dart
│   │           │   ├── search_text_field.dart
│   │           │   └── search_toolbar.dart
│   │           ├── pdf_toolbar/
│   │           │   ├── pdf_bookmark_button.dart
│   │           │   ├── pdf_first_page_button.dart
│   │           │   ├── pdf_search_button.dart
│   │           │   ├── pdf_settings_menu.dart
│   │           │   ├── pdf_sticky_note_button.dart
│   │           │   ├── pdf_text_toolbar_button.dart
│   │           │   ├── pdf_toolbar.dart
│   │           │   └── pdf_undo_redo_buttons.dart
│   │           ├── note_button.dart
│   │           ├── note_input_field.dart
│   │           ├── pdf_page_navigation.dart
│   │           ├── reading_book_appBar.dart
│   │           ├── search_toolbar_widget.dart
│   │           └── text_selections_toolbar.dart
│   ├── search/
│   │   ├── data/
│   │   │   ├── search_repo.dart
│   │   │   └── search_repo_impl.dart
│   │   ├── logic/
│   │   │   ├── search_cubit.dart
│   │   │   └── search_state.dart
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── search_screen.dart
│   │       └── widgets/
│   │           ├── search_body.dart
│   │           ├── search_books_list.dart
│   │           ├── search_field.dart
│   │           └── search_header_section.dart
│   ├── splash/
│   │   └── presentation/
│   │       ├── screens/
│   │       │   └── splash_screen.dart
│   │       └── widgets/
│   │           ├── splash_body.dart
│   │           └── splash_text_section.dart
│   └── welcome/
│       └── presentation/
│           ├── screens/
│           │   └── welcome_screen.dart
│           └── widgets/
│               ├── continue_button.dart
│               ├── disclaimer_title_section.dart
│               ├── footer_section.dart
│               ├── header_section.dart
│               └── welcome_body.dart
│── firebase_options.dart
│── main.dart
│── my_app.dart
