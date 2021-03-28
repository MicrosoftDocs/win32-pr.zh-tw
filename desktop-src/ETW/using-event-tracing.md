---
description: 下列主題描述如何使用 ETW API 進行事件追蹤。
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: 使用事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191609"
---
# <a name="using-event-tracing"></a>使用事件追蹤

下列主題描述如何使用 ETW API 進行事件追蹤。



| 主題                                                                          | 描述                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [控制事件追蹤會話](controlling-event-tracing-sessions.md)   | 說明如何管理事件追蹤會話。                                                                         |
| [提供事件](providing-events.md)                                       | 說明如何註冊和檢測事件追蹤提供者。                                                       |
| [使用事件](consuming-events.md)                                       | 描述如何實回呼函式，用來從追蹤記錄檔或即時取用和處理事件。 |
| [Windows 軟體追蹤預處理器](windows-software-trace-preprocessor.md) | 提供有效的機制來記錄和取用應用程式或驅動程式執行期間所發生的事件。  |



 

在包含 Evntrace .h 標頭檔之前，請先包含 Wmistr .h 標頭檔。

 

 



