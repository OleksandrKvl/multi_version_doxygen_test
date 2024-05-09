find_package(Doxygen REQUIRED)

if(MVDT_OVERRIDE_DOCS_DIR)
    set(DOXYGEN_HTML_OUTPUT "${MVDT_OVERRIDE_DOCS_DIR}")
else()
    set(DOXYGEN_HTML_OUTPUT "${PROJECT_VERSION}")
endif()

set(DOXYGEN_OUTPUT_DIRECTORY "docs")
set(DOXYGEN_HTML_HEADER "header.html")
set(DOXYGEN_HTML_EXTRA_FILES "version_selector_handler.js")

doxygen_add_docs(
    doc
    "${PROJECT_SOURCE_DIR}"
)