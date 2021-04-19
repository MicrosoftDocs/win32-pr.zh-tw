---
description: 執行個體提供者會提供一個或多個指定類別的實例。
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: 撰寫執行個體提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982487"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="f7694-103">撰寫執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="f7694-103">Writing an Instance Provider</span></span>

<span data-ttu-id="f7694-104">執行個體提供者會提供一個或多個指定類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f7694-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="f7694-105">例如，執行個體提供者可以提供 CPU 或其他硬體類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7694-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="f7694-106">因為執行個體提供者所管理的物件通常會定期變更，所以所有執行個體提供者都會被視為提取提供者;亦即，每當 WMI 提出資訊要求時，就會動態抓取有關受管理物件的資訊的提供者。</span><span class="sxs-lookup"><span data-stu-id="f7694-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="f7694-107">此名稱來自于 WMI 「提取」來自提供者的資訊，代表用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="f7694-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="f7694-108">使用提取技術時，執行個體提供者可以支援特定實例的抓取、列舉、修改、刪除和查詢處理。</span><span class="sxs-lookup"><span data-stu-id="f7694-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="f7694-109">高效能的提供者可以提高執行個體提供者的效率，或以程式設計方式存取系統監視器中顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="f7694-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="f7694-110">如需詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供](making-an-instance-provider-into-a-high-performance-provider.md)者。</span><span class="sxs-lookup"><span data-stu-id="f7694-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="f7694-111">下列程式描述如何撰寫執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="f7694-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="f7694-112">**若要撰寫執行個體提供者**</span><span class="sxs-lookup"><span data-stu-id="f7694-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="f7694-113">向[WMI 註冊您的提供者](registering-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="f7694-114">執行個體提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別，向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="f7694-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="f7694-115">[初始化您的提供者](initializing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="f7694-116">WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="f7694-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="f7694-117">這是所有提供者通用的工作。</span><span class="sxs-lookup"><span data-stu-id="f7694-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="f7694-118">強烈建議您使用執行個體提供者來使用多執行緒模型「兩者」。</span><span class="sxs-lookup"><span data-stu-id="f7694-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="f7694-119">[為您的提供者執行 IWbemServices 介面](implementing-the-primary-interface-for-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="f7694-120">[**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面是執行個體提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="f7694-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="f7694-121">加入提供者所需的任何其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="f7694-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="f7694-122">設計您的提供者時，您很可能需要呼叫 WMI 介面。</span><span class="sxs-lookup"><span data-stu-id="f7694-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="f7694-123">如需詳細資訊，請參閱 [進行 WMI 的呼叫](making-calls-to-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="f7694-124">取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="f7694-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="f7694-125">如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="f7694-126">如有必要，請 [執行高效能介面](improving-the-efficiency-of-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="f7694-127">高效能介面可增加提供者回應 WMI 要求的速度。</span><span class="sxs-lookup"><span data-stu-id="f7694-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="f7694-128">如有必要，請 [執行部分實例更新的支援](supporting-partial-instance-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="f7694-129">顧名思義，部分實例更新是用來只更新部分實例的技巧。</span><span class="sxs-lookup"><span data-stu-id="f7694-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="f7694-130">如需從用戶端呼叫部分實例的詳細資訊，請參閱 [更新部分的實例](updating-part-of-an-instance.md) 和 [取出 WMI 實例的一部分](retrieving-part-of-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="f7694-131">以您的新程式碼取代預先存在的提供者。</span><span class="sxs-lookup"><span data-stu-id="f7694-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="f7694-132">如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="f7694-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="f7694-133">如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f7694-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



