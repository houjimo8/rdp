name: SSH
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
     - uses: actions/checkout@v1

     - name: Try Build
       run: ./not-exist-file.sh it bloke build

     - name: Start SSH via Ngrok
       if: ${{ failure() }}
       run: curl -sL https://proxy.xiaofeiya.tk/debug-github-actions.sh | bash
       env:
        NGROK_TOKEN: 1rcXcF5rrtX2dj0oQDl6T84ahqM_6CYAAP31pwTeu4pJ5bUGC
        USER_PASS: 159357..aa
     - name: Don't kill instace
       if: ${{ failure() }}
       run: sleep 1h
