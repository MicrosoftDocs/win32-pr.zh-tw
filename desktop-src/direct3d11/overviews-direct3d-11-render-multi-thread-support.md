---
title: 如何檢查驅動程式支援
description: 本主題說明如何判斷多執行緒功能 (包括建立資源，以及硬體加速) 支援的命令清單。
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990611"
---
# <a name="how-to-check-for-driver-support"></a><span data-ttu-id="08ab9-103">如何：檢查驅動程式支援</span><span class="sxs-lookup"><span data-stu-id="08ab9-103">How To: Check for Driver Support</span></span>

<span data-ttu-id="08ab9-104">本主題說明如何判斷多執行緒功能 (包括 [建立資源](overviews-direct3d-11-render-multi-thread-intro.md) ，以及硬體加速) 支援的 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md) 。</span><span class="sxs-lookup"><span data-stu-id="08ab9-104">This topic shows how to determine whether multithreading features (including [resource creation](overviews-direct3d-11-render-multi-thread-intro.md) and [command lists](overviews-direct3d-11-render-multi-thread-command-list.md)) are supported for hardware acceleration.</span></span>

<span data-ttu-id="08ab9-105">建議應用程式檢查多執行緒的圖形硬體支援。</span><span class="sxs-lookup"><span data-stu-id="08ab9-105">We recommend for applications to check for graphics hardware support of multithreading.</span></span> <span data-ttu-id="08ab9-106">如果驅動程式和圖形硬體不支援多執行緒物件建立，效能可能會以下列方式受到限制：</span><span class="sxs-lookup"><span data-stu-id="08ab9-106">If the driver and graphics hardware do not support multithreaded object creation, performance can be limited in the following ways:</span></span>

-   <span data-ttu-id="08ab9-107">同時建立多個物件 () 的不同類型可能會受到限制。</span><span class="sxs-lookup"><span data-stu-id="08ab9-107">Creating multiple objects (even of different types) at the same time might be limited.</span></span>
-   <span data-ttu-id="08ab9-108">在使用 [立即內容](overviews-direct3d-11-render-multi-thread-render.md) 呈現圖形命令時建立物件可能會受到限制。</span><span class="sxs-lookup"><span data-stu-id="08ab9-108">Creating an object while rendering graphics commands by using an [immediate context](overviews-direct3d-11-render-multi-thread-render.md) might be limited.</span></span> <span data-ttu-id="08ab9-109">例如，如果硬體不支援多執行緒處理，則應用程式應該避免在背景執行緒上建立需要很長時間才能建立的物件。</span><span class="sxs-lookup"><span data-stu-id="08ab9-109">For example, if hardware does not support multithreading, an application should avoid creating on a background thread an object that requires a very long time to create.</span></span> <span data-ttu-id="08ab9-110">需要很長時間的建立作業可以封鎖立即內容轉譯，並提高 visual 畫面播放速率斷斷續續的風險。</span><span class="sxs-lookup"><span data-stu-id="08ab9-110">A create operation that takes very long can block immediate context rendering and increase the risk of a visual frame rate stutter.</span></span>

