---
title: '記錄 (Windows 篩選平台) '
description: Windows 篩選平台 (WFP) 提供封包捨棄和 IKE/AuthIP 失敗的記錄。
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106994969"
---
# <a name="logging-windows-filtering-platform"></a>記錄 (Windows 篩選平台) 

Windows 篩選平台 (WFP) 提供封包捨棄和 IKE/AuthIP 失敗的記錄。

記錄的事件會定義在 [**FWPM \_ NET \_ 事件 \_ 類型**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) 列舉型別中，如下所示。

-   IKE/AuthIP 主要模式失敗。
-   IKE/AuthIP 快速模式失敗。
-   AuthIP 延伸模式失敗。
-   分類期間捨棄的封包。
-   IPsec 丟棄的封包。

根據預設，會針對單播輸入封包和所有輸出封包啟用 WFP 記錄， (單播、多播和廣播) 。 您可以透過 [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) 管理功能，針對其餘的封包啟用記錄，或針對所有封包停用記錄。 事件設定在重新開機時持續存在。

記錄的事件會儲存在迴圈記錄中，也就是當記錄檔到達大小上限時，新的事件會覆寫舊的事件，而且可以使用 WFP 提供的 [事件管理](fwp-mgmt-functions.md) 函式進行分析。 事件記錄檔的大小上限為 128 KB，且最多可保存100到150個事件。

一般來說，列舉函數和 [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)會在建立列舉控制碼時，取得記錄的快照。 使用相同列舉控制碼的後續呼叫會傳回下一組專案，後面接著最後一個輸出緩衝區中的專案。

當應用程式透過呼叫 [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) 來停用 WFP 記錄 () 所有應用程式都會受到影響。 在應用程式重新啟用 WFP 記錄之前，不會清除事件記錄檔，但在那之前無法查詢事件記錄檔。

在重新開機之後，會清空 WFP 事件記錄檔。

 

 




