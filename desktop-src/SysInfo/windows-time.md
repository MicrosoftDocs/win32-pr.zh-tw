---
description: Windows time 是自上次啟動系統以來經過的毫秒數。
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Windows Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115168"
---
# <a name="windows-time"></a>Windows Time

*Windows time* 是自上次啟動系統以來經過的毫秒數。 這種格式的存在主要是為了與16位 Windows 的回溯相容性。 為了確保為16位 Windows 設計的應用程式可繼續順利執行， [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函數會傳回目前的 Windows 時間。

您通常會使用 [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 或 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) 函數，將目前的 Windows 時間與 [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) 函式所傳回的時間進行比較。 **GetMessageTime** 會傳回指定的訊息建立時的 Windows 時間。 **GetTickCount** 和 **GetTickCount64** 僅限於系統計時器的解析度，大約10毫秒到16毫秒。 **GetTickCount** 或 **GetTickCount64** 所取出的經過時間，包括系統花在睡眠或休眠狀態的時間。

如果您需要較高的解析度計時器，請使用 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 函數、 [多媒體計時器](/windows/desktop/Multimedia/multimedia-timers)或 [高解析度計時器](../winmsg/about-timers.md)。 **QueryUnbiasedInterruptTime** 函式所抓取的經過時間只包含系統花在工作狀態的時間。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP/2000：** 從 Windows 7 和 Windows Server 2008 R2 開始，可以使用 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 函數。

您可以使用 [系統執行時間] 效能計數器來取得自電腦啟動以來經過的秒數。 您可以從登錄機碼 **HKEY \_ 效能 \_ 資料** 的效能資料中抓取此效能計數器。 傳回的值是8位元組值。 如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。

 

 
