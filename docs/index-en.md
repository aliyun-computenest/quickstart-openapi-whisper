<h1>OpenAI Whisper Compute Nest Deployment and Usage Documentation</h1>

<h2>Overview</h2>

<p>Using Compute Nest, you can deploy Whisper with a single click in seconds, immediately starting your AIGC journey. Without Compute Nest, you might spend hours or even longer on environment preparation and service deployment. Based on Compute Nest, you can significantly improve your work efficiency and focus your energy on business logic.</p>

<p>OpenAI, the company behind the ChatGPT language model, has open-sourced the Whisper automatic speech recognition system. OpenAI emphasizes that Whisper's speech recognition capabilities have reached human-level performance.</p>

<p>Whisper is a general-purpose speech recognition model trained on a large dataset of multilingual and multitask supervised data. It achieves robustness and accuracy close to human levels in English speech recognition. Whisper can also perform tasks such as multilingual speech recognition, speech translation, and language identification. Whisper's architecture is a simple end-to-end approach, employing an encoder-decoder Transformer model that converts input audio into corresponding text sequences and specifies different tasks based on special tokens.</p>

<h2>Instance Description</h2>

<p>The Whisper deployment is the community open-source version. For source code, please refer to the <a href="https://huggingface.co/spaces/sanchit-gandhi/whisper-large-v2/tree/main" target="_blank">Hugging Face Repo</a>. Currently available instance specifications are as follows:</p>

<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th>Instance Family</th>
            <th>vCPU & Memory</th>
            <th>System Disk</th>
            <th>GPU/FPGA</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ecs.gn7i-c16g1.4xlarge</td>
            <td>16 vCPU 60 GiB</td>
            <td>200G</td>
            <td>1 * NVIDIA A10 (24G)</td>
        </tr>
        <tr>
            <td>ecs.gn7i-c32g1.8xlarge</td>
            <td>32 vCPU 188 GiB</td>
            <td>200G</td>
            <td>1 * NVIDIA A10 (24G)</td>
        </tr>
        <tr>
            <td>ecs.gn7i-c32g1.16xlarge</td>
            <td>64 vCPU 376 GiB</td>
            <td>200G</td>
            <td>2 * NVIDIA A10 (24G)</td>
        </tr>
        <tr>
            <td>ecs.gn7i-c32g1.32xlarge</td>
            <td>128 vCPU 752 GiB</td>
            <td>200G</td>
            <td>4 * NVIDIA A10 (24G)</td>
        </tr>
    </tbody>
</table>

<h2>Deployment Process</h2>

<h3>0. Preparation</h3>

<p>Before formally using the service, you need an Alibaba Cloud account to access and create resources such as ECS and VPC.</p>

<ul>
    <li>If you are using a personal account, you can create service instances directly.</li>
    <li>If you are using a RAM user to create service instances, and it is your first time using Alibaba Cloud Compute Nest:
        <ul>
            <li>You need to add permissions for the corresponding resources to the RAM user account before creating the service instance. For detailed operations on adding RAM permissions, please refer to <a href="https://help.aliyun.com/document_detail/121945.html" target="_blank">Authorize RAM Users</a>.</li>
            <li>You also need to authorize the creation of associated roles. Refer to the figure below and select <strong>Agree to Authorize and Create Associated Role</strong>.</li>
        </ul>
    </li>
</ul>

<h3>1. Deployment Entry</h3>

<p>You can search for it yourself in Alibaba Cloud Compute Nest, or quickly reach it via the deployment link below:<br>
<a href="https://computenest.console.aliyun.com/vendor/cn-hangzhou/serviceDetail/service-51e7e7bf804d44d4bcd0/1" target="_blank">Deployment Link</a></p>

<h3>2. Create Whisper Service Instance</h3>

<h4>2.1 Parameter List</h4>

<p>During the process of creating a service instance, you need to configure the parameter list for the service instance information, as detailed below:</p>

<h4>2.2 Specific Steps</h4>

<p>Create the service by following the steps below, referring to the figures:</p>

<ol>
    <li>Create an instance name.</li>
    <li>Select the region, such as "China (Hangzhou)" in the figure below.</li>
    <li>Select the billing method: "Pay-As-You-Go" or "Subscription".</li>
    <li>Select the instance type and configure the instance password.</li>
    <li>Enter the software login username and password.</li>
    <li>Click the "Next: Confirm Order" button to enter the order confirmation page.</li>
    <li>Check the checkbox in the "Terms of Service".</li>
    <li>Click the "Create Now" button to create the Whisper service instance.</li>
</ol>

<h3>3. Start Whisper Service</h3>

<p><strong>View Service Instance:</strong> After the service instance is successfully created, the deployment takes approximately 5 minutes. Wait for the service instance status to change to "Deployed", then click the "Details" button to enter the service instance details page, as shown in the figure below:</p>

<p>After entering the service instance, you can obtain the "Login Address" on the page:</p>

<p>Click the login address, enter the software username and password configured during service instance creation, and you can access the deployed Whisper Web page. It is recommended that beginners start by using the demo features via the Whisper Web interface to get started quickly:</p>

<p>Users can upload audio files and click "Transcribe" to convert the audio into text.</p>

<h3>More Examples</h3>

<p>For more features, please refer to: <a href="https://github.com/openai/whisper" target="_blank">Whisper Usage Documentation</a></p>

<p>We look forward to your deeper exploration and welcome you to practice and supplement corresponding cases to this document.</p>
