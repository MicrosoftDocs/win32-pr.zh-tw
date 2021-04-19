---
description: 深入瞭解：記憶體管理追蹤事件
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: 記憶體管理追蹤事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997265"
---
# <a name="memory-management-tracing-events"></a>記憶體管理追蹤事件

本節說明特定記憶體管理追蹤事件詳細資料的詳細資訊。

記憶體管理追蹤是一個疑難排解功能，可在零售二進位檔中啟用，以盡可能減少額外負荷來追蹤特定的記憶體管理事件。 這項功能可讓開發人員和產品支援獲得更佳的診斷功能。 記憶體管理事件追蹤支援追蹤堆積配置、重新配置和可用的作業。

記憶體管理事件追蹤會使用 Windows 的事件追蹤 (ETW) 是作業系統所提供的一般用途高速追蹤功能。 ETW 針對使用者模式應用程式和核心模式設備磁碟機所引發的事件，提供追蹤機制。 ETW 可以動態啟用和停用記錄，讓您輕鬆地在生產環境中執行詳細追蹤，而不需要重新開機或重新開機應用程式。 Windows 7、Windows Server 2008 R2 和更新版本支援使用 ETW 的記憶體管理事件追蹤。 如需 ETW 的一般資訊，請參閱 [使用 Etw 改善偵錯工具和效能微調](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)。

下列清單提供每個記憶體管理追蹤事件的詳細資訊。 如需任何事件的詳細資訊，請按一下事件名稱。



| 活動名稱                                                  | Description                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**ETW \_ 堆積 \_ 事件 \_ 分配**](etw-heap-event-alloc.md)     | 堆積配置作業的記憶體管理追蹤事件。    |
| [**ETW \_ 堆積 \_ 事件 \_ 可用**](etw-heap-event-free.md)       | 堆積免費作業的記憶體管理追蹤事件。          |
| [**ETW \_ 堆積 \_ 事件 \_ REALLOC**](etw-heap-event-realloc.md) | 堆積重新配置作業的記憶體管理追蹤事件。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 ETW 改善偵錯和效能調整](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
