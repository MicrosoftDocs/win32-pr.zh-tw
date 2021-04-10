---
title: 網路管理函數緩衝區
description: RPC 執行時間程式庫會處理32位資料抓取網路管理功能所需的緩衝區，如下所示。
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183647"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="ed3db-103">網路管理函數緩衝區</span><span class="sxs-lookup"><span data-stu-id="ed3db-103">Network Management Function Buffers</span></span>

<span data-ttu-id="ed3db-104">RPC 執行時間程式庫會處理32位資料抓取網路管理功能所需的緩衝區，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ed3db-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="ed3db-105">**將資料傳送至伺服器** (\[) 參數中所指定的資料 \] 。</span><span class="sxs-lookup"><span data-stu-id="ed3db-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="ed3db-106">呼叫端必須配置和解除配置相關資訊結構 (或結構) 的緩衝區，並將指標變數傳遞給函式。</span><span class="sxs-lookup"><span data-stu-id="ed3db-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="ed3db-107">呼叫端不需要指定緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="ed3db-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="ed3db-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="ed3db-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="ed3db-109">**從伺服器抓取資料** (out 參數所指定的資料 \[ \]) 。</span><span class="sxs-lookup"><span data-stu-id="ed3db-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="ed3db-110">系統會為傳回的資訊配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ed3db-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="ed3db-111">呼叫端必須將指標變數傳遞給輸入上的函式。</span><span class="sxs-lookup"><span data-stu-id="ed3db-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="ed3db-112">在成功傳回時，指標會收到系統組態的緩衝區位址，其中包含傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="ed3db-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="ed3db-113">這麼做可簡化呼叫程式碼，因為呼叫端不需要估計緩衝區大小，也不需要調整緩衝區大小，然後重新發出函數。</span><span class="sxs-lookup"><span data-stu-id="ed3db-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="ed3db-114">當呼叫端處理傳回的資訊之後，它必須藉由呼叫 [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) 函式來釋放系統組態的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ed3db-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="ed3db-115">如需有關指定緩衝區大小的詳細資訊，請參閱 [網路管理函數緩衝區長度](network-management-function-buffer-lengths.md)。</span><span class="sxs-lookup"><span data-stu-id="ed3db-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="ed3db-116">範例： [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="ed3db-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 




