---
description: 事件追蹤會話會記錄控制器所啟用的一或多個提供者的事件。
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: 事件追蹤會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce49453881d9106119dab15b64ac0698e9a493f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850312"
---
# <a name="event-tracing-sessions"></a>事件追蹤會話

事件追蹤會話會記錄[控制器](controlling-event-tracing-sessions.md)所啟用的一或多個[提供者](providing-events.md)的事件。 會話也負責管理和清除緩衝區。 控制器會定義會話，這通常包括指定會話和記錄檔名稱、要使用的記錄檔類型，以及用來記錄事件的時間戳記解析。

事件追蹤最多可支援64個事件追蹤會話同時執行。 在這些課程中，有兩個特殊用途的會話。 其餘的會話可供一般使用。 這兩個特殊用途的會話為：

-   全域記錄器會話
-   NT 核心記錄器會話

全域記錄器事件追蹤會話會記錄作業系統開機程式初期發生的事件，例如設備磁碟機所產生的事件。 如需設定全域記錄器事件追蹤會話的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。

NT Kernel 記錄器事件追蹤會話會記錄作業系統所產生的預先定義系統事件，例如磁片 IO 或分頁錯誤事件。 如需設定 NT Kernel 記錄器事件追蹤會話的詳細資訊，請設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。

如需定義一般事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

**Windows 2000：** 僅支援32事件追蹤會話。

 

 



