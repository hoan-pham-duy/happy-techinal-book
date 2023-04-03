** Lambda:
1. Run Lambda in each seconds (<1 minute): https://aws.amazon.com/vi/blogs/architecture/a-serverless-solution-for-invoking-aws-lambda-at-a-sub-minute-frequency/
https://aws.amazon.com/vi/blogs/architecture/a-serverless-solution-for-invoking-aws-lambda-at-a-sub-minute-frequency/
2. Lambda Code signing: Lambda checks every code deployment and verifies that the code package is signed by a trusted source. (ex. AWS signer to create signing profiles, which IAM can sign code package) https://docs.aws.amazon.com/lambda/latest/dg/configuration-codesigning.html?icmpid=docs_lambda_help
3. Lambda enable function URL: create A function URL is a dedicated HTTP(S) endpoint for your function, can secure via IAM, JWT/OIDC/OAuth2 authentication methods or None
Can configure CORS also
4. INVOKE MODE: BUFFERED, RESPONSE_STREAM 
