################################################################################

add_executable(benchgates.exe benchgates.cpp)
target_link_libraries(benchgates.exe PRIVATE iqs)

add_executable(grover_4qubit.exe grover_4qubit.cpp)
target_link_libraries(grover_4qubit.exe PRIVATE iqs)

add_executable(quantum_fourier_transform.exe quantum_fourier_transform.cpp)
target_link_libraries(quantum_fourier_transform.exe iqs)

add_executable(expect_value_test.exe expect_value_test.cpp)
target_link_libraries(expect_value_test.exe iqs)

add_executable(heisenberg_dynamics.exe heisenberg_dynamics.cpp)
target_link_libraries(heisenberg_dynamics.exe iqs)

add_executable(circuit_with_noise_gates.exe circuit_with_noise_gates.cpp)
target_link_libraries(circuit_with_noise_gates.exe iqs)

add_executable(noise_via_chi_matrix.exe noise_via_chi_matrix.cpp)
target_link_libraries(noise_via_chi_matrix.exe iqs)

add_executable(test_of_custom_gates.exe test_of_custom_gates.cpp)
target_link_libraries(test_of_custom_gates.exe iqs)

add_executable(communication_reduction_via_qubit_reordering.exe communication_reduction_via_qubit_reordering.cpp)
target_link_libraries(communication_reduction_via_qubit_reordering.exe iqs)

################################################################################

set_target_properties( benchgates.exe
                       quantum_fourier_transform.exe
                       grover_4qubit.exe
                       expect_value_test.exe
                       heisenberg_dynamics.exe
                       circuit_with_noise_gates.exe
                       noise_via_chi_matrix.exe
                       test_of_custom_gates.exe
                       communication_reduction_via_qubit_reordering.exe
    PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/bin"
)

################################################################################
