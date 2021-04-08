---
title: IAccessible 支援的類型
description: IAccessible 支援的類型
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673324"
---
# <a name="types-of-iaccessible-support"></a>IAccessible 支援的類型

Microsoft Active Accessibility 伺服器有兩種類型的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援：原生和 proxy。 應用程式中使用的 UI 元素決定適當的支援類型。 現今撰寫的許多伺服器都能充分利用 **IAccessible** proxy，並且只針對非由 Oleacc.dll 進行 proxy 處理的控制項執行 **IAccessible** ，例如使用自訂視窗類別名稱的無視窗控制項或控制項。

## <a name="in-this-section"></a>本節內容

-   [原生 Active Accessibility 實作為](native-active-accessibility-implementation.md)
-   [IAccessible proxy](iaccessible-proxies.md)

 

 




