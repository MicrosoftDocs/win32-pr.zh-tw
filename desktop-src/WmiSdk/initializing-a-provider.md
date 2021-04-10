---
description: 您必須為提供者撰寫程式碼的第一項工作就是初始化程式，其中涵蓋了提供者必須執行的任何工作，讓它能夠從 WMI 傳送和接收資訊、控制受管理物件，以及執行其他工作。
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: 初始化提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852635"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="053af-103">初始化提供者</span><span class="sxs-lookup"><span data-stu-id="053af-103">Initializing a Provider</span></span>

<span data-ttu-id="053af-104">您必須為提供者撰寫程式碼的第一項工作就是初始化程式，其中涵蓋了提供者必須執行的任何工作，讓它能夠從 WMI 傳送和接收資訊、控制受管理物件，以及執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="053af-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="053af-105">每一種類型的提供者都有一組不同的工作必須執行，而且有一組隨附的唯一介面。</span><span class="sxs-lookup"><span data-stu-id="053af-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="053af-106">不過，所有提供者都會透過 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面初始化，並透過 [**IWBEMPROVIDERINITSINK**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) 介面通知 WMI 其初始化狀態。</span><span class="sxs-lookup"><span data-stu-id="053af-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="053af-107">下列程式描述如何初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="053af-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="053af-108">**初始化提供者**</span><span class="sxs-lookup"><span data-stu-id="053af-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="053af-109">為您的提供者執行 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) 。</span><span class="sxs-lookup"><span data-stu-id="053af-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="053af-110">當 WMI 判斷用戶端需要提供者的服務時，WMI 會藉由呼叫 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) 方法來載入提供者。</span><span class="sxs-lookup"><span data-stu-id="053af-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="053af-111">針對您的提供者類型，執行任何獨特的介面。</span><span class="sxs-lookup"><span data-stu-id="053af-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="053af-112">藉由呼叫 [**IWbemProviderInitSink：： SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)，告知 WMI 您的提供者已完成初始化。</span><span class="sxs-lookup"><span data-stu-id="053af-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="053af-113">[**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)的所有執行都必須呼叫 [**IWbemProviderInitSink：： SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) ，才能向 WMI 報告初始化狀態。</span><span class="sxs-lookup"><span data-stu-id="053af-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="053af-114">**SetStatus** 方法可讓 WMI 判斷提供者是否已準備好接收要求，以及提供者已準備好接收的要求類型。</span><span class="sxs-lookup"><span data-stu-id="053af-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="053af-115">下列程式說明如何報告初始化成功。</span><span class="sxs-lookup"><span data-stu-id="053af-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="053af-116">**若要報告初始化成功**</span><span class="sxs-lookup"><span data-stu-id="053af-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="053af-117">將 [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)的 *IStatus* 參數設定為 **已 \_ \_ 初始化的 WBEM S**。</span><span class="sxs-lookup"><span data-stu-id="053af-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="053af-118">藉由傳回已 **\_ \_ 初始化的 WBEM**，提供者表示已準備好處理來自應用程式、WMI 和其他提供者的要求。</span><span class="sxs-lookup"><span data-stu-id="053af-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="053af-119">在接收 WBEM \_ \_ 初始化之後，WMI 會對提供者呼叫 [**IWbemProviderInit：： QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 方法。</span><span class="sxs-lookup"><span data-stu-id="053af-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="053af-120">此查詢會捕獲提供者主要介面的指標。</span><span class="sxs-lookup"><span data-stu-id="053af-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="053af-121">下列程式描述如何在初始化期間報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="053af-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="053af-122">**若要在初始化期間報告錯誤**</span><span class="sxs-lookup"><span data-stu-id="053af-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="053af-123">將 [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)的 *IStatus* 參數設定為 **WBEM \_ E \_ 失敗**。</span><span class="sxs-lookup"><span data-stu-id="053af-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="053af-124">傳回 WBEM E 的 WMI 視圖提供者 **\_ \_ 無法** 正常運作。</span><span class="sxs-lookup"><span data-stu-id="053af-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="053af-125">Wmi 在取得提供者的主要介面指標或初始化失敗之後，就會釋放 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 指標。</span><span class="sxs-lookup"><span data-stu-id="053af-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="053af-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="053af-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="053af-127">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="053af-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="053af-128">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="053af-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="053af-129">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="053af-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



