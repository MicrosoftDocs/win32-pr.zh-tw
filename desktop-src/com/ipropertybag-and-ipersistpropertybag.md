---
title: IPropertyBag 和 IPersistPropertyBag
description: IPropertyBag 和 IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2b3df0a3ad1166b9d6878aaaad85a8158508b5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683176"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a><span data-ttu-id="971c3-103">IPropertyBag 和 IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="971c3-103">IPropertyBag and IPersistPropertyBag</span></span>

<span data-ttu-id="971c3-104">[**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) 和 [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) 會將 [另存新檔] 機制優化，因此建議用於執行「另存為文字」機制的 ActiveX 控制項容器。</span><span class="sxs-lookup"><span data-stu-id="971c3-104">[**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) and [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) optimize save as text mechanisms, and therefore are recommended for ActiveX Control containers that implement a save as text mechanism.</span></span> <span data-ttu-id="971c3-105">**IPropertyBag** 是由容器所執行，大致類似于 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。</span><span class="sxs-lookup"><span data-stu-id="971c3-105">**IPropertyBag** is implemented by a container, and is roughly analogous to [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="971c3-106">**IPersistPropertyBag** 是由控制項所執行，大致上與 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)類似。</span><span class="sxs-lookup"><span data-stu-id="971c3-106">**IPersistPropertyBag** is implemented by controls, and is roughly analogous to [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream).</span></span>

 

 