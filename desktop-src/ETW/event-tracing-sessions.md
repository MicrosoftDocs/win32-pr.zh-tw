---
description: 事件追蹤會話會記錄控制器所啟用的一或多個提供者的事件。
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: 事件追蹤會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2edfe4bdfaf621575d8f2f8ab7d81a09aae8bfbddcb3f63890c4083378bb905b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083238"
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

 

 



