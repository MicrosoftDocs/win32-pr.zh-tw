---
title: 建立變形和參考裝置的限制
description: 在 Direct3D 10.1 和 Direct3D 11.0 中建立變形和參考裝置有一些限制。 本主題討論這些限制。
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315196"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="cf5d5-104">建立變形和參考裝置的限制</span><span class="sxs-lookup"><span data-stu-id="cf5d5-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="cf5d5-105">在 Direct3D 10.1 和 Direct3D 11.0 中建立變形和參考裝置有一些限制。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="cf5d5-106">本主題討論這些限制。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="cf5d5-107">D3D10 \_ 驅動程式 \_ 類型的 \_ 變形和 D3D10 驅動程式類型參考驅動程式類型在 \_ \_ \_ \_ Direct3D 10.1 的 D3D10 功能等級 \_ \_ 9 \_ 1 到 D3D10 \_ 功能等級 \_ \_ 9 \_ 3 功能層級上不受支援。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="cf5d5-108">此外， \_ \_ \_ \_ DIRECT3D 11.0 中的 d3d 功能 \_ 等級 \_ 11 0 不支援 d3d 驅動程式類型變形驅動程式類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="cf5d5-109">也就是說，當您呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) 來建立 direct3d 10.1 裝置，或當您呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 來建立 direct3d 11.0 裝置時，如果您在呼叫中指定這些驅動程式類型的其中一個，且其中一個功能等級的組合是不正確，則呼叫無效。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="cf5d5-110">只有下列功能層級、執行時間和驅動程式類型組合適用于變形和參考裝置：</span><span class="sxs-lookup"><span data-stu-id="cf5d5-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="cf5d5-111">\_ \_ \_ Direct3D 11.1 中所有功能層級的 D3D 驅動程式類型變形，Windows 8 包含</span><span class="sxs-lookup"><span data-stu-id="cf5d5-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="cf5d5-112">\_ \_ \_ Direct3D 11.1 中所有功能層級的 D3D 驅動程式類型參考</span><span class="sxs-lookup"><span data-stu-id="cf5d5-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="cf5d5-113">當您呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 來建立 Direct3D 11.1 裝置時，如果您將其中一個驅動程式類型的組合指定為其中一個功能層級，則呼叫會是有效的。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="cf5d5-114">D3d \_ 驅動程式 \_ 類型 \_ 在 d3d \_ 功能 \_ 層級 9 1 到 d3d 功能層級上的變形（ \_ \_ \_ \_ \_ \_ Direct3D 11 的功能等級為 10 1）</span><span class="sxs-lookup"><span data-stu-id="cf5d5-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="cf5d5-115">\_ \_ \_ Direct3D 11 中的 d3d 驅動程式類型參考在 d3d 功能層 \_ \_ 級 \_ 9 \_ 1 到 d3d 功能 \_ \_ 等級 \_ 11 \_ 0 功能等級</span><span class="sxs-lookup"><span data-stu-id="cf5d5-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="cf5d5-116">當您呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 來建立 Direct3D 11 裝置時，如果您將其中一個驅動程式類型的組合指定為其中一個功能層級，則呼叫會是有效的。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="cf5d5-117">\_ \_ \_ \_ \_ \_ 在 \_ \_ \_ \_ \_ \_ \_ Direct3D 10.1 中透過 D3D10 功能等級 10 \_ 1 的功能層級 10 0 上的 D3D10 功能層級 10 0 D3D10 驅動程式類型的變形與 D3D10 驅動程式類型參考</span><span class="sxs-lookup"><span data-stu-id="cf5d5-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="cf5d5-118">當您呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) 來建立 Direct3D 10.1 裝置時，如果您將其中一個驅動程式類型的組合指定為其中一個功能層級，則呼叫會是有效的。</span><span class="sxs-lookup"><span data-stu-id="cf5d5-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf5d5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf5d5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf5d5-120">裝置</span><span class="sxs-lookup"><span data-stu-id="cf5d5-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="cf5d5-121">舊版硬體上的 Direct3D 11 簡介</span><span class="sxs-lookup"><span data-stu-id="cf5d5-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="cf5d5-122">如何：建立變形裝置</span><span class="sxs-lookup"><span data-stu-id="cf5d5-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="cf5d5-123">如何：建立參考裝置</span><span class="sxs-lookup"><span data-stu-id="cf5d5-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="cf5d5-124">**D3D10 \_ 驅動程式 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="cf5d5-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="cf5d5-125">**D3D10 功能 1-1 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf5d5-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="cf5d5-126">**D3D \_ 驅動程式 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="cf5d5-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="cf5d5-127">**D3D \_ 功能 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="cf5d5-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 