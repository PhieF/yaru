sassc = find_program('sassc')

gtk3_dir = join_paths(theme_dir, 'gtk-3.0')
gtk3_asset_dir = join_paths(gtk3_dir, 'assets')

# theme sources .scss files
gtk3_scss_sources = [
  'gtk-dark',   # applications requesting dark theme when using the light one.
  'gtk',
]


# Dependencies of the files that need to be compiled
gtk3_scss_dependencies = [
  '_colors-public.scss',
  '_ubuntu-colors.scss',
  '_colors.scss',
  '_common.scss',
  '_drawing.scss',
]

gtk3_assets = [
  'assets/checkbox-active-selectionmode@2.png',
  'assets/checkbox-active-selectionmode.png',
  'assets/checkbox-backdrop-selectionmode@2.png',
  'assets/checkbox-backdrop-selectionmode.png',
  'assets/checkbox-checked@2.png',
  'assets/checkbox-checked-active@2.png',
  'assets/checkbox-checked-active.png',
  'assets/checkbox-checked-active-selectionmode@2.png',
  'assets/checkbox-checked-active-selectionmode.png',
  'assets/checkbox-checked-backdrop@2.png',
  'assets/checkbox-checked-backdrop-insensitive@2.png',
  'assets/checkbox-checked-backdrop-insensitive.png',
  'assets/checkbox-checked-backdrop.png',
  'assets/checkbox-checked-backdrop-selectionmode@2.png',
  'assets/checkbox-checked-backdrop-selectionmode.png',
  'assets/checkbox-checked-hover@2.png',
  'assets/checkbox-checked-hover.png',
  'assets/checkbox-checked-hover-selectionmode@2.png',
  'assets/checkbox-checked-hover-selectionmode.png',
  'assets/checkbox-checked-insensitive@2.png',
  'assets/checkbox-checked-insensitive.png',
  'assets/checkbox-checked.png',
  'assets/checkbox-checked-selectionmode@2.png',
  'assets/checkbox-checked-selectionmode.png',
  'assets/checkbox-hover-selectionmode@2.png',
  'assets/checkbox-hover-selectionmode.png',
  'assets/checkbox-mixed@2.png',
  'assets/checkbox-mixed-active@2.png',
  'assets/checkbox-mixed-active.png',
  'assets/checkbox-mixed-backdrop@2.png',
  'assets/checkbox-mixed-backdrop-insensitive@2.png',
  'assets/checkbox-mixed-backdrop-insensitive.png',
  'assets/checkbox-mixed-backdrop.png',
  'assets/checkbox-mixed-hover@2.png',
  'assets/checkbox-mixed-hover.png',
  'assets/checkbox-mixed-insensitive@2.png',
  'assets/checkbox-mixed-insensitive.png',
  'assets/checkbox-mixed.png',
  'assets/checkbox-selectionmode@2.png',
  'assets/checkbox-selectionmode.png',
  'assets/checkbox-unchecked@2.png',
  'assets/checkbox-unchecked-active@2.png',
  'assets/checkbox-unchecked-active.png',
  'assets/checkbox-unchecked-backdrop@2.png',
  'assets/checkbox-unchecked-backdrop-insensitive@2.png',
  'assets/checkbox-unchecked-backdrop-insensitive.png',
  'assets/checkbox-unchecked-backdrop.png',
  'assets/checkbox-unchecked-hover@2.png',
  'assets/checkbox-unchecked-hover.png',
  'assets/checkbox-unchecked-insensitive@2.png',
  'assets/checkbox-unchecked-insensitive.png',
  'assets/checkbox-unchecked.png',
  'assets/radio-checked@2.png',
  'assets/radio-checked-active@2.png',
  'assets/radio-checked-active.png',
  'assets/radio-checked-backdrop@2.png',
  'assets/radio-checked-backdrop-insensitive@2.png',
  'assets/radio-checked-backdrop-insensitive.png',
  'assets/radio-checked-backdrop.png',
  'assets/radio-checked-hover@2.png',
  'assets/radio-checked-hover.png',
  'assets/radio-checked-insensitive@2.png',
  'assets/radio-checked-insensitive.png',
  'assets/radio-checked.png',
  'assets/radio-mixed@2.png',
  'assets/radio-mixed-active@2.png',
  'assets/radio-mixed-active.png',
  'assets/radio-mixed-backdrop@2.png',
  'assets/radio-mixed-backdrop-insensitive@2.png',
  'assets/radio-mixed-backdrop-insensitive.png',
  'assets/radio-mixed-backdrop.png',
  'assets/radio-mixed-hover@2.png',
  'assets/radio-mixed-hover.png',
  'assets/radio-mixed-insensitive@2.png',
  'assets/radio-mixed-insensitive.png',
  'assets/radio-mixed.png',
  'assets/radio-unchecked@2.png',
  'assets/radio-unchecked-active@2.png',
  'assets/radio-unchecked-active.png',
  'assets/radio-unchecked-backdrop@2.png',
  'assets/radio-unchecked-backdrop-insensitive@2.png',
  'assets/radio-unchecked-backdrop-insensitive.png',
  'assets/radio-unchecked-backdrop.png',
  'assets/radio-unchecked-hover@2.png',
  'assets/radio-unchecked-hover.png',
  'assets/radio-unchecked-insensitive@2.png',
  'assets/radio-unchecked-insensitive.png',
  'assets/radio-unchecked.png',
  'assets/slider-horz-scale-has-marks-above@2.png',
  'assets/slider-horz-scale-has-marks-above-active@2.png',
  'assets/slider-horz-scale-has-marks-above-active.png',
  'assets/slider-horz-scale-has-marks-above-backdrop@2.png',
  'assets/slider-horz-scale-has-marks-above-backdrop-insensitive@2.png',
  'assets/slider-horz-scale-has-marks-above-backdrop-insensitive.png',
  'assets/slider-horz-scale-has-marks-above-backdrop.png',
  'assets/slider-horz-scale-has-marks-above-hover@2.png',
  'assets/slider-horz-scale-has-marks-above-hover.png',
  'assets/slider-horz-scale-has-marks-above-insensitive@2.png',
  'assets/slider-horz-scale-has-marks-above-insensitive.png',
  'assets/slider-horz-scale-has-marks-above.png',
  'assets/slider-horz-scale-has-marks-below@2.png',
  'assets/slider-horz-scale-has-marks-below-active@2.png',
  'assets/slider-horz-scale-has-marks-below-active.png',
  'assets/slider-horz-scale-has-marks-below-backdrop@2.png',
  'assets/slider-horz-scale-has-marks-below-backdrop-insensitive@2.png',
  'assets/slider-horz-scale-has-marks-below-backdrop-insensitive.png',
  'assets/slider-horz-scale-has-marks-below-backdrop.png',
  'assets/slider-horz-scale-has-marks-below-hover@2.png',
  'assets/slider-horz-scale-has-marks-below-hover.png',
  'assets/slider-horz-scale-has-marks-below-insensitive@2.png',
  'assets/slider-horz-scale-has-marks-below-insensitive.png',
  'assets/slider-horz-scale-has-marks-below.png',
  'assets/slider-vert-scale-has-marks-above@2.png',
  'assets/slider-vert-scale-has-marks-above-active@2.png',
  'assets/slider-vert-scale-has-marks-above-active.png',
  'assets/slider-vert-scale-has-marks-above-backdrop@2.png',
  'assets/slider-vert-scale-has-marks-above-backdrop-insensitive@2.png',
  'assets/slider-vert-scale-has-marks-above-backdrop-insensitive.png',
  'assets/slider-vert-scale-has-marks-above-backdrop.png',
  'assets/slider-vert-scale-has-marks-above-hover@2.png',
  'assets/slider-vert-scale-has-marks-above-hover.png',
  'assets/slider-vert-scale-has-marks-above-insensitive@2.png',
  'assets/slider-vert-scale-has-marks-above-insensitive.png',
  'assets/slider-vert-scale-has-marks-above.png',
  'assets/slider-vert-scale-has-marks-below@2.png',
  'assets/slider-vert-scale-has-marks-below-active@2.png',
  'assets/slider-vert-scale-has-marks-below-active.png',
  'assets/slider-vert-scale-has-marks-below-backdrop@2.png',
  'assets/slider-vert-scale-has-marks-below-backdrop-insensitive@2.png',
  'assets/slider-vert-scale-has-marks-below-backdrop-insensitive.png',
  'assets/slider-vert-scale-has-marks-below-backdrop.png',
  'assets/slider-vert-scale-has-marks-below-hover@2.png',
  'assets/slider-vert-scale-has-marks-below-hover.png',
  'assets/slider-vert-scale-has-marks-below-insensitive@2.png',
  'assets/slider-vert-scale-has-marks-below-insensitive.png',
  'assets/slider-vert-scale-has-marks-below.png',
  'assets/text-select-end@2.png',
  'assets/text-select-end-active@2.png',
  'assets/text-select-end-active.png',
  'assets/text-select-end-hover@2.png',
  'assets/text-select-end-hover.png',
  'assets/text-select-end.png',
  'assets/text-select-start@2.png',
  'assets/text-select-start-active@2.png',
  'assets/text-select-start-active.png',
  'assets/text-select-start-hover@2.png',
  'assets/text-select-start-hover.png',
  'assets/text-select-start.png',
]

# generate .css files
# and install to themes/THEMENAME/gtk-3.0
foreach f : gtk3_scss_sources
  custom_target('generate_' + f + '_3_0',
      input: f + '.scss',
      output: f + '.css',
      depend_files: files(gtk3_scss_dependencies),
      command: [sassc, '-a', '@INPUT@', '@OUTPUT@'],
      build_by_default: true,
      install: true,
      install_dir: gtk3_dir,
  )
endforeach

# Install asset files to themes/THEMENAME/gtk-3.0/assets
install_data(gtk3_assets, install_dir: gtk3_asset_dir)
