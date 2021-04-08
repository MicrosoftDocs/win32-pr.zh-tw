---
title: 簡易框架網站內含專案
description: 簡易框架網站內含專案
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932067"
---
# <a name="simple-frame-site-containment"></a><span data-ttu-id="fc85d-103">簡易框架網站內含專案</span><span class="sxs-lookup"><span data-stu-id="fc85d-103">Simple Frame Site Containment</span></span>

<span data-ttu-id="fc85d-104">容器控制項是可以包含其他控制項的 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="fc85d-104">A container control is an ActiveX control that is capable of containing other controls.</span></span> <span data-ttu-id="fc85d-105">包含選項按鈕集合的群組方塊是容器控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="fc85d-105">A group box that contains a collection of radio buttons is an example of a container control.</span></span> <span data-ttu-id="fc85d-106">容器控制項應設定 OLEMISC \_ SIMPLEFRAME 狀態位，而且應該呼叫其容器的 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 執行。</span><span class="sxs-lookup"><span data-stu-id="fc85d-106">Container controls should set the OLEMISC\_SIMPLEFRAME status bit, and should call its container's [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementation.</span></span> <span data-ttu-id="fc85d-107">支援容器控制項的 ActiveX 控制項容器必須執行 **ISimpleFrameSite**。</span><span class="sxs-lookup"><span data-stu-id="fc85d-107">An ActiveX control container that supports container controls must implement **ISimpleFrameSite**.</span></span>

<span data-ttu-id="fc85d-108">CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl</span><span class="sxs-lookup"><span data-stu-id="fc85d-108">CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID\_SimpleFrameControl</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc85d-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc85d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc85d-110">元件類別</span><span class="sxs-lookup"><span data-stu-id="fc85d-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




