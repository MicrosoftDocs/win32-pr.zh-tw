---
title: 用戶端指導方針
description: 用戶端開發人員應該使用下列功能來取得使用者介面元素的相關資訊。
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133941"
---
# <a name="client-guidelines"></a>用戶端指導方針

用戶端開發人員應該使用下列功能來取得使用者介面元素的相關資訊：

-   若要取得物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，請呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。
-   若要檢查及操作可存取的物件，請使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法。
-   若要接收 [WinEvents](winevents-overview.md)，請呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) ，針對與用戶端應用程式相關的事件註冊 new-winevent 回呼函式。

## <a name="in-this-section"></a>本節內容

-   [用戶端如何取得子識別碼](how-clients-obtain-child-ids.md)

 

 




