---
title: WFP 架構
description: 本節提供 Windows 篩選平台架構的簡短總覽。
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185924"
---
# <a name="wfp-architecture"></a><span data-ttu-id="fc6b5-103">WFP 架構</span><span class="sxs-lookup"><span data-stu-id="fc6b5-103">WFP Architecture</span></span>

<span data-ttu-id="fc6b5-104">下圖顯示 Windows 篩選平台 (WFP) 的基本架構。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![windows 篩選平臺圖表的基本架構](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="fc6b5-106">篩選引擎</span><span class="sxs-lookup"><span data-stu-id="fc6b5-106">Filter Engine</span></span>

<span data-ttu-id="fc6b5-107">篩選引擎包含使用者模式元件和核心模式元件，可共同執行網路資料的所有篩選作業。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="fc6b5-108">篩選引擎包含多個篩選層，這些層級會鬆散對應到作業系統的網路堆疊層。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="fc6b5-109">篩選引擎圖層會根據擁有這些層級的篩選引擎元件，分成使用者模式層和核心模式層。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="fc6b5-110">使用者模式元件會執行 RPC 和 IPsec 篩選。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="fc6b5-111">篩選引擎包含大約10個使用者模式篩選層。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="fc6b5-112">核心模式元件會在 TC/IP 堆疊的網路和傳輸層執行篩選。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="fc6b5-113">此元件也會在 [分類](basic-operation.md) 程式期間呼叫可用的標注函數。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="fc6b5-114">篩選引擎包含大約50的核心模式篩選層。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="fc6b5-115">請參閱 [**篩選圖層識別碼**](management-filtering-layer-identifiers-.md) ，以取得每個篩選引擎層的描述。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="fc6b5-116">基礎篩選引擎</span><span class="sxs-lookup"><span data-stu-id="fc6b5-116">Base Filtering Engine</span></span>

<span data-ttu-id="fc6b5-117">基底篩選引擎 (BFE) 是一種使用者模式服務， (bfe.dll 在協調 WFP 元件的 svchost.exe 進程) 中執行。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="fc6b5-118">BFE 執行的主要工作包括從系統新增和移除篩選、儲存篩選器設定，以及強制執行 WFP 設定安全性。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="fc6b5-119">應用程式會透過 [WFP 管理功能](fwp-mgmt-functions.md)與 BFE 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="fc6b5-120">標注驅動程式</span><span class="sxs-lookup"><span data-stu-id="fc6b5-120">Callout Drivers</span></span>

<span data-ttu-id="fc6b5-121">注標驅動程式提供額外的篩選功能，方法是將自訂注標函數新增至篩選引擎的一或多個核心模式篩選層。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="fc6b5-122">標注支援深度檢查和封包以及資料流程修改。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="fc6b5-123">在標注驅動程式將其標注函式新增至篩選引擎之後，就可以將指定驅動程式注標函數的篩選加入至篩選程式。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="fc6b5-124">使用者模式管理應用程式或標注驅動程式本身可以新增這類篩選。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="fc6b5-125">在 Windows 開發工具組中提供的核心模式介面，應該只在需要時使用，而不是用來取代使用者模式 API。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="fc6b5-126">如需有關 callout 驅動程式的詳細資訊，請參閱 [Windows 開發工具組](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)的 Windows 篩選平台一節。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="fc6b5-127">Windows 篩選平台包含一些內建的 callout 函式，可用於 IPsec 安全資料通訊、可設定狀態的篩選設定，以及隱形模式篩選。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="fc6b5-128">如需內建標注函式的完整清單，請參閱 [**內建的標注識別碼**](built-in-callout-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="fc6b5-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc6b5-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc6b5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc6b5-130">物件模型</span><span class="sxs-lookup"><span data-stu-id="fc6b5-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="fc6b5-131">WFP 操作</span><span class="sxs-lookup"><span data-stu-id="fc6b5-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="fc6b5-132">Windows 篩選平台標注驅動程式-設計指南</span><span class="sxs-lookup"><span data-stu-id="fc6b5-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="fc6b5-133">Windows 篩選平台標注驅動程式-參考</span><span class="sxs-lookup"><span data-stu-id="fc6b5-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 