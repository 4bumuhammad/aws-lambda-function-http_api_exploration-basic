# &#x1F6A9; AWS Lambda Function | example API Gateway from scratch
**Function : http_api_exploration**

&nbsp;

Start by opening an AWS lambda service.
<div align="center">
    <img src="./gambar-petunjuk/ss_001_aws_lambda_function.png" alt="ss_001_aws_lambda_function" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

Fill in the basic information for the service function that will be used.
<div align="center">
    <img src="./gambar-petunjuk/ss_002_aws_lambda_create_from_scratch.png" alt="ss_002_aws_lambda_create_from_scratch" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

Define and script triggers in the service layer function.
<div align="center">
    <img src="./gambar-petunjuk/ss_003_aws_lambda_function_http_api_exploration.png" alt="ss_003_aws_lambda_function_http_api_exploration" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_004_aws_lambda_function_api_add_trigger.png" alt="ss_004_aws_lambda_function_api_add_trigger" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_005_aws_lambda_function_http_api_exploration_gateway.png" alt="ss_005_aws_lambda_function_http_api_exploration_gateway" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

Tries to run the default script by triggering the predefined trigger.
<div align="center">
    <img src="./gambar-petunjuk/ss_006_aws_lambda_run.png" alt="ss_006_aws_lambda_run" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

Make changes to the script to see the events obtained when activating the trigger.
<div align="center">
    <img src="./gambar-petunjuk/ss_007_aws_lambda_code.png" alt="ss_007_aws_lambda_code" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_008_aws_lambda_run_dumps_event.png" alt="ss_008_aws_lambda_run_dumps_event" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

Create custom scripts.
<div align="center">
    <img src="./gambar-petunjuk/ss_009_aws_lambda_custom_code.png" alt="ss_009_aws_lambda_custom_code" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<pre>
    import json

    def lambda_handler(event, context):
        # TODO implement
        result = {}
        if event['requestContext']['identity']['sourceIp'] == "45.251.5.94":
            result['recognition_status'] = "Ini adalah device Dhony Abu Muhammad."
        else:
            result['recognition_status'] = "Device tidak dikenali sebagai perangkat terdaftar."
        result['user_agent'] = event['requestContext']['identity']['userAgent']     
        return {
            'statusCode': 200,
            'body': json.dumps(result)
        }
</pre>

&nbsp;

&#x1F525; **Result :**
<div align="center">
    <img src="./gambar-petunjuk/ss_010_aws_lambda_function_http_api_exploration_response.png" alt="ss_010_aws_lambda_function_http_api_exploration_response" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

&nbsp;

&nbsp;

---

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_011_aws_lambda_functions.png" alt="ss_011_aws_lambda_functions" style="display: block; margin: 0 auto;">
</div>

&nbsp;

---

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/well_done.png" alt="well_done" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

---

&nbsp;

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/syukron.png" alt="syukron" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

&nbsp;
