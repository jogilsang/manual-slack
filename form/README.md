

###
```
https://app.slack.com/block-kit-builder
```

### 메세지 형식1
```
                // msg = {
                        //     "response_type": "in_channel",
                        //     "attachments": [
                        //         {
                        //             "color": "#50BCDF",
                        //             "blocks": [
                        //                 {
                        //                     "type": "header",
                        //                     "text": {
                        //                         "type": "plain_text",
                        //                         "text": "Task 이슈가 생성됬습니다",
                        //                         "emoji": true
                        //                     }
                        //                 },
                        //                 {
                        //                     "type": "divider"
                        //                 },
                        //                 {
                        //                     "type": "section",
                        //                     "text": {
                        //                         "type": "mrkdwn",
                        //                         "text": resultTitle
                        //                     }
                        //                 },
                        //                 {
                        //                     "type": "section",
                        //                     "text": {
                        //                         "type": "mrkdwn",
                        //                         "text": resultLink
                        //                     }
                        //                 }
                        //             ]
                        //         }
                        //     ]
                        // }
```

### 메세지 형식2
```
             // 단위테스트 또는 통합테스트
                        msg = {
                            "response_type": "in_channel",
                            "attachments": [
                                {
                                    "fallback": "Task(Issue) has been created.",
                                    "pretext": "Task(Issue) has been created.",
                                    "color": colorList[issuetype],
                                    "fields": [
                                        {
                                            "title": resultTitle,
                                            "value": resultLink,
                                            "short": false
                                        }
                                    ]
                                }
                            ]
                        };
```
