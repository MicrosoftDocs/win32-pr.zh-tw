---
description: 計時或重複事件是在某個特定時間和日期發生的事件，或定期重複發生的事件。 例如，事件可能會在2015年12月2日的午夜發生，或在星期二下午2:31 點發生一次。
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: 接收計時或重複事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45808d9d43ddc7b5370b129e29a4fc268fe09856013599c70bb65187a1c0b918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817474"
---
# <a name="receiving-a-timed-or-repeating-event"></a>接收計時或重複事件

計時或重複事件是在某個特定時間和日期發生的事件，或定期重複發生的事件。 例如，事件可能會在2015年12月2日的午夜發生，或在星期二下午2:31 點發生一次。

下表列出用來建立計時或重複事件的不同類別。



| 類別                                                                                            | 描述                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)或 [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | 標準 Microsoft 事件模型。<br/> 如需詳細資訊，請參閱 [使用 win32 \_ LocalTime 或 Win32 \_ UTCTime 建立計時器事件](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)。<br/> |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                               | 舊版技術。<br/> 如需詳細資訊，請參閱 [使用 \_ TimerInstruction 建立計時器事件](creating-a-timer-event-with---timerinstruction.md)。<br/>                                             |



 

如果您想要將工作或工作排程在特定時間或重複執行，請使用 [**Win32 \_ register-scheduledjob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) 類別和其方法。 此類別代表在命令視窗中使用 AT 命令建立的作業，從 **開始** 然後 **執行**，或從 **主控台** 中的 **排程** 工作。

 

