---
title: 搖桿通知
description: 搖桿通知
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 捕捉的搖桿
- 未插的操縱杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86666645a4589d1ecd638b81541aab2954839ca08889ef567b69f4abda17d211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140325"
---
# <a name="joystick-notifications"></a>搖桿通知

您可以使用 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) 函式來捕捉要傳送至函式的直接搖桿訊息。 一次只有一個應用程式可以從搖桿捕捉訊息，但您可以使用 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 或 [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) 函式，從另一個應用程式查詢搖桿。

> [!Note]  
> 如果第二個應用程式使用 **joyGetPos** 或 **joyGetPosEx** 來查詢搖桿（大約是傳送訊息的相同時間），則搖桿訊息可能無法連線到捕捉搖桿的應用程式。 在此情況下，第二個應用程式可能會攔截訊息。

 

如果您想要從連接到系統的兩個操縱杆中捕捉訊息，請針對每個搖桿使用 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) 兩次。 您的視窗會針對每個裝置接收不同的不同訊息。

您可以使用 [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) 函式來釋放已捕捉的搖桿。 如果應用程式未在結束之前釋出遊戲杆，則會在「捕獲視窗」終結後立即自動釋出遊戲杆。

您無法抓取未插的搖桿。 如果未插上指定的裝置， **joySetCapture** 函式會傳回 JOYERR \_ 插即用。

 

 