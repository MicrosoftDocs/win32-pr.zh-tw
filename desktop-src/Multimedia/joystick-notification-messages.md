---
title: 搖桿通知訊息
description: 搖桿通知訊息
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 操縱杆、位置
- 操縱杆，按鈕
- MM_JOY1 訊息
- MM_JOY2 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27113adeb6f9fd4444f8fc30431df0eab686db667fa2674e81d7f5d4e568be64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140338"
---
# <a name="joystick-notification-messages"></a>搖桿通知訊息

操縱杆訊息會通知您的應用程式，搖桿已變更位置或其中一個按鈕的狀態已變更。 \_如果您的應用程式使用識別碼 JOYSTICKID1 從搖桿要求輸入，則會將以 MM JOY1 開頭的訊息傳送至函式，而 \_ 如果您的應用程式使用識別碼 JOYSTICKID2 從搖桿要求輸入，則會傳送 mm JOY2 訊息。

下表中的訊息會識別搖桿按鈕的狀態：



| 訊息                                         | 描述                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md) | 已按下游戲杆 JOYSTICKID1 上的按鈕。              |
| [**MM \_ JOY1BUTTONUP**](mm-joy1buttonup.md)     | 已釋放搖桿 JOYSTICKID1 上的按鈕。             |
| [**MM \_ JOY1MOVE**](mm-joy1move.md)             | 操縱杆 JOYSTICKID1 已變更 x 或 y 方向的位置。 |
| [**MM \_ JOY1ZMOVE**](mm-joy1zmove.md)           | 操縱杆 JOYSTICKID1 以 z 方向變更位置。       |
| [**MM \_ JOY2BUTTONDOWN**](mm-joy2buttondown.md) | 已按下游戲杆 JOYSTICKID2 上的按鈕。              |
| [**MM \_ JOY2BUTTONUP**](mm-joy2buttonup.md)     | 已釋放搖桿 JOYSTICKID2 上的按鈕。             |
| [**MM \_ JOY2MOVE**](mm-joy2move.md)             | 操縱杆 JOYSTICKID2 已變更 x 或 y 方向的位置  |
| [**MM \_ JOY2ZMOVE**](mm-joy2zmove.md)           | 操縱杆 JOYSTICKID2 以 z 方向變更位置。       |



 

所有訊息都會將不存在的按鈕報告為已發行。

 

 




