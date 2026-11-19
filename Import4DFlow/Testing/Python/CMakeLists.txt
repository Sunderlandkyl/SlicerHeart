# Feature tests (they write a markdown report with screenshots, see FlowTestingUtils.py).
# The anonymized clinical data set test is skipped if MRI_4D_FLOW_TEST_DATA is not set.
slicer_add_python_unittest(SCRIPT Import4DFlowFeaturesTest.py)
# The test takes several minutes, and much longer on a slow computer that runs other tests at the same time:
# allow more time than the default timeout of the dashboards.
set_tests_properties(py_Import4DFlowFeaturesTest PROPERTIES TIMEOUT 3600)
