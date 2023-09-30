set(headers
    minimp3.h
    minimp3_ex.h
)

idf_component_register(
    INCLUDE_DIRS
        .
    SRCS
        ${headers}
)

target_compile_options(${COMPONENT_TARGET}
    PRIVATE
        -fstack-reuse=all
        -fstack-protector-all
        -Wno-unused-function
        -Wno-deprecated-declarations
        -Wno-missing-field-initializers
        -Wno-parentheses
)



