---
description: 您可以建立一個計時器事件，方法是 \_ \_ 在任何 WMI 命名空間中建立衍生自 TimerInstruction 類別的類別實例。
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: 使用 __TimerInstruction 建立計時器事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb943419a255846fbde4e17e357f8ce199824085d542d8ad300fb7e301fa3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030668"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>使用 TimerInstruction 建立計時器事件 \_ \_

您可以建立一個計時器事件，方法是在任何 WMI 命名空間中建立衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)類別的類別實例。 WMI 接著會在適當的時間產生計時器事件。 如果您因為電腦停機而錯過了計時器事件，WMI 會通知您遺漏的事件。 WMI 支援計時器事件以提供回溯相容性，以及適用于您必須知道自從上一個傳遞事件以來已錯過多少事件的情況。 但是針對大部分的計時器事件，您應該建立 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 或 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)的事件篩選。 如需詳細資訊，請參閱 [使用 win32 \_ LocalTime 或 Win32 \_ UTCTime 建立計時器事件](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)。

下列程式描述如何使用 TimerInstruction 建立及接收計時器事件 \_ \_ 。

**使用 TimerInstruction 建立和接收計時器事件 \_ \_**

1.  建立 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)或 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)類別的實例。

    [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)和 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)類別衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)類別，該類別包含唯一的開發人員指派的字串，可識別計時器事件的類型。 **\_ \_ TimerInstruction** 類別也包含一個值，這個值會指定當 wmi 無法使用時，wmi 是否應該傳送 belated 通知。

    使用 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)來傳送絕對計時器事件，此事件會在特定時間于特定日期發生。 使用 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)傳送間隔計時器事件，這會定期發生。

2.  設定您的應用程式以接收 [**\_ \_ TimerEvent**](--timerevent.md)實例。

    為了產生事件，WMI 會建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例，並將實例轉送至您的取用者。 **\_ \_ TimerEvent** 實例包含取用者的計時器指令識別碼。 此實例也包含值，指定 wmi 無法觸達取用者時，WMI 應該在任何間隔期間傳送計時器事件通知的次數。

 

 
