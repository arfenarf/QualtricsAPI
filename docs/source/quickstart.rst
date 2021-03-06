Quick Start
==========================

There are 3 IDs that Qualtrics users use to access to their Qualtrics account via the API. These IDs can all be found
by logging into your Qualtrics account, and navigating to your account settings page. Once on the account setting's
page click on the Qualtrics IDs tab.

Finding Qualtrics API Credentials
#################################

On this page you will be able to generate an API token specific to your user account. This token is the first ID
that will be needed to use the Qualtrics API. The second ID that you will need is your directory id. This can also
be found on the same page and should begin with a 'POOL' at the beginning. The final ID can be found in the url,
it will follow either the (yourorganizationid.yourdatacenter.qualtrics.com) or (yourdatacenter.qualtrics.com)
In either case you want to use the yourdatacenter portion as your datacenter ID. If you are struggling to
find one of these IDs check out `Qualtrics - Finding Your Qualtrics IDs Guide <https://api.qualtrics.com/docs/finding-your-qualtrics-ids>`_


.. autoclass:: QualtricsAPI.Setup.credentials.Credentials
    :members: qualtrics_api_credentials

Example Implementation
----------------------

Here is an example on how to implement the qualtrics_api_credentials() method.
::

    from QualtricsAPI.Setup import Credentials

    #Create an instance of Credentials
    c = Credentials()

    #Call the qualtrics_api_credentials() method
    c.qualtrics_api_credentials(token='Your API Token',data_center='Your Data Center',directory_id='Your Directory ID')
