---
description: 事件追蹤會話會記錄一或多個提供者的事件。
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: 控制事件追蹤會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972232"
---
# <a name="controlling-event-tracing-sessions"></a>控制事件追蹤會話

事件追蹤會話會記錄一或多個 [提供者](providing-events.md)的事件。 控制器會定義會話並啟用提供者。 定義會話通常包括指定會話和記錄檔名稱、要使用的記錄檔類型，以及用來記錄事件的時間戳記解析。 控制器也可以更新和查詢事件追蹤會話。

下列主題將示範如何定義和更新會話，以及如何啟用事件追蹤提供者：

-   [設定和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)
-   [設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)
-   [設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)
-   [設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)
-   [更新事件追蹤會話](updating-an-event-tracing-session.md)
-   [正在抓取其他事件追蹤資料](retrieving-additional-event-tracing-data.md)

如需排清和查詢會話的詳細資訊，請分別參閱 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 和 [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa)。

只有以較高的系統管理許可權執行的使用者、Performance Log Users 群組中的使用者，以及以 LocalSystem、LocalService 或 NetworkService 身分執行的應用程式，才能控制事件追蹤會話。 若要授與受限制的使用者控制追蹤會話的能力，請將它們新增至 Performance Log Users 群組。

**WINDOWS XP 和 windows 2000：** 任何人都可以控制追蹤會話。

 

 
