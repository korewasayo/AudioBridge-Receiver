cmake_minimum_required(VERSION 3.20)
project(AudioBridge_Receiver VERSION 1.0.0)

# Tell me where the JUCE folder is located on your PC.
add_subdirectory("C:/Dev/JUCE" juce)

# Create the application (This would be your Transmitter or Receiver)
juce_add_gui_app(AudioBridge_RX
    PRODUCT_NAME "AudioBridge RX"
    VERSION 1.0.0)

juce_generate_juce_header(AudioBridge_RX)

# Add the source code that you will write
target_sources(AudioBridge_RX PRIVATE
    Main.cpp)

# Link the JUCE modules you need (Audio and GUI)
target_link_libraries(AudioBridge_RX PRIVATE
    juce::juce_audio_utils
    juce::juce_gui_extra)

