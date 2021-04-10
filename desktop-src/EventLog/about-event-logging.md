---
description: 發生錯誤時，系統管理員或支援代表必須判斷造成錯誤的原因、嘗試復原遺失的資料，並防止錯誤重複發生。
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: 關於事件記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026331"
---
# <a name="about-event-logging"></a>關於事件記錄

發生錯誤時，系統管理員或支援代表必須判斷造成錯誤的原因、嘗試復原遺失的資料，並防止錯誤重複發生。 如果應用程式、作業系統和其他系統服務記錄重要事件（例如，記憶體不足的狀況或過多的存取磁片的嘗試），這會很有説明。 然後，系統管理員可以使用事件記錄檔來協助判斷哪些狀況造成錯誤，並找出發生錯誤的內容。 藉由定期查看事件記錄檔，系統管理員可以找出問題 (例如失敗的硬碟) ，然後才會造成損毀。

> [!Note]  
> 事件記錄 API 是針對在 Windows Server 2003、Windows XP 或 Windows 2000 作業系統上執行的應用程式所設計。 在 Windows Vista 中，已重新設計事件記錄基礎結構。 設計成在 Windows Vista 或更新版本的作業系統上執行的應用程式，現在應該會使用 [Windows 事件記錄](/windows/desktop/WES/windows-event-log) 檔來記錄事件。

 
本節討論使用事件記錄撰寫和取用事件的程式設計介面。

-   [事件類型](event-types.md)
-   [記錄指導方針](logging-guidelines.md)
-   [事件記錄元素](event-logging-elements.md)
-   [事件記錄作業](event-logging-operations.md)
-   [事件記錄模型](event-logging-model.md)
-   [事件記錄安全性](event-logging-security.md)

> [!Note]  
> 在 Windows Server 2003、Windows XP 或 Windows 2000 電腦上發佈大於 64 kb 之事件的應用程式，將無法在 Windows Vista 或更新版本的電腦上發佈事件。
