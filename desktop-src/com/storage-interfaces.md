---
title: 儲存體介面
description: 儲存體介面
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549263"
---
# <a name="storage-interfaces"></a><span data-ttu-id="26937-103">儲存體介面</span><span class="sxs-lookup"><span data-stu-id="26937-103">Storage Interfaces</span></span>

<span data-ttu-id="26937-104">控制項容器必須能夠支援執行 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)或 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)的控制項。</span><span class="sxs-lookup"><span data-stu-id="26937-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="26937-105">（選擇性）容器可支援任何其他持續性介面，例如 [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))、 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)和 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) 提供支援的控制項。</span><span class="sxs-lookup"><span data-stu-id="26937-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="26937-106">當 ActiveX 控制項容器選擇並初始化儲存介面以使用 ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)、 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)等) 之後，該儲存體介面將會在控制項的存留期內維持主要儲存介面，也就是控制項將仍擁有儲存體。</span><span class="sxs-lookup"><span data-stu-id="26937-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="26937-107">這並不會阻止容器儲存到其他儲存介面。</span><span class="sxs-lookup"><span data-stu-id="26937-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="26937-108">ActiveX 控制項容器不需要支援另存為文字機制，因此使用 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) 和相關聯的容器端介面 [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="26937-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) and the associated container-side interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26937-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="26937-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26937-110">容器</span><span class="sxs-lookup"><span data-stu-id="26937-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 