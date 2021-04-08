---
title: ADSI 擴充功能架構
description: ADSI 擴充功能是以 COM 匯總模型為基礎，具有數個增強功能。 擴充功能必須遵守所有 COM 規則。 如需詳細資訊，請參閱 COM 規格。
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- 延伸模組 ADSI、延伸模組架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377409f4b9ac36d72d6885e89860b9e6e680b103
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683104"
---
# <a name="adsi-extension-architecture"></a><span data-ttu-id="e37ab-106">ADSI 擴充功能架構</span><span class="sxs-lookup"><span data-stu-id="e37ab-106">ADSI Extension Architecture</span></span>

<span data-ttu-id="e37ab-107">ADSI 擴充功能是以 COM 匯總模型為基礎，具有數個增強功能。</span><span class="sxs-lookup"><span data-stu-id="e37ab-107">ADSI extensions are based on the COM aggregation model with several enhancements.</span></span> <span data-ttu-id="e37ab-108">擴充功能必須遵守所有 COM 規則。</span><span class="sxs-lookup"><span data-stu-id="e37ab-108">Extensions must adhere to all COM rules.</span></span> <span data-ttu-id="e37ab-109">如需詳細資訊，請參閱 COM 規格。</span><span class="sxs-lookup"><span data-stu-id="e37ab-109">For more information, see the COM specification.</span></span>

<span data-ttu-id="e37ab-110">以下是 COM 匯總模型的評論。</span><span class="sxs-lookup"><span data-stu-id="e37ab-110">Here is a review of the COM aggregation model.</span></span>

![com 匯總模型](images/comagmod.png)

<span data-ttu-id="e37ab-112">匯總（也稱為內建物件）是匯總工具所建立的物件。</span><span class="sxs-lookup"><span data-stu-id="e37ab-112">An aggregate, also known as an inner object, is an object that an aggregator creates.</span></span> <span data-ttu-id="e37ab-113">您的擴充物件是匯總。</span><span class="sxs-lookup"><span data-stu-id="e37ab-113">Your extension object is an aggregate.</span></span>

<span data-ttu-id="e37ab-114">匯總工具（也稱為外部物件）是建立匯總的物件。</span><span class="sxs-lookup"><span data-stu-id="e37ab-114">An aggregator, also known as an outer object, is an object that creates an aggregate.</span></span> <span data-ttu-id="e37ab-115">ADSI 是一個匯總工具。</span><span class="sxs-lookup"><span data-stu-id="e37ab-115">ADSI is an aggregator.</span></span>

<span data-ttu-id="e37ab-116">內建物件會將其 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 委派給匯總工具的 **iunknown**。</span><span class="sxs-lookup"><span data-stu-id="e37ab-116">The inner object delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to the aggregator's **IUnknown**.</span></span>

<span data-ttu-id="e37ab-117">ADSI 擴充功能會將下列增強功能新增至 COM 匯總，以滿足其需求：</span><span class="sxs-lookup"><span data-stu-id="e37ab-117">ADSI extensions add the following enhancements to COM aggregation to satisfy its requirements:</span></span>

-   <span data-ttu-id="e37ab-118">可讓每個延伸模組寫入器擴充 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="e37ab-118">Enables each extension writer to extend ADSI objects.</span></span> <span data-ttu-id="e37ab-119">延伸模組寫入器可以使用 ADSI 註冊它的擴充功能，而不會受到其他副檔名的存在影響。</span><span class="sxs-lookup"><span data-stu-id="e37ab-119">An extension writer can register its extension with ADSI and not be affected by the existence of other extensions.</span></span> <span data-ttu-id="e37ab-120">在 COM 匯總模型中，匯總工具必須有匯總的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e37ab-120">In the COM aggregation model, the aggregator must have the aggregate's CLSID.</span></span> <span data-ttu-id="e37ab-121">ADSI 會放寬這項需求，使其成為所有延伸模組的匯總工具。</span><span class="sxs-lookup"><span data-stu-id="e37ab-121">ADSI relaxes this requirement by making itself act as the aggregator for all extensions.</span></span> <span data-ttu-id="e37ab-122">因此，延伸模組會位於相同層級，而不是形成一層嵌套的元件。</span><span class="sxs-lookup"><span data-stu-id="e37ab-122">Therefore, instead of forming a layer of nested components, extensions are at the same level.</span></span>
-   <span data-ttu-id="e37ab-123">允許一個物件，一個 IDispatch。</span><span class="sxs-lookup"><span data-stu-id="e37ab-123">Allows one object, one IDispatch.</span></span> <span data-ttu-id="e37ab-124">自動化支援是 ADSI 最重要的功能之一。</span><span class="sxs-lookup"><span data-stu-id="e37ab-124">Automation support is one of the most important features of ADSI.</span></span> <span data-ttu-id="e37ab-125">因為 ADSI 支援 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面，所以可達成自動化支援。</span><span class="sxs-lookup"><span data-stu-id="e37ab-125">Automation support is achieved because ADSI supports the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e37ab-126">建議延伸模組寫入器支援 **IDispatch** 介面。</span><span class="sxs-lookup"><span data-stu-id="e37ab-126">Extension writers are encouraged to support the **IDispatch** interface.</span></span> <span data-ttu-id="e37ab-127">不過，指定的物件上應該只有一個 **IDispatch** 介面。</span><span class="sxs-lookup"><span data-stu-id="e37ab-127">However, there should be only one **IDispatch** interface on a given object.</span></span> <span data-ttu-id="e37ab-128">ADSI 整合並收集不同擴充功能的許多 **IDispatch** 介面，並將其顯示為自動化控制器的一個一致 **idispatch** 。</span><span class="sxs-lookup"><span data-stu-id="e37ab-128">ADSI integrates and collects the many **IDispatch** interfaces from different extensions and presents them as one consistent **IDispatch** to the Automation controller.</span></span> <span data-ttu-id="e37ab-129">每個擴充功能在匯總時，都必須將其 **idispatch** 呼叫重新路由傳送至 ADSI 所提供的 **idispatch** 。</span><span class="sxs-lookup"><span data-stu-id="e37ab-129">Each extension, when aggregated, must re-route its **IDispatch** calls to the **IDispatch** provided by ADSI.</span></span>

<span data-ttu-id="e37ab-130">由於 ADSI 物件管理員提供的服務（位於每個 ADSI 提供者上），因此這些解決方案都是可行的。</span><span class="sxs-lookup"><span data-stu-id="e37ab-130">All these solutions are possible because of services that the ADSI Object Manager provides, which reside on each ADSI provider.</span></span>

<span data-ttu-id="e37ab-131">下圖顯示 ADSI 擴充功能模型架構。</span><span class="sxs-lookup"><span data-stu-id="e37ab-131">The following figure shows the ADSI Extension Model architecture.</span></span>

![adsi 擴充模型架構](images/adsiexmo.png)

<span data-ttu-id="e37ab-133">ADSI 支援兩種層級的延伸模組：</span><span class="sxs-lookup"><span data-stu-id="e37ab-133">ADSI supports two levels of extension:</span></span>

-   <span data-ttu-id="e37ab-134">早期繫結支援。</span><span class="sxs-lookup"><span data-stu-id="e37ab-134">Early Binding Support.</span></span> <span data-ttu-id="e37ab-135">這是延伸模組的第一個層級。</span><span class="sxs-lookup"><span data-stu-id="e37ab-135">This is the first level of extension.</span></span> <span data-ttu-id="e37ab-136">延伸模組必須支援註冊和執行新的介面。</span><span class="sxs-lookup"><span data-stu-id="e37ab-136">An extension must support registration and implement new interfaces.</span></span> <span data-ttu-id="e37ab-137">擴充功能取用者必須使用支援早期繫結的工具或腳本主機，例如 Visual C++ Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="e37ab-137">The extension consumers must use tools or scripting hosts that support early binding, for example, Visual C++ , Visual Basic.</span></span>
-   <span data-ttu-id="e37ab-138">晚期繫結支援。</span><span class="sxs-lookup"><span data-stu-id="e37ab-138">Late Binding Support.</span></span> <span data-ttu-id="e37ab-139">當延伸模組滿足所有早期繫結需求，並執行額外的介面 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e37ab-139">This happens when an extension satisfies all early binding requirements, and implements an additional interface, [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span> <span data-ttu-id="e37ab-140">延伸模組實作者可以使用任何以 Automation 控制器運作的工具，例如 Windows Script Host、Active Server Pages 或具有 VBScript 的 HTML。</span><span class="sxs-lookup"><span data-stu-id="e37ab-140">Extension implementers can use any tool that operates as an Automation controller, such as the Windows Script Host, Active Server Pages, or HTML with VBScript.</span></span>

 

 