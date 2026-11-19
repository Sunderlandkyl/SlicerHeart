slicer_add_python_unittest(SCRIPT Converter4DSequencesTest.py)
# These tests take several minutes, and much longer on a slow computer that runs other tests at the same time:
# allow more time than the default timeout of the dashboards.
set_tests_properties(py_Converter4DSequencesTest PROPERTIES TIMEOUT 3600)
