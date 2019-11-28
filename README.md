# v2hero  [![Build Status](https://travis-ci.org/onplus/v2hero.svg?branch=core-3.1)](https://travis-ci.org/onplus/v2hero)
本项目是一个利用Travis-CI部署Docker到Heroku 的学习示例。

如果为您的学习提供了帮助，欢迎给一个Star ^_^
* 快捷部署
   [![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/erdcy/v2hero/tree/core-latest)
* 部署方法
   https://github.com/onplus/v2hero/wiki/Deploy-V2ray-To-Heroku

## 建议使用heroku.yml部署  https://github.com/wangyi2005/v2ray-heroku
 
* 提问&建议
   https://github.com/onplus/v2hero/issues
   发起issue前请尽量先使用文档和搜索

* 相关项目
   https://wsss.herokuapp.com/

* 实现参考 
   - https://github.com/v2ray/v2ray-core
   - https://github.com/wangyi2005/v2ray
   - Heroku https://devcenter.heroku.com/articles/container-registry-and-runtime
   - Travis-CI https://docs.travis-ci.com/user/docker
## 配置
"outbound": {
    "tag": "agentout",
    "protocol": "vmess",
    "settings": {
      "vnext": [
        {
          "address": "v2hero.herokuapp.com",
          "port": 80,
          "users": [
            {
              "id": "91cb66ba-a373-43a0-8169-33d4eeaeb857",
              "alterId": 64,
              "security": "aes-128-gcm"
            }
          ]
        }
      ]
    },
    "streamSettings": {
      "network": "ws",
      "security": "",
      "tcpSettings": null,
      "kcpSettings": null,
      "wsSettings": {
        "connectionReuse": true,
        "path": "",
        "headers": null
      }
    },
    "mux": {
      "enabled": true
    }
  },

