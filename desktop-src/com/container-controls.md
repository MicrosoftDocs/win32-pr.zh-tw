---
title: 容器控制項
description: 容器控制項
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462480"
---
# <a name="container-controls"></a><span data-ttu-id="d7acc-103">容器控制項</span><span class="sxs-lookup"><span data-stu-id="d7acc-103">Container Controls</span></span>

<span data-ttu-id="d7acc-104">如上所述，容器控制項是以視覺方式包含其他控制項的 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="d7acc-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="d7acc-105">ActiveX 控制項架構會指定 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 介面，以啟用容器控制項。</span><span class="sxs-lookup"><span data-stu-id="d7acc-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="d7acc-106">雖然無法保證行為，但容器也可支援容器控制項，但不支援 **ISimpleFrameSite**。</span><span class="sxs-lookup"><span data-stu-id="d7acc-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="d7acc-107">基於這個理由，SimpleFrameSite 控制項的元件類別是必要的，因此需要此介面的完整功能。</span><span class="sxs-lookup"><span data-stu-id="d7acc-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="d7acc-108">若要在不執行 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)的情況下支援容器控制項，ActiveX 控制項容器必須：</span><span class="sxs-lookup"><span data-stu-id="d7acc-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="d7acc-109">隨時啟動所有控制項。</span><span class="sxs-lookup"><span data-stu-id="d7acc-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="d7acc-110">將包含的控制項重設為包含控制項的 hWnd。</span><span class="sxs-lookup"><span data-stu-id="d7acc-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="d7acc-111">維持容器控制項的父系。</span><span class="sxs-lookup"><span data-stu-id="d7acc-111">Remain the parent of the container control.</span></span>

 

 




