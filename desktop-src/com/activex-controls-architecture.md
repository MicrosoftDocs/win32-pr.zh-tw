---
title: ActiveX 控制項架構
description: ActiveX 控制項技術是以 OLE 中許多較低層級物件和介面的基礎為基礎。 控制項上可用的確切介面會因其功能而有所不同。 本節將進一步探討控制項可能提供的功能。
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672568"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="8ee75-105">ActiveX 控制項架構</span><span class="sxs-lookup"><span data-stu-id="8ee75-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="8ee75-106">ActiveX 控制項技術是以 OLE 中許多較低層級物件和介面的基礎為基礎。</span><span class="sxs-lookup"><span data-stu-id="8ee75-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="8ee75-107">控制項上可用的確切介面會因其功能而有所不同。</span><span class="sxs-lookup"><span data-stu-id="8ee75-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="8ee75-108">本節將進一步探討控制項可能提供的功能。</span><span class="sxs-lookup"><span data-stu-id="8ee75-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="8ee75-109">ActiveX 控制項可用來提供在應用程式中建立使用者介面的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="8ee75-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="8ee75-110">例如，當按下容器應用程式時，在容器應用程式中起始動作的按鈕是一個簡單的控制項。</span><span class="sxs-lookup"><span data-stu-id="8ee75-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="8ee75-111">以下是提供這些使用者介面建立區塊的相關層面：</span><span class="sxs-lookup"><span data-stu-id="8ee75-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="8ee75-112">控制項可以內嵌在其容器用戶端內，以支援用戶端內的一些使用者介面活動。</span><span class="sxs-lookup"><span data-stu-id="8ee75-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="8ee75-113">因此，當控制項內嵌在容器內時，必須提供其本身的視覺標記法，並需要提供方法來儲存其狀態，例如其屬性值及其在容器中的位置。</span><span class="sxs-lookup"><span data-stu-id="8ee75-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="8ee75-114">用戶端必須支援做為内嵌物件的容器。</span><span class="sxs-lookup"><span data-stu-id="8ee75-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="8ee75-115">藉由使用鍵盤或滑鼠啟用控制項，終端使用者就會在用戶端應用程式中起始一些動作。</span><span class="sxs-lookup"><span data-stu-id="8ee75-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="8ee75-116">因此，控制項必須回應鍵盤活動，而且必須能夠與用戶端通訊，如此它就可以通知其活動的容器，並在用戶端觸發事件。</span><span class="sxs-lookup"><span data-stu-id="8ee75-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="8ee75-117">用戶端通常也會提供程式設計語言，讓使用者可以透過它來起始控制項的屬性和方法所提供的動作。</span><span class="sxs-lookup"><span data-stu-id="8ee75-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="8ee75-118">因此，控制項必須支援自動化，以及一組設計階段與執行時間功能。</span><span class="sxs-lookup"><span data-stu-id="8ee75-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="8ee75-119">由於其在提供使用者介面建立區塊中的角色，因此，控制項通常會使用 OLE 技術來支援下欄區域中的功能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8ee75-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="8ee75-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>屬性和方法</span><span class="sxs-lookup"><span data-stu-id="8ee75-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="8ee75-121">控制項和任何 OLE 物件一樣，都可以透過一組包含屬性和方法的傳入介面，提供大部分的功能。</span><span class="sxs-lookup"><span data-stu-id="8ee75-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="8ee75-122">容器可以提供其他環境屬性，也可以支援透過匯總延伸控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="8ee75-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="8ee75-123">這些功能可在 OLE automation、屬性頁、可連線物件和 ActiveX 控制項技術上 rest。</span><span class="sxs-lookup"><span data-stu-id="8ee75-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="8ee75-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>事件</span><span class="sxs-lookup"><span data-stu-id="8ee75-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="8ee75-125">除了提供屬性和方法之外，ActiveX 控制項也可以提供輸出介面，通知其事件的用戶端。</span><span class="sxs-lookup"><span data-stu-id="8ee75-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="8ee75-126">用戶端必須支援這些事件的處理。</span><span class="sxs-lookup"><span data-stu-id="8ee75-126">The client must support handling of these events.</span></span> <span data-ttu-id="8ee75-127">這些功能使用 OLE automation 和可連接的物件。</span><span class="sxs-lookup"><span data-stu-id="8ee75-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="8ee75-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>視覺標記法</span><span class="sxs-lookup"><span data-stu-id="8ee75-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="8ee75-129">控制項可以支援定位，並在其容器內顯示本身。</span><span class="sxs-lookup"><span data-stu-id="8ee75-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="8ee75-130">容器會定位控制項並判斷其大小。</span><span class="sxs-lookup"><span data-stu-id="8ee75-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="8ee75-131">這些功能使用複合檔案技術，包括 OLE 拖放技術。</span><span class="sxs-lookup"><span data-stu-id="8ee75-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="8ee75-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>鍵盤處理</span><span class="sxs-lookup"><span data-stu-id="8ee75-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="8ee75-133">控制項可以回應鍵盤快速鍵，讓終端使用者可以起始控制項所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="8ee75-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="8ee75-134">容器會管理其所有內嵌控制項的鍵盤活動。</span><span class="sxs-lookup"><span data-stu-id="8ee75-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="8ee75-135">這些功能使用控制項和複合檔案技術。</span><span class="sxs-lookup"><span data-stu-id="8ee75-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="8ee75-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>堅持</span><span class="sxs-lookup"><span data-stu-id="8ee75-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="8ee75-137">控制項可以儲存其狀態。</span><span class="sxs-lookup"><span data-stu-id="8ee75-137">A control can save its state.</span></span> <span data-ttu-id="8ee75-138">用戶端會管理其內嵌控制項的持續性。</span><span class="sxs-lookup"><span data-stu-id="8ee75-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="8ee75-139">這些功能使用結構化儲存體和物件持續性技術。</span><span class="sxs-lookup"><span data-stu-id="8ee75-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="8ee75-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>註冊和授權</span><span class="sxs-lookup"><span data-stu-id="8ee75-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="8ee75-141">控制項通常支援自我註冊，並且在具現化時，會建立一組登錄專案。</span><span class="sxs-lookup"><span data-stu-id="8ee75-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="8ee75-142">您也可以授權控制項來協助防止未經授權的使用。</span><span class="sxs-lookup"><span data-stu-id="8ee75-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="8ee75-143">大部分的功能都牽涉到控制項及其用戶端容器。</span><span class="sxs-lookup"><span data-stu-id="8ee75-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ee75-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ee75-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ee75-145">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="8ee75-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




