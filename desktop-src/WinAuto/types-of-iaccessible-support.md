---
title: IAccessible 支援的類型
description: IAccessible 支援的類型
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb38ed0b5f7a306f2551085c77f77a3793efec3bc9281cd44d1d7277abe81fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993978"
---
# <a name="types-of-iaccessible-support"></a>IAccessible 支援的類型

Microsoft Active Accessibility 伺服器有兩種類型的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援：原生和 proxy。 應用程式中使用的 UI 元素決定適當的支援類型。 現今撰寫的許多伺服器都能充分利用 **IAccessible** proxy，並且只針對非由 Oleacc.dll 進行 proxy 處理的控制項執行 **IAccessible** ，例如使用自訂視窗類別名稱的無視窗控制項或控制項。

## <a name="in-this-section"></a>本節內容

-   [原生 Active Accessibility 實作為](native-active-accessibility-implementation.md)
-   [IAccessible proxy](iaccessible-proxies.md)

 

 




