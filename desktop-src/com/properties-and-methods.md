---
title: 屬性和方法
description: 就像任何 OLE 物件一樣，控制項可透過一組包含屬性和方法的傳入介面，提供大部分的功能。
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021115"
---
# <a name="properties-and-methods"></a><span data-ttu-id="16b1a-103">屬性和方法</span><span class="sxs-lookup"><span data-stu-id="16b1a-103">Properties and Methods</span></span>

<span data-ttu-id="16b1a-104">就像任何 OLE 物件一樣，控制項可透過一組包含屬性和方法的傳入介面，提供大部分的功能。</span><span class="sxs-lookup"><span data-stu-id="16b1a-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="16b1a-105">控制項會透過 OLE automation 來公開屬性和方法，讓容器能夠在容器提供的程式設計語言的控制下存取這些屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="16b1a-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="16b1a-106">為了支援透過使用者介面存取屬性，控制項提供屬性頁、OLEIVERB 屬性的支援 \_ 、每個屬性流覽，以及透過屬性變更通知的資料系結。</span><span class="sxs-lookup"><span data-stu-id="16b1a-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="16b1a-107">透過屬性頁，控制項可以顯示其屬性，並視需要顯示其容器。</span><span class="sxs-lookup"><span data-stu-id="16b1a-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="16b1a-108">藉由支援 OLEIVERB \_ 屬性，屬性專案就會顯示在容器的功能表上。</span><span class="sxs-lookup"><span data-stu-id="16b1a-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="16b1a-109">然後，終端使用者可以選取 [ **屬性** ] 專案來查看控制項的屬性頁，以及修改屬性。</span><span class="sxs-lookup"><span data-stu-id="16b1a-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="16b1a-110">每個屬性流覽支援的容器，可以將控制項的屬性顯示為較大屬性工作表的一部分，其中可能包含來自容器中數個控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="16b1a-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="16b1a-111">透過屬性變更通知，控制項可以通知用戶端其屬性已變更，讓用戶端可以執行任何必要的動作。</span><span class="sxs-lookup"><span data-stu-id="16b1a-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="16b1a-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="16b1a-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="16b1a-113">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="16b1a-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="16b1a-114">控制項方法</span><span class="sxs-lookup"><span data-stu-id="16b1a-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="16b1a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="16b1a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b1a-116">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="16b1a-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="16b1a-117">屬性頁和屬性工作表</span><span class="sxs-lookup"><span data-stu-id="16b1a-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




