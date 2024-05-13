### SystemReady-IR-Workshop

##### Environment Setup

```
sudo apt update
sudo apt upgrade
sudo apt install ccache wget libopenblas-dev
```

##### Demo-0


##### Demo-1

- build llama.cpp

```
wget https://huggingface.co/Qwen/Qwen1.5-1.8B-Chat-GGUF/resolve/main/qwen1_5-1_8b-chat-q5_k_m.gguf
git clone https://github.com/ggerganov/llama.cpp.git
cd llama.cpp
make LLAMA_OPENBLAS=1 -j4
```

- prompt measurement using llama.cpp main example

```
sudo taskset -c 4,5,6,7 ./main -m ../qwen1_5-1_8b-chat-q5_k_m.gguf -f prompts/chat-with-qwen.txt -c 2048 -n 512 --color -cml --ignore-eos
```

- build mnn-llm

```
git clone https://github.com/ownia/mnn-llm.git -b workshop
cd mnn-llm
./script/build.sh
```

- prompt measurement using mnn-llm cli_demo

```
./script/download_model.sh qwen1.5-1.8b-chat
# ./script/download_model.sh qwen1.5-4b-chat
# ./script/download_model.sh qwen1.5-7b-chat
./build/cli_demo qwen1.5-1.8b-chat resource/workshop_prompt_0
./build/cli_demo qwen1.5-1.8b-chat resource/workshop_prompt_1
```


##### Demo-2



##### Backup

```
2.5G    qwen1.5-1.8b-chat
3.2G    qwen1.5-4b-chat
4.5G    qwen1.5-7b-chat
```
