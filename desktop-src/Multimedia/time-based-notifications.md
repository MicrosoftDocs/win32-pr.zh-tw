---
title: Time-Based 通知
description: Time-Based 通知
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 操縱杆，以時間為基礎的通知
- 以時間為基礎的搖桿通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80052d5e728a7a5b00e6177a36c30f470fe80daeafbe39a12aa4c9a883766534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688248"
---
# <a name="time-based-notifications"></a>Time-Based 通知

您可以藉由將 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)的 *fChanged* 參數設定為 **FALSE** ，並指定連續訊息之間的間隔長度，來通知作業系統將搖桿訊息定期傳送至應用程式。 若要這樣做，請在搖桿的最小和最大輪詢頻率之間指派一個值給 *uPeriod* 參數。 您可以使用 [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)函式來判斷此範圍，該函數會填入 [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)結構中的 **wPeriodMin** 和 **wPeriodMax** 成員。 如果 *uPeriod* 值超出搖桿的有效輪詢頻率範圍，則搖桿驅動程式會使用最小或最大的輪詢頻率，以較接近 *uPeriod* 的值為准。

> [!Note]  
> Windows 會在每次呼叫 **joySetCapture** 時設定計時器事件。

 

 

 