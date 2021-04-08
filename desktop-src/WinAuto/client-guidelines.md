---
title: 用戶端指導方針
description: 用戶端開發人員應該使用下列功能來取得使用者介面元素的相關資訊。
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103932881"
---
# <a name="client-guidelines"></a><span data-ttu-id="8e045-103">用戶端指導方針</span><span class="sxs-lookup"><span data-stu-id="8e045-103">Client Guidelines</span></span>

<span data-ttu-id="8e045-104">用戶端開發人員應該使用下列功能來取得使用者介面元素的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="8e045-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="8e045-105">若要取得物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，請呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。</span><span class="sxs-lookup"><span data-stu-id="8e045-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="8e045-106">若要檢查及操作可存取的物件，請使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="8e045-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="8e045-107">若要接收 [WinEvents](winevents-overview.md)，請呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) ，針對與用戶端應用程式相關的事件註冊 new-winevent 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="8e045-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8e045-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="8e045-108">In this section</span></span>

-   [<span data-ttu-id="8e045-109">用戶端如何取得子識別碼</span><span class="sxs-lookup"><span data-stu-id="8e045-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




