## BSTestRunner is bootstrap3 version of HTMLTestRunner

![report](report.png)

## How to use

A TestRunner for use with the Python unit testing framework. It generates a HTML report to show the result at a glance.


For more customization options, instantiates a BSTestRunner object.
BSTestRunner is a counterpart to unittest's TextTestRunner. E.g.

'''Python3

    # create a test suite
    suite = unittest.TestSuite()
    suite.addTest(test_login.TestLogin('test_login_pass'))
    
    # output to a file
    file_path = "result.html"
    file_result= open(file_path, 'wb')
    runner = BSTestRunner.BSTestRunner(stream=file_result, title="Test BSTestRunner", description="BSTestRunner Description")
    
    # Use an external stylesheet.
    # See the Template_mixin class for more customizable options
    runner.STYLESHEET_TMPL = '<link rel="stylesheet" href="my_stylesheet.css" type="text/css">'
    
    # run the test  
    runner.run(suite)
    file_result.close()
'''




