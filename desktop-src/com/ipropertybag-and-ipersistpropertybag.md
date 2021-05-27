---
title: IPropertyBag 和 IPersistPropertyBag
description: IPropertyBag 和 IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a012fb2c202d93bcf4f4c8fa477133e841740b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549063"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a><span data-ttu-id="cf831-103">IPropertyBag 和 IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cf831-103">IPropertyBag and IPersistPropertyBag</span></span>

<span data-ttu-id="cf831-104">[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) 和 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) 會將 [另存新檔] 機制優化，因此建議用於執行「另存為文字」機制的 ActiveX 控制項容器。</span><span class="sxs-lookup"><span data-stu-id="cf831-104">[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) and [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) optimize save as text mechanisms, and therefore are recommended for ActiveX Control containers that implement a save as text mechanism.</span></span> <span data-ttu-id="cf831-105">**IPropertyBag** 是由容器所執行，大致類似于 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。</span><span class="sxs-lookup"><span data-stu-id="cf831-105">**IPropertyBag** is implemented by a container, and is roughly analogous to [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="cf831-106">**IPersistPropertyBag** 是由控制項所執行，大致上與 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)類似。</span><span class="sxs-lookup"><span data-stu-id="cf831-106">**IPersistPropertyBag** is implemented by controls, and is roughly analogous to [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream).</span></span>

 

 