# ChatGPT, DALL·E, Stable Diffusion Telegram bot

## Table of Contents

+ [About](#about)
+ [Start](#start)
+ [ChatGPT](#chatgpt)
+ [DALL·E](#dalle)
+ [Stable Diffusion](#stablediffusion)
+ [Account and buy](#accountbuy)
+ [API tokens](#apitokens)
+ [Database](#database)
+ [How to deploy](#howtodeploy)
+ [License](#license)

## About <a name = "about"></a>
Nowadays neural networks are able to conduct a dialogue, quickly search for the information we need, answer questions, explain complex concepts and draw pictures according to words. This is Telegram bot written in Python that allows to chat with ChatGPT and generate images using DALL·E and Stable Diffusion. I think it is very comfortable to unite these neural networks in one Telegram bot.

You can look on this bot in Telegram: [@ChatGpt_Dall_E_Bot](https://t.me/ChatGPT_Dall_E_Bot)

## Start <a name = "start"></a>
When the user enters the start command, the bot sends him a welcome message stating that the user has free 3000 ChatGPT tokens, 3 DALL·E image generations and 3 Stable Diffusion image generations and displays 4 buttons: "💭Chatting — ChatGPT 3.5 Turbo", "🌄Image generation — DALL·E", "🌅Image generation — Stable Diffusion" and "👤My account | 💰Buy". If the user is already registered, the bot only displays buttons.

![ChatGPT, DALL·E, Stable Diffusion _ Telegram bot 2023-04-16 18-14-35 _online-video-cutter com_](https://user-images.githubusercontent.com/60838512/232325199-508eb8c5-4bfc-44ad-afde-d87b820fc4bb.gif)


## ChatGPT <a name = "chatgpt"></a>
If the user wants to chat with ChatGPT, he presses the "💭Chatting — ChatGPT 3.5 Turbo" button and chats.

![ChatGPT, DALL·E, Stable Diffusion _ Telegram bot 2023-04-16 18-34-00 _online-video-cutter com_](https://user-images.githubusercontent.com/60838512/232324085-8998d1e4-c075-4b72-818f-e516838c199a.gif)

In [chatgpt.py](https://github.com/vladislav-bordiug/ChatGPT_DALL_E_StableDiffusion_Telegram_Bot/blob/main/chatgpt.py) there are two parameters:

```max_tokens``` - The maximum number of tokens to generate in the chat completion.

```temperature``` - What sampling temperature to use, between 0 and 2. Higher values like 0.8 will make the output more random, while lower values like 0.2 will make it more focused and deterministic.

## DALL·E <a name = "dalle"></a>
If the user wants to generate image with DALL·E, he presses the "🌄Image generation — DALL·E" button and generates.

![ChatGPT, DALL·E, Stable Diffusion _ Telegram bot – _1_ 2023-04-16 18-47-44 _online-video-cutter com_ (1)](https://user-images.githubusercontent.com/60838512/232324731-81761500-1a5c-4bd3-a728-b8917c8dd1eb.gif)

Generated image:

![photo_2023-04-16_18-47-57](https://user-images.githubusercontent.com/60838512/232333088-8cca3d7c-81b8-4f99-81b1-f621a2759452.jpg)

In [dalle.py](https://github.com/vladislav-bordiug/ChatGPT_DALL_E_StableDiffusion_Telegram_Bot/blob/main/dalle.py) there are two parameters:

```n``` - The number of images to generate. Must be between 1 and 10.

```size``` - The size of the generated images. Must be one of 256x256, 512x512, or 1024x1024.

## Stable Diffusion <a name = "stablediffusion"></a>
If the user wants to generate image with Stable Diffusion, he presses the "🌅Image generation — Stable Diffusion" button and generates.

![ChatGPT, DALL·E, Stable Diffusion _ Telegram bot 2023-04-16 19-06-33 _online-video-cutter com_](https://user-images.githubusercontent.com/60838512/232325734-ac97a733-91ef-490e-a30f-e970358ad585.gif)

Generated image:

![image](https://user-images.githubusercontent.com/60838512/232325586-649bb911-aa0a-4a7b-9fa1-4ea544f93485.png)

In [stablediffusion.py](https://github.com/vladislav-bordiug/ChatGPT_DALL_E_StableDiffusion_Telegram_Bot/blob/main/stablediffusion.py) there are eight parameters:

```engine``` - Set the engine to use for generation. Available engines: stable-diffusion-v1, stable-diffusion-v1-5, stable-diffusion-512-v2-0, stable-diffusion-768-v2-0, stable-diffusion-512-v2-1, stable-diffusion-768-v2-1, stable-inpainting-v1-0, stable-inpainting-512-v2-0.

```seed``` - If a seed is provided, the resulting generated image will be deterministic. What this means is that as long as all generation parameters remain the same, you can always recall the same image simply by generating it again.

```steps``` - Amount of inference steps performed on image generation. Defaults to 30.

```cfg_scale``` - Influences how strongly your generation is guided to match your prompt. Setting this value higher increases the strength in which it tries to match your prompt. Defaults to 7.0 if not specified.

```width``` - Generation width, defaults to 512 if not included.

```height``` - Generation height, defaults to 512 if not included.

```samples``` - Number of images to generate, defaults to 1 if not included.

```sampler``` - Choose which sampler we want to denoise our generation with. Defaults to k_dpmpp_2m if not specified. Clip Guidance only supports ancestral samplers. (Available Samplers: ddim, plms, k_euler, k_euler_ancestral, k_heun, k_dpm_2, k_dpm_2_ancestral, k_dpmpp_2s_ancestral, k_lms, k_dpmpp_2m)

## Account and buy <a name = "accountbuy"></a>
If the user wants to see account information or buy tokens and generations, he presses the "👤My account | 💰Buy" button. After pressing the button, the bot displays information about the rest of the user's ChatGPT tokens, DALL·E image generations and Stable Diffusion image generations. If user wants to buy tokens and generations, he presses "💰Buy tokens and generations" button, selects product and currrency. After that, the user needs to press the "💰Buy" button and pay in Crypto Bot if he wants to pay. If the user has paid, he should press "☑️Check" button and tokens or image generations will be added to his account. If the user hasn't paid, the bot will display the message "⌚️We have not received payment yet".

![ChatGPT, DALL·E, Stable Diffusion _ Telegram bot 2023-04-16 19-14-29 _online-video-cutter com_](https://user-images.githubusercontent.com/60838512/232326500-dc77b158-bb4f-49b9-a7c3-f9198ae56bfb.gif)

## API tokens <a name = "apitokens"></a>

These project needs these API tokens: 

```CHAT_GPT3_API_KEY``` - OpenAI API key which you can get here: [OpenAI API key](https://platform.openai.com/account/api-keys)

```STABLE_DIFFUSION_API_KEY``` - Stable Diffusion API key which you can get here: [Stable Diffusion API key](https://beta.dreamstudio.ai/account)

```TELEGRAM_BOT_TOKEN``` - Telegram Bot API key which you can get here after creation of your bot: [@BotFather](https://t.me/BotFather)

```CRYPTOPAY_KEY``` - Crypto Bot API key which you can get here after registration in bot (Crypto Pay - Create App): [@CryptoBot](https://t.me/CryptoBot)

## Database <a name = "database"></a>

These project requires PostgreSQL database with two tables: orders(purchase_id, user_id) and users(user_id, username, chatgpt, dall_e, stable_diffusion). 

Users and information about them will be added to the "users" table, orders would be added to the "orders" table.

```DATABASE_URL``` - url to database.

## How to deploy <a name = "howtodeploy"></a>

This project was deployed on the [Railway](https://railway.app/).

For deployment you just need to create the GitHub repository, click "Start a New Project" button on the Railway website.

![image](https://user-images.githubusercontent.com/60838512/232328076-fd3f8281-e523-4b08-ade9-47cd3c7fb9ab.png)

After that you need to choose "Deploy from GitHub repo".

![image](https://user-images.githubusercontent.com/60838512/232328194-5fbfcea8-1cfd-4b4e-b484-727a3e9498be.png)

Here you need to choose your repository.

![image](https://user-images.githubusercontent.com/60838512/232328334-2db545e9-07ba-4b1b-a89a-14f0ecbbf12e.png)

After that click "add variables".

![image](https://user-images.githubusercontent.com/60838512/232328415-5d10a920-a8a6-4c11-8675-9ad5ce6fb30a.png)

Add your ptoject's variables. For example, for this project you need to add here 4 variables: CHAT_GPT3_API_KEY, CRYPTOPAY_KEY, DATABASE_URL, STABLE_DIFFUSION_API_KEY and TELEGRAM_BOT_TOKEN.

![image](https://user-images.githubusercontent.com/60838512/232328573-8cbb0eca-aca9-4fc0-8656-e303b4af90e8.png)

Return to your project and add database.

![image](https://user-images.githubusercontent.com/60838512/232328651-e02d41cc-2cd3-4b1c-ac52-a7f6312ed2cd.png)

Choose PostgreSQL.

![image](https://user-images.githubusercontent.com/60838512/232328670-25835f92-57bd-4f2b-9477-075638574454.png)

Here you need to press create tables.

![image](https://user-images.githubusercontent.com/60838512/232328709-476b146f-42e6-44ed-826f-c10762697aeb.png)

For example, tables for this project:

![image](https://github.com/vladislav-bordiug/ChatGPT_DALL_E_StableDiffusion_Telegram_Bot/assets/60838512/08cefb41-6997-434d-9a87-ed9fc4d834b5)

![image](https://user-images.githubusercontent.com/60838512/232328899-2a0dd7de-932e-45c8-8580-06e3a281fb7a.png)

Return to variables and add DATABASE_URL. All variables:

![image](https://user-images.githubusercontent.com/60838512/232329016-5961b459-e1ca-4e73-90af-7c6dddf9d24d.png)

## License <a name = "license"></a>

[License](https://github.com/vladislav-bordiug/ChatGPT_DALL_E_StableDiffusion_Telegram_Bot/blob/main/LICENSE) - this project is licensed under Apache-2.0 license.
