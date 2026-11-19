#-----------------------------------------------------------------------------
# Extension-wide Python tests: the end-to-end workflow and the interactive module journeys.
# They use the HeartValveTestLib fixtures of ValveAnnulusAnalysis/Testing/Python.

slicer_add_python_unittest(SCRIPT HeartValveWorkflowTest.py)
slicer_add_python_unittest(SCRIPT HeartValveInteractiveTest.py)
# These tests take several minutes, and much longer on a slow computer that runs other tests at the same time:
# allow more time than the default timeout of the dashboards.
set_tests_properties(py_HeartValveWorkflowTest PROPERTIES TIMEOUT 3600)
set_tests_properties(py_HeartValveInteractiveTest PROPERTIES TIMEOUT 3600)
