---
description: 在 WMI 基礎結構中， (Winmgmt) 的 WMI 服務是作業系統元件，可做為管理應用程式與 WMI 資料提供者之間的中繼程式。 WMI 存放庫是 WMI 相關靜態資料的儲存區域。
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: WMI 基礎結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bc4492c7d26f422705863609a2e0ec19af5eb930e0aa80f4fd8bb8c26bea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757328"
---
# <a name="wmi-infrastructure"></a>WMI 基礎結構

在 WMI 基礎結構中， (Winmgmt) 的 WMI 服務是作業系統元件，可做為管理應用程式與 WMI 資料 [*提供者*](gloss-p.md)之間的中繼程式。 [*Wmi 存放庫*](gloss-w.md)是 wmi 相關靜態資料的儲存區域。

在 (SVCHOST) 的共用服務主機進程內，會將 WMI 服務實作為服務進程。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

WMI 服務會在第一個管理應用程式或腳本呼叫以連接至 WMI 命名空間時啟動。 視設定而定，當管理應用程式未呼叫 WMI 服務時，可能會關閉或進入記憶體不足的設定檔。

WMI 服務會透過 COM 介面與管理應用程式互動。 當應用程式透過介面提出要求時，WMI 會判斷要求是否適用于靜態或動態資料。 如果要求牽涉到靜態資料，例如受管理物件的名稱，WMI 就會從存放庫中取出資料。 如果要求牽涉到動態資料，例如受管理物件目前使用的記憶體數量，則 WMI 會將要求傳遞給提供者。

提供者會向 WMI 服務註冊其位置，這可讓 WMI 路由傳送資料要求。 提供者也會註冊對特定作業的支援，例如資料抓取、修改、刪除、列舉或查詢處理。 WMI 服務會使用提供者註冊資訊來比對應用程式要求與適當的提供者。 WMI 也會視需要使用註冊資訊來載入和卸載提供者。 當提供者完成處理要求時，提供者會將結果傳回給 WMI 服務。 WMI 接著會透過 COM 介面將結果轉送至應用程式。 如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。

WMI 使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) 來記錄 WMI 服務活動。

由於基礎結構會處理提供者與管理應用程式之間的所有流量，因此基礎結構會提供下列功能：

-   事件通知支援

    如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。

-   查詢語言支援

    如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

-   安全性支援

    如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

-   腳本存取效能計數器資料

    如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 架構](wmi-architecture.md)
</dt> </dl>

 

 
