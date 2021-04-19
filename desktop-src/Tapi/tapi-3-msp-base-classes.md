---
description: 本檔說明 MSP 基類的設計和使用。 這些類別並不是必要的，但大部分的開發人員會發現它們簡化了針對 TAPI 3 秒新 MSPI 建立 DirectShow 型 MSP 的工作。
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: TAPI 3 MSP 基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987776"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="6be78-104">TAPI 3 MSP 基類</span><span class="sxs-lookup"><span data-stu-id="6be78-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="6be78-105">本檔說明 MSP 基類的設計和使用。</span><span class="sxs-lookup"><span data-stu-id="6be78-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="6be78-106">這些類別並不是必要的，但大部分的開發人員會發現它們簡化了針對 TAPI 3 的新 MSPI 建立 DirectShow 型 MSP 的工作。</span><span class="sxs-lookup"><span data-stu-id="6be78-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="6be78-107">MSP 基礎類別的原始程式碼可在平臺軟體發展工具組 (SDK) 的範例目錄中找到。</span><span class="sxs-lookup"><span data-stu-id="6be78-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="6be78-108">假設您熟悉 COM、ATL、DirectShow 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="6be78-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="6be78-109">讀者也必須知道 [媒體服務提供者 (MSP) ](about-the-media-service-provider-msp-.md) 和 [媒體服務提供者介面 (MSPI) ](media-service-provider-interface-mspi-.md)中的一般內容。</span><span class="sxs-lookup"><span data-stu-id="6be78-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="6be78-110">Windows 2000 需要 ATL 2.1。</span><span class="sxs-lookup"><span data-stu-id="6be78-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="6be78-111">從 Windows XP 開始，ATL 2.1 和3.0 都會編譯。</span><span class="sxs-lookup"><span data-stu-id="6be78-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="6be78-112"> (可以在 SDK) 中取得 MSP 基礎類別庫：</span><span class="sxs-lookup"><span data-stu-id="6be78-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="6be78-113">Mspbase .lib</span><span class="sxs-lookup"><span data-stu-id="6be78-113">Mspbase.lib</span></span>
-   <span data-ttu-id="6be78-114">Mspid .lib</span><span class="sxs-lookup"><span data-stu-id="6be78-114">Mspid.lib</span></span>
-   <span data-ttu-id="6be78-115">Strmbase .lib</span><span class="sxs-lookup"><span data-stu-id="6be78-115">Strmbase.lib</span></span>
-   <span data-ttu-id="6be78-116">Tmuid .lib</span><span class="sxs-lookup"><span data-stu-id="6be78-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="6be78-117">應該使用動態而非靜態連結。</span><span class="sxs-lookup"><span data-stu-id="6be78-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="6be78-118"> (在 SDK) 提供的 MSP 基類標頭檔：</span><span class="sxs-lookup"><span data-stu-id="6be78-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="6be78-119">Mspaddr。h</span><span class="sxs-lookup"><span data-stu-id="6be78-119">Mspaddr.h</span></span>
-   <span data-ttu-id="6be78-120">Mspbase。h</span><span class="sxs-lookup"><span data-stu-id="6be78-120">Mspbase.h</span></span>
-   <span data-ttu-id="6be78-121">Mspcall。h</span><span class="sxs-lookup"><span data-stu-id="6be78-121">Mspcall.h</span></span>
-   <span data-ttu-id="6be78-122">Msplog。h</span><span class="sxs-lookup"><span data-stu-id="6be78-122">Msplog.h</span></span>
-   <span data-ttu-id="6be78-123">Mspstrm。h</span><span class="sxs-lookup"><span data-stu-id="6be78-123">Mspstrm.h</span></span>
-   <span data-ttu-id="6be78-124">Mspterm。h</span><span class="sxs-lookup"><span data-stu-id="6be78-124">Mspterm.h</span></span>
-   <span data-ttu-id="6be78-125">Mspthrd。h</span><span class="sxs-lookup"><span data-stu-id="6be78-125">Mspthrd.h</span></span>
-   <span data-ttu-id="6be78-126">Msptmac。h</span><span class="sxs-lookup"><span data-stu-id="6be78-126">Msptmac.h</span></span>
-   <span data-ttu-id="6be78-127">Msptmvc。h</span><span class="sxs-lookup"><span data-stu-id="6be78-127">Msptmvc.h</span></span>
-   <span data-ttu-id="6be78-128">Msptrmvc。h</span><span class="sxs-lookup"><span data-stu-id="6be78-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="6be78-129">Msptrmac。h</span><span class="sxs-lookup"><span data-stu-id="6be78-129">Msptrmac.h</span></span>
-   <span data-ttu-id="6be78-130">Msptrmar。h</span><span class="sxs-lookup"><span data-stu-id="6be78-130">Msptrmar.h</span></span>
-   <span data-ttu-id="6be78-131">Msputils。h</span><span class="sxs-lookup"><span data-stu-id="6be78-131">Msputils.h</span></span>

<span data-ttu-id="6be78-132"> (可在 SDK 範例中使用的 MSP 基礎類別來源檔案) ：</span><span class="sxs-lookup"><span data-stu-id="6be78-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="6be78-133">Mspaddr .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="6be78-134">Mspcall .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="6be78-135">Msplog .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-135">Msplog.cpp</span></span>
-   <span data-ttu-id="6be78-136">Mspstrm .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="6be78-137">Mspterm .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="6be78-138">Mspthrd .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="6be78-139">Msptrmac .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="6be78-140">Msptrmar .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="6be78-141">Msptrmvc .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="6be78-142">Msputils .cpp</span><span class="sxs-lookup"><span data-stu-id="6be78-142">Msputils.cpp</span></span>

 

 



