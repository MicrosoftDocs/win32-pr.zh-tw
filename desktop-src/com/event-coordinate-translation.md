---
title: 事件座標轉譯
description: 事件座標轉譯
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675012"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="d28b7-103">事件座標轉譯</span><span class="sxs-lookup"><span data-stu-id="d28b7-103">Event Coordinate Translation</span></span>

<span data-ttu-id="d28b7-104">控制項的96規格需要針對控制項所引發的事件傳遞的座標，使其不會被 HIMETRIC 為以點為基礎。</span><span class="sxs-lookup"><span data-stu-id="d28b7-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="d28b7-105">這項變更會讓事件以屬性和方法來進行協調，因此座標轉譯不再是容器的責任。</span><span class="sxs-lookup"><span data-stu-id="d28b7-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="d28b7-106">這會引發特定的相容性問題，其中控制項會使用非預期的座標基底引發事件，這應該只是96控制項容器裝載舊版96前控制項的問題，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d28b7-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="d28b7-107">當舊版的96前容器裝載96控制項時，控制項會將事件座標呈現為點，這應該不會造成容器任何問題，因為容器應辨識參數類型。</span><span class="sxs-lookup"><span data-stu-id="d28b7-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="d28b7-108">當96容器裝載96前控制項時，控制項將會顯示具有座標的容器，並預期容器會有任何需要的轉譯。</span><span class="sxs-lookup"><span data-stu-id="d28b7-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="d28b7-109">不過，96容器會預期控制項必須符合96控制項規格，並將其座標呈現為點。</span><span class="sxs-lookup"><span data-stu-id="d28b7-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="d28b7-110">控制項在容器所提供的 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)介面上使用 [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords)方法的方式，與用來達成此目標的屬性和方法相同。</span><span class="sxs-lookup"><span data-stu-id="d28b7-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="d28b7-111">因此，裝載96前控制項的96容器使用者必須注意，當引發事件時，可能需要進一步轉譯座標。</span><span class="sxs-lookup"><span data-stu-id="d28b7-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 




