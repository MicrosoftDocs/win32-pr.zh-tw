---
title: Event-Based 通知
description: Event-Based 通知
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 操縱杆，以事件為基礎的通知
- 操縱杆，移動閾值
- 以事件為基礎的搖桿通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b50e973434d5f5706c92a22f76846ada150bfc7caf3f5ba88c3f385f7eaf84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526178"
---
# <a name="event-based-notifications"></a>Event-Based 通知

只要搖桿軸的位置值大於裝置的 *移動臨界* 值，您就可以要求系統將搖桿訊息傳送至應用程式。 移動閾值是在搖桿位置變更訊息傳送至已捕獲裝置的視窗之前，搖桿必須移動的距離。 如需詳細資訊，請參閱 [**mm \_ JOY1MOVE**](mm-joy1move.md)、 [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md)、 [**mm \_ JOY2MOVE**](mm-joy2move.md)或 [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md)。

閾值一開始為零。 您可以使用 [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) 函數來設定移動臨界值。 您可以使用 [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) 函式來取得搖桿的最小輪詢頻率。

 

 