---
description: WMI 支援不同的執行緒模型，取決於提供者的裝載方式和提供者功能的類型，例如類別或屬性。
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: 選擇正確的註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977953"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="6553c-103">選擇正確的註冊</span><span class="sxs-lookup"><span data-stu-id="6553c-103">Choosing Correct Registration</span></span>

<span data-ttu-id="6553c-104">WMI 支援不同的執行緒模型，取決於提供者的裝載方式和提供者功能的類型，例如 [類別](writing-a-class-provider.md) 或 [屬性](writing-a-property-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="6553c-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="6553c-105">例如，低 [*耦合提供者*](gloss-d.md) 不支援所有類型的提供者功能。</span><span class="sxs-lookup"><span data-stu-id="6553c-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="6553c-106">如需不同裝載模型及其設定方式的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="6553c-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="6553c-107">In-Process 提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-107">In-Process Providers</span></span>

<span data-ttu-id="6553c-108">同進程提供者是在共用的主機進程中執行，Wmiprvse.exe。</span><span class="sxs-lookup"><span data-stu-id="6553c-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="6553c-109">大部分的內建提供者類型都會使用多執行緒的單元 (MTA) 模型。</span><span class="sxs-lookup"><span data-stu-id="6553c-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="6553c-110">MTA 模型支援下列類型的提供者功能：</span><span class="sxs-lookup"><span data-stu-id="6553c-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="6553c-111">類別提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="6553c-112">執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="6553c-113">方法提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="6553c-114">屬性提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="6553c-115">事件提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="6553c-116">事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="6553c-117">針對某些類型的提供者功能，支援單一執行緒的單元 (STA) 模型：</span><span class="sxs-lookup"><span data-stu-id="6553c-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="6553c-118">執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="6553c-119">方法提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="6553c-120">事件提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="6553c-121">事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="6553c-122">跨進程提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-122">Out-of-Process Providers</span></span>

<span data-ttu-id="6553c-123">裝載于不同共用服務主機的提供者支援下列提供者功能：</span><span class="sxs-lookup"><span data-stu-id="6553c-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="6553c-124">類別提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="6553c-125">執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="6553c-126">方法提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="6553c-127">屬性提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="6553c-128">事件提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="6553c-129">事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="6553c-130">如需共用服務主機的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="6553c-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="6553c-131">低耦合提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-131">Decoupled Providers</span></span>

<span data-ttu-id="6553c-132">低耦合提供者是裝載在應用程式中。</span><span class="sxs-lookup"><span data-stu-id="6553c-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="6553c-133">如需詳細資訊，請參閱 [將提供者併入應用程式](incorporating-a-provider-in-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="6553c-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="6553c-134">在 .NET Framework 中使用 WMI 建立的提供者會分離。</span><span class="sxs-lookup"><span data-stu-id="6553c-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="6553c-135">低耦合提供者支援下列提供者功能：</span><span class="sxs-lookup"><span data-stu-id="6553c-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="6553c-136">執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="6553c-137">方法提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="6553c-138">事件提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="6553c-139">事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="6553c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="6553c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6553c-141">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="6553c-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="6553c-142">提供者裝載和安全性</span><span class="sxs-lookup"><span data-stu-id="6553c-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



