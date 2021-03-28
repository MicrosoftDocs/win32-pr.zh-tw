---
title: Direct3D 11.4 功能
description: Direct3D 11.4 已新增下列功能。
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933397"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="f80a3-103">Direct3D 11.4 功能</span><span class="sxs-lookup"><span data-stu-id="f80a3-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="f80a3-104">Direct3D 11.4 已新增下列功能。</span><span class="sxs-lookup"><span data-stu-id="f80a3-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="f80a3-105">另請參閱 [DIRECTX SDK 的位置](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="f80a3-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="f80a3-106">移除 Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="f80a3-106">Direct3D device removal</span></span>

<span data-ttu-id="f80a3-107">[**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)和 [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved)方法是由新的介面 [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)所支援，可支援在移除 Direct3D 裝置時接收非同步事件通知。</span><span class="sxs-lookup"><span data-stu-id="f80a3-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="f80a3-108">多執行緒保護</span><span class="sxs-lookup"><span data-stu-id="f80a3-108">Multithreaded protection</span></span>

<span data-ttu-id="f80a3-109">為了確保特定的圖形命令會以特定循序執行， [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) 介面具有開啟和關閉多執行緒保護的方法，以及輸入和離開需要這項保護的關鍵程式碼的方法。</span><span class="sxs-lookup"><span data-stu-id="f80a3-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="f80a3-110">使用 Direct3D 12 進行多重裝置同步處理和交互操作的圍牆</span><span class="sxs-lookup"><span data-stu-id="f80a3-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="f80a3-111">[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence)、 [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5)和 [**ID3D11DeviceCoNtext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4)提供與 direct3d 11 的 direct3d 12 相同的隔離功能。</span><span class="sxs-lookup"><span data-stu-id="f80a3-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="f80a3-112">您可以使用「使用」來同步處理多個 Direct3D11 裝置，以及針對 Direct3D 11 和 Direct3D 12 之間的 interop。</span><span class="sxs-lookup"><span data-stu-id="f80a3-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="f80a3-113">Windows 10 Creators Update 支援的。</span><span class="sxs-lookup"><span data-stu-id="f80a3-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="f80a3-114">外延 NV12 材質支援</span><span class="sxs-lookup"><span data-stu-id="f80a3-114">Extended NV12 texture support</span></span>

<span data-ttu-id="f80a3-115">具有 capture 和影片編碼功能的 NV12 紋理現在支援共用。</span><span class="sxs-lookup"><span data-stu-id="f80a3-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="f80a3-116">適用于影片編碼和捕捉的較舊 D3D11 材質旗標已被取代為 NV12，因為它會在新驅動程式的所有時間進行設定。</span><span class="sxs-lookup"><span data-stu-id="f80a3-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="f80a3-117">這類紋理不僅可以與 D3D11 共用，也可與 D3D12 共用。</span><span class="sxs-lookup"><span data-stu-id="f80a3-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="f80a3-118">在 D3D12 中，沒有任何新的旗標代表這些材質功能。</span><span class="sxs-lookup"><span data-stu-id="f80a3-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="f80a3-119">請參閱 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4)中的布林值設定。</span><span class="sxs-lookup"><span data-stu-id="f80a3-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="f80a3-120">著色器快取</span><span class="sxs-lookup"><span data-stu-id="f80a3-120">Shader Caching</span></span>

<span data-ttu-id="f80a3-121">驅動程式在 Windows 10 建立者更新中，可能支援作業系統管理的 Direct3D11 應用程式的著色器快取。</span><span class="sxs-lookup"><span data-stu-id="f80a3-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f80a3-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="f80a3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f80a3-123">Direct3D 11 的新功能</span><span class="sxs-lookup"><span data-stu-id="f80a3-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 