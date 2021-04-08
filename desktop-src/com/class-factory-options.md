---
title: Class Factory 選項
description: Class Factory 選項
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683140"
---
# <a name="class-factory-options"></a><span data-ttu-id="46751-103">Class Factory 選項</span><span class="sxs-lookup"><span data-stu-id="46751-103">Class Factory Options</span></span>

<span data-ttu-id="46751-104">ActiveX 控制項（藉由使用 COM 物件）必須有相關聯的伺服器程式碼，以支援透過 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 來建立控制項的最小值。</span><span class="sxs-lookup"><span data-stu-id="46751-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="46751-105">這是選擇性的（非必要），此類別物件也支援 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 以進行授權管理。</span><span class="sxs-lookup"><span data-stu-id="46751-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="46751-106">只有在意授權的廠商才需要支援 COM 的授權機制。</span><span class="sxs-lookup"><span data-stu-id="46751-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="46751-107">換句話說，因為 **IClassFactory2** 是達成 COM 層級授權的唯一方法，所以在需要授權的控制項的類別物件上需要這個介面。</span><span class="sxs-lookup"><span data-stu-id="46751-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46751-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="46751-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46751-109">控制項</span><span class="sxs-lookup"><span data-stu-id="46751-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 