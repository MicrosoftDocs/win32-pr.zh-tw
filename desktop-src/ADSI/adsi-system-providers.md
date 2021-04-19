---
title: ADSI 服務提供者
description: 本主題概述伺服器中所提供的 ADSI 服務提供者。
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、服務提供者
- 服務提供者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106967288"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="3053c-105">ADSI 服務提供者</span><span class="sxs-lookup"><span data-stu-id="3053c-105">ADSI Service Providers</span></span>

<span data-ttu-id="3053c-106">ADSI 包含下表列出的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="3053c-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="3053c-107">服務提供者</span><span class="sxs-lookup"><span data-stu-id="3053c-107">Service provider</span></span> | <span data-ttu-id="3053c-108">描述</span><span class="sxs-lookup"><span data-stu-id="3053c-108">Description</span></span>                                                                                | <span data-ttu-id="3053c-109">取得詳細資訊</span><span class="sxs-lookup"><span data-stu-id="3053c-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3053c-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="3053c-110">LDAP</span></span><br/>  | <span data-ttu-id="3053c-111">與輕量型目錄存取協定相容的命名空間執行。</span><span class="sxs-lookup"><span data-stu-id="3053c-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="3053c-112">ADSI LDAP 提供者</span><span class="sxs-lookup"><span data-stu-id="3053c-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="3053c-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="3053c-113">WinNT</span></span><br/> | <span data-ttu-id="3053c-114">與 Windows 相容的命名空間實作為。</span><span class="sxs-lookup"><span data-stu-id="3053c-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="3053c-115">ADSI WinNT 提供者</span><span class="sxs-lookup"><span data-stu-id="3053c-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="3053c-116">其他服務提供者包含在 ADSI 以外的產品中。</span><span class="sxs-lookup"><span data-stu-id="3053c-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="3053c-117">以下是 Microsoft 所實行的 ADSI 服務提供者。</span><span class="sxs-lookup"><span data-stu-id="3053c-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="3053c-118">服務提供者</span><span class="sxs-lookup"><span data-stu-id="3053c-118">Service provider</span></span> | <span data-ttu-id="3053c-119">取得詳細資訊</span><span class="sxs-lookup"><span data-stu-id="3053c-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3053c-120">IIS</span><span class="sxs-lookup"><span data-stu-id="3053c-120">IIS</span></span><br/>   | <span data-ttu-id="3053c-121">[IIS ADSI 提供者架構](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="3053c-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="3053c-122">並非每個服務提供者都支援 ADSI 介面所公開的方法與屬性方法。</span><span class="sxs-lookup"><span data-stu-id="3053c-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="3053c-123">由於不同的目錄服務會因儲存的物件和屬性類型而異，因此請使用不同的通訊協定和驗證，ADSI 是設計來與支援的服務提供者順暢地搭配運作。</span><span class="sxs-lookup"><span data-stu-id="3053c-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="3053c-124">因此，有一些介面、方法和屬性方法適用于一個服務提供者，例如 LDAP，可能無法在另一個上運作，例如 WinNT。</span><span class="sxs-lookup"><span data-stu-id="3053c-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="3053c-125">本節包含提供者特定的資訊，例如 ADsPath 格式、用於該服務提供者的 ADSI 物件清單，以及 ADSI 中所含服務提供者的資料類型和語法資訊。</span><span class="sxs-lookup"><span data-stu-id="3053c-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="3053c-126">此外，ADSI 中包含的每個提供者都支援 ADSI 介面的摘要描述。</span><span class="sxs-lookup"><span data-stu-id="3053c-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="3053c-127">在 ADSI 中，不同的提供者會與不同的 Dll 相關聯。</span><span class="sxs-lookup"><span data-stu-id="3053c-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="3053c-128">LDAP 提供者與 Adsldp.dll、Adsldpc.dll 和 Adsmsext.dll 相關聯。</span><span class="sxs-lookup"><span data-stu-id="3053c-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="3053c-129">WinNT 提供者與 Adsnt.dll 相關聯。</span><span class="sxs-lookup"><span data-stu-id="3053c-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="3053c-130">路由器提供者與 Activeds.dll 相關聯。</span><span class="sxs-lookup"><span data-stu-id="3053c-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="3053c-131">請勿假設預設的 ADSI 提供者為安全線程。</span><span class="sxs-lookup"><span data-stu-id="3053c-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="3053c-132">多執行緒應用程式開發人員應該透過適當的同步處理物件（例如，信號、mutex、重要區段等等）來協調執行緒之間的存取。</span><span class="sxs-lookup"><span data-stu-id="3053c-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="3053c-133">如需 ADSI 服務提供者的詳細資訊，請參閱 adsi [路由器](adsi-router.md) 和 [Adsi 介面的提供者支援](provider-support-of-adsi-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="3053c-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

