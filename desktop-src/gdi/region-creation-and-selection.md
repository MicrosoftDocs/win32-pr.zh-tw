---
description: 應用程式會藉由呼叫與特定圖形相關聯的函式來建立區域。 下表顯示與每個標準圖形相關聯的函式 () 。
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: 區域建立和選取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972548"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="8af94-104">區域建立和選取</span><span class="sxs-lookup"><span data-stu-id="8af94-104">Region Creation and Selection</span></span>

<span data-ttu-id="8af94-105">應用程式會藉由呼叫與特定圖形相關聯的函式來建立區域。</span><span class="sxs-lookup"><span data-stu-id="8af94-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="8af94-106">下表顯示與每個標準圖形相關聯的函式 () 。</span><span class="sxs-lookup"><span data-stu-id="8af94-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="8af94-107">形狀</span><span class="sxs-lookup"><span data-stu-id="8af94-107">Shape</span></span>                                   | <span data-ttu-id="8af94-108">函式</span><span class="sxs-lookup"><span data-stu-id="8af94-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af94-109">矩形區域</span><span class="sxs-lookup"><span data-stu-id="8af94-109">Rectangular region</span></span>                      | <span data-ttu-id="8af94-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)、 [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)、 [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span><span class="sxs-lookup"><span data-stu-id="8af94-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="8af94-111">具有圓角的矩形區域</span><span class="sxs-lookup"><span data-stu-id="8af94-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="8af94-112">**CreateRoundRectRgn**</span><span class="sxs-lookup"><span data-stu-id="8af94-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="8af94-113">橢圓形區域</span><span class="sxs-lookup"><span data-stu-id="8af94-113">Elliptical region</span></span>                       | <span data-ttu-id="8af94-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)、 [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="8af94-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="8af94-115">多邊形區域</span><span class="sxs-lookup"><span data-stu-id="8af94-115">Polygonal region</span></span>                        | <span data-ttu-id="8af94-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)、 [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="8af94-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="8af94-117">每個區域建立函數都會傳回識別新區域的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8af94-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="8af94-118">應用程式可以使用此控制碼，藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式並提供此控制碼作為第二個引數，來選取區域進入裝置內容。</span><span class="sxs-lookup"><span data-stu-id="8af94-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="8af94-119">將區域選取至裝置內容之後，應用程式就可以對其執行各種作業。</span><span class="sxs-lookup"><span data-stu-id="8af94-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