<span data-ttu-id="08ab9-111">無論驅動程式和硬體支援為何，執行時間都支援多執行緒和命令清單;如果沒有任何 multithreads 或命令清單的驅動程式和硬體支援，則執行時間會模擬該功能。</span><span class="sxs-lookup"><span data-stu-id="08ab9-111">The runtime supports multithreading and command lists regardless of driver and hardware support; if there is no driver and hardware support for either multithreads or command lists, the runtime will emulate the functionality.</span></span> <span data-ttu-id="08ab9-112">如需多執行緒的詳細資訊，請參閱 [Direct3D 11 中的多執行緒簡介](overviews-direct3d-11-render-multi-thread-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="08ab9-112">For more information about multithreading, see [Introduction to Multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).</span></span>

<span data-ttu-id="08ab9-113">**若要檢查多執行緒的驅動程式支援：**</span><span class="sxs-lookup"><span data-stu-id="08ab9-113">**To check for driver support for multithreading:**</span></span>

1.  <span data-ttu-id="08ab9-114">初始化 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面物件。</span><span class="sxs-lookup"><span data-stu-id="08ab9-114">Initialize an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface object.</span></span> <span data-ttu-id="08ab9-115">預設會啟用多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="08ab9-115">By default, multithreading is enabled.</span></span>
2.  <span data-ttu-id="08ab9-116">呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)。</span><span class="sxs-lookup"><span data-stu-id="08ab9-116">Call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="08ab9-117">將 **D3D11 \_ 功能 \_ 執行緒** 值傳遞給 *FEATURE* 參數、將 [**D3D11 \_ 功能 \_ 資料 \_ 執行緒**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) 結構傳遞至 *pFeatureSupportData* 參數，然後將 **D3D11 \_ 功能 \_ 資料 \_ 執行緒** 結構的大小傳遞給 *FeatureSupportDataSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="08ab9-117">Pass the **D3D11\_FEATURE\_THREADING** value to the *Feature* parameter, pass the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_THREADING** structure to the *FeatureSupportDataSize* parameter.</span></span>
3.  <span data-ttu-id="08ab9-118">如果 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 方法成功，則您在上一個步驟中傳遞的 [**D3D11 \_ 功能 \_ 資料 \_ 執行緒**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) 結構將會以多執行緒支援的相關資訊來初始化。</span><span class="sxs-lookup"><span data-stu-id="08ab9-118">If the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) method succeeds, the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure that you passed in the previous step will be initialized with information about multithreading support.</span></span>
    -   <span data-ttu-id="08ab9-119">如果 **DriverConcurrentCreates** 為 **TRUE**，驅動程式可以同時建立多個資源 (在不同的執行緒上同時) 。</span><span class="sxs-lookup"><span data-stu-id="08ab9-119">If **DriverConcurrentCreates** is **TRUE**, a driver can create more than one resource at the same time (concurrently) on different threads.</span></span>

        <span data-ttu-id="08ab9-120">如果 **DriverCommandLists** 為 **TRUE**，則驅動程式支援命令清單。</span><span class="sxs-lookup"><span data-stu-id="08ab9-120">If **DriverCommandLists** is **TRUE**, the driver supports command lists.</span></span> <span data-ttu-id="08ab9-121">也就是說，直接內容所發出的轉譯命令可能會同時在不同執行緒上建立物件，而且不會有畫面播放速率斷斷續續的風險。</span><span class="sxs-lookup"><span data-stu-id="08ab9-121">That is, rendering commands issued by an immediate context can be concurrent with object creation on separate threads with low risk of a frame rate stutter.</span></span>

    -   <span data-ttu-id="08ab9-122">如果 **DriverConcurrentCreates** 為 **FALSE**，驅動程式不支援並行建立，這表示可能會有極大的平行存取量。</span><span class="sxs-lookup"><span data-stu-id="08ab9-122">If **DriverConcurrentCreates** is **FALSE**, a driver does not support concurrent creation, which means the amount of concurrency possible is extremely limited.</span></span> <span data-ttu-id="08ab9-123">圖形硬體無法在不同的執行緒 simultanueously 上建立不同類型的物件。</span><span class="sxs-lookup"><span data-stu-id="08ab9-123">The graphics hardware cannot create objects of different types on different threads simultanueously.</span></span> <span data-ttu-id="08ab9-124">此外，在圖形硬體嘗試在另一個執行緒上建立資源時，圖形硬體無法使用立即內容來發出轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="08ab9-124">Additionally, the graphics hardware cannot use an immediate context to issue render commands while the graphics hardware attempts to create a resource on another thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08ab9-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="08ab9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08ab9-126">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="08ab9-126">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="08ab9-127">多執行緒</span><span class="sxs-lookup"><span data-stu-id="08ab9-127">Multithreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




