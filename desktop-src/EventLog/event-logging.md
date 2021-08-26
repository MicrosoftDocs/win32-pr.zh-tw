---
description: 許多應用程式會在專屬的錯誤記錄檔中記錄錯誤和事件，每個都有自己的格式和使用者介面。
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: '事件記錄 (事件記錄) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8894c7a6d038efdc317611ca6284f62d99c82ebc767b6f96f83931803a887185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927838"
---
# <a name="event-logging-event-logging"></a>事件記錄 (事件記錄) 

許多應用程式會在專屬的錯誤記錄檔中記錄錯誤和事件，每個都有自己的格式和使用者介面。 不同應用程式中的資料無法輕鬆地合併為一份完整的報告，需要系統管理員或支援代表來檢查各種來源以診斷問題。

事件記錄可為應用程式提供標準、集中式的方式 (以及記錄重要軟體和硬體事件的作業系統) 。 事件記錄服務會記錄來自各種來源的事件，並將它們儲存在稱為 *事件記錄* 檔的單一集合中。 事件檢視器可讓您查看記錄;程式設計介面也可讓您檢查記錄。

-   [關於事件記錄](about-event-logging.md)
-   [使用事件記錄](using-event-logging.md)
-   [事件記錄參考](event-logging-reference.md)

> [!Note]  
> 事件記錄 API 是針對 Windows Server 2003、Windows XP 或 Windows 2000 作業系統上執行的應用程式所設計。 在 Windows Vista 中，已重新設計事件記錄基礎結構。 設計用來在 Windows Vista 或更新版本的作業系統上執行的應用程式，應該使用[Windows 事件記錄](/windows/desktop/WES/windows-event-log)檔來記錄事件。
