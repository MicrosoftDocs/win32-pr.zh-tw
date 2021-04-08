---
title: 開發 RPC Windows 應用程式
description: 當您安裝 (SDK) 的平臺軟體發展工具組時，會自動安裝下列 RPC 開發環境、執行時間程式庫和工具。
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023983"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="4452d-103">開發 RPC Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="4452d-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="4452d-104">當您安裝 (SDK) 的平臺軟體發展工具組時，會自動安裝下列 RPC 開發環境、執行時間程式庫和工具：</span><span class="sxs-lookup"><span data-stu-id="4452d-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="4452d-105">C/c + + 語言標頭 (。H) 檔案</span><span class="sxs-lookup"><span data-stu-id="4452d-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="4452d-106">RPC 匯入程式庫 ( .lib) 檔案</span><span class="sxs-lookup"><span data-stu-id="4452d-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="4452d-107">範例程式</span><span class="sxs-lookup"><span data-stu-id="4452d-107">Sample programs</span></span>
-   <span data-ttu-id="4452d-108">RPC 參考說明檔</span><span class="sxs-lookup"><span data-stu-id="4452d-108">RPC reference Help files</span></span>
-   <span data-ttu-id="4452d-109">**Uuidgen.exe** 公用程式</span><span class="sxs-lookup"><span data-stu-id="4452d-109">The **uuidgen** utility</span></span>

<span data-ttu-id="4452d-110">當您安裝 Windows 時，會安裝下列各項：</span><span class="sxs-lookup"><span data-stu-id="4452d-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="4452d-111">RPC 執行時間 Dll</span><span class="sxs-lookup"><span data-stu-id="4452d-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="4452d-112">Windows Vista 和更新版本不支援 Microsoft 定位器 () </span><span class="sxs-lookup"><span data-stu-id="4452d-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="4452d-113">RPC 端點對應服務</span><span class="sxs-lookup"><span data-stu-id="4452d-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="4452d-114">下列 RPC 匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="4452d-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="4452d-115">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="4452d-115">Import library</span></span> | <span data-ttu-id="4452d-116">Description</span><span class="sxs-lookup"><span data-stu-id="4452d-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="4452d-117">Rpcns4 .lib</span><span class="sxs-lookup"><span data-stu-id="4452d-117">Rpcns4.lib</span></span>     | <span data-ttu-id="4452d-118">名稱-服務函數</span><span class="sxs-lookup"><span data-stu-id="4452d-118">Name-service functions</span></span>     |
| <span data-ttu-id="4452d-119">Rpcrt4 .lib</span><span class="sxs-lookup"><span data-stu-id="4452d-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="4452d-120">Windows 執行時間函數</span><span class="sxs-lookup"><span data-stu-id="4452d-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="4452d-121">Rpcns4 已淘汰，不再支援。</span><span class="sxs-lookup"><span data-stu-id="4452d-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="4452d-122">下列 RPC 程式庫隨附于下層支援。</span><span class="sxs-lookup"><span data-stu-id="4452d-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="4452d-123">動態連結程式庫</span><span class="sxs-lookup"><span data-stu-id="4452d-123">Dynamic-link library</span></span> | <span data-ttu-id="4452d-124">說明</span><span class="sxs-lookup"><span data-stu-id="4452d-124">Description</span></span>                 | <span data-ttu-id="4452d-125">平台</span><span class="sxs-lookup"><span data-stu-id="4452d-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="4452d-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="4452d-127">用戶端具名管道傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-127">Client named-pipe transport</span></span> | <span data-ttu-id="4452d-128">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-129">Rpclts1.dll</span></span>          | <span data-ttu-id="4452d-130">伺服器具名管道傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-130">Server named-pipe transport</span></span> | <span data-ttu-id="4452d-131">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="4452d-133">用戶端 TCP/IP 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="4452d-134">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-135">Rpclts3.dll</span></span>          | <span data-ttu-id="4452d-136">伺服器 TCP/IP 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="4452d-137">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="4452d-139">用戶端 NetBIOS 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="4452d-140">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-141">Rpclts5.dll</span></span>          | <span data-ttu-id="4452d-142">伺服器 NetBIOS 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="4452d-143">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="4452d-145">用戶端 SPX 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-145">Client SPX transport</span></span>        | <span data-ttu-id="4452d-146">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-147">Rpclts6.dll</span></span>          | <span data-ttu-id="4452d-148">伺服器 SPX 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-148">Server SPX transport</span></span>        | <span data-ttu-id="4452d-149">Windows NT、Windows 98、Windows 95</span><span class="sxs-lookup"><span data-stu-id="4452d-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="4452d-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="4452d-151">用戶端 IPX 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-151">Client IPX transport</span></span>        | <span data-ttu-id="4452d-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="4452d-152">Windows NT</span></span>                         |
| <span data-ttu-id="4452d-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="4452d-154">伺服器 IPX 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-154">Server IPX transport</span></span>        | <span data-ttu-id="4452d-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="4452d-155">Windows NT</span></span>                         |
| <span data-ttu-id="4452d-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="4452d-157">用戶端 UDP 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-157">Client UDP transport</span></span>        | <span data-ttu-id="4452d-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="4452d-158">Windows NT</span></span>                         |
| <span data-ttu-id="4452d-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="4452d-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="4452d-160">伺服器 UDP 傳輸</span><span class="sxs-lookup"><span data-stu-id="4452d-160">Server UDP transport</span></span>        | <span data-ttu-id="4452d-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="4452d-161">Windows NT</span></span>                         |



 

<span data-ttu-id="4452d-162">您也將需要 Microsoft 介面定義語言 (MIDL) 編譯器。</span><span class="sxs-lookup"><span data-stu-id="4452d-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="4452d-163">如需詳細資訊，請參閱 [使用 MIDL 編譯器](/windows/desktop/Midl/using-the-midl-compiler-2)。</span><span class="sxs-lookup"><span data-stu-id="4452d-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 