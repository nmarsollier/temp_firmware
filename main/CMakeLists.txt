# main component — sources and REQUIRES grouped by module.
idf_component_register(
        SRCS
        "main.c"

        "i2c_bus/i2c_bus.c"

        "accelerometer/accelerometer_init.c"
        "accelerometer/accelerometer_read.c"

        "sht31/sht31_init.c"
        "sht31/sht31_read.c"

        "environment/environment.c"
        "vibration/vibration.c"

        "usb_cdc/usb_cdc_init.c"
        "usb_cdc/usb_cdc_rx.c"
        "usb_cdc/usb_cdc_tx.c"

        "proto/proto_init.c"
        "proto/proto_frame.c"
        "proto/proto_json.c"
        "proto/proto_dispatch.c"
        "proto/proto_session.c"
        "proto/proto_capabilities.c"
        "proto/proto_state.c"
        "proto/proto_action.c"
        "proto/proto_config.c"
        "proto/proto_control.c"

        "runtime/runtime_setup.c"
        "runtime/runtime_loop.c"

        INCLUDE_DIRS
        "."
        "config"
        "i2c_bus"
        "accelerometer"
        "sht31"
        "environment"
        "vibration"
        "usb_cdc"
        "proto"
        "runtime"

        REQUIRES
        esp_timer
        nvs_flash
        esp_driver_i2c
)
