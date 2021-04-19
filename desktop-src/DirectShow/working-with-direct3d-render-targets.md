---
description: 使用 Direct3D 轉譯目標
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: 使用 Direct3D 轉譯目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8aca19082c5db9521cfc1c7341fd74c98270cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993016"
---
# <a name="working-with-direct3d-render-targets"></a><span data-ttu-id="c01fa-103">使用 Direct3D 轉譯目標</span><span class="sxs-lookup"><span data-stu-id="c01fa-103">Working with Direct3D Render Targets</span></span>

<span data-ttu-id="c01fa-104">許多適用于 Direct3D 轉譯目標的媒體子類型都定義為與 VMR-7 和 VMR-9 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c01fa-104">Several media subtypes for Direct3D render targets are defined for use with the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="c01fa-105">當上游篩選準則向其中一個子類型提出連接時，會向 VMR 指出要在 Direct3D 轉譯目標上執行轉譯。</span><span class="sxs-lookup"><span data-stu-id="c01fa-105">When an upstream filter proposes a connection with one of these subtypes, it indicates to the VMR that the rendering is to be performed on a Direct3D render target.</span></span> <span data-ttu-id="c01fa-106">若為 VMR-7，這會是 DirectX 7 Direct3D 轉譯目標，而針對 VMR-9，這會是 DirectX 9 Direct3D 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="c01fa-106">For VMR-7, this will be a DirectX 7 Direct3D render target, and for VMR-9 this will be a DirectX 9 Direct3D render target.</span></span> <span data-ttu-id="c01fa-107">如果 VMR 處於混合模式，介面也會是 Direct3D 材質介面。</span><span class="sxs-lookup"><span data-stu-id="c01fa-107">If the VMR is in mixing mode, the surface will also be a Direct3D texture surface.</span></span> <span data-ttu-id="c01fa-108">如果 VMR 不在混合模式中，則介面會是一般的 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="c01fa-108">If the VMR is not in mixing mode, the surface will be a regular Direct3D surface.</span></span> <span data-ttu-id="c01fa-109">只有在 VMR 為混合模式時，才支援 ARGB 像素格式。</span><span class="sxs-lookup"><span data-stu-id="c01fa-109">The ARGB pixel formats are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="c01fa-110">轉譯目標子類型為：</span><span class="sxs-lookup"><span data-stu-id="c01fa-110">The render target subtypes are:</span></span>



| <span data-ttu-id="c01fa-111">VMR-7</span><span class="sxs-lookup"><span data-stu-id="c01fa-111">VMR-7</span></span>                                | <span data-ttu-id="c01fa-112">VMR-9</span><span class="sxs-lookup"><span data-stu-id="c01fa-112">VMR-9</span></span>                                |
|--------------------------------------|--------------------------------------|
| <span data-ttu-id="c01fa-113">MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-113">MEDIASUBTYPE\_RGB32\_D3D\_DX7\_RT</span></span>    | <span data-ttu-id="c01fa-114">MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-114">MEDIASUBTYPE\_RGB32\_D3D\_DX9\_RT</span></span>    |
| <span data-ttu-id="c01fa-115">MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-115">MEDIASUBTYPE\_RGB16\_D3D\_DX7\_RT</span></span>    | <span data-ttu-id="c01fa-116">MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-116">MEDIASUBTYPE\_RGB16\_D3D\_DX9\_RT</span></span>    |
| <span data-ttu-id="c01fa-117">MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-117">MEDIASUBTYPE\_ARGB32\_D3D\_DX7\_RT</span></span>   | <span data-ttu-id="c01fa-118">MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-118">MEDIASUBTYPE\_ARGB32\_D3D\_DX9\_RT</span></span>   |
| <span data-ttu-id="c01fa-119">MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-119">MEDIASUBTYPE\_ARGB4444\_D3D\_DX7\_RT</span></span> | <span data-ttu-id="c01fa-120">MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-120">MEDIASUBTYPE\_ARGB4444\_D3D\_DX9\_RT</span></span> |
| <span data-ttu-id="c01fa-121">MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-121">MEDIASUBTYPE\_ARGB1555\_D3D\_DX7\_RT</span></span> | <span data-ttu-id="c01fa-122">MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT</span><span class="sxs-lookup"><span data-stu-id="c01fa-122">MEDIASUBTYPE\_ARGB1555\_D3D\_DX9\_RT</span></span> |



 

<span data-ttu-id="c01fa-123">這些類型定義于標頭檔 uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="c01fa-123">These types are defined in the header file uuids.h.</span></span> <span data-ttu-id="c01fa-124">MEDIASUBTYPE \_ RGB32 媒體類型是 RGBx888 格式，而 MEDIASUBTYPE \_ RGB16 媒體類型是 RGB565 格式。</span><span class="sxs-lookup"><span data-stu-id="c01fa-124">The MEDIASUBTYPE\_RGB32 media types are an RGBx888 format and MEDIASUBTYPE\_RGB16 media types are an RGB565 format.</span></span> <span data-ttu-id="c01fa-125">如需這些像素格式的詳細資訊，請參閱 DirectX 圖形檔。</span><span class="sxs-lookup"><span data-stu-id="c01fa-125">For more information on these pixel formats, see the DirectX Graphics documentation.</span></span>

<span data-ttu-id="c01fa-126">**要求未鎖定的介面**</span><span class="sxs-lookup"><span data-stu-id="c01fa-126">**Requesting an Unlocked Surface**</span></span>

<span data-ttu-id="c01fa-127">鎖定和解除鎖定 DirectDraw 介面是計算成本高昂的作業。</span><span class="sxs-lookup"><span data-stu-id="c01fa-127">Locking and unlocking DirectDraw surfaces are computationally expensive operations.</span></span> <span data-ttu-id="c01fa-128">使用 Direct3D 轉譯目標媒體子類型時，上游篩選器需要將介面解除鎖定，才能在圖形硬體上操作。</span><span class="sxs-lookup"><span data-stu-id="c01fa-128">When using the Direct3D render target media subtypes, the upstream filter needs the surfaces to be unlocked so that it can operate on them with the graphics hardware.</span></span> <span data-ttu-id="c01fa-129">為了避免不必要的鎖定解除鎖定作業，VMR 會在 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法（AM GBF NODDSURFACELOCK）上支援新的旗標，該旗標會 \_ 指示 VMR 在將 \_ 範例傳遞給上游篩選之前，不鎖定 DirectDraw 介面。</span><span class="sxs-lookup"><span data-stu-id="c01fa-129">To avoid an unnecessary locking-unlocking operation, the VMR supports a new flag on the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, AM\_GBF\_NODDSURFACELOCK, that instructs the VMR not to lock the DirectDraw surface before passing a sample to the upstream filter.</span></span> <span data-ttu-id="c01fa-130">使用這個旗標時， [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 的呼叫將會失敗，因為沒有鎖定的指標。</span><span class="sxs-lookup"><span data-stu-id="c01fa-130">When this flag is used, calls to [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) will fail because there is no locked pointer.</span></span> <span data-ttu-id="c01fa-131">若要取得 DirectDraw 介面的存取權，篩選準則必須在傳回的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)物件上呼叫 **QueryInterface** ，並要求 [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface)介面。</span><span class="sxs-lookup"><span data-stu-id="c01fa-131">To obtain access to the DirectDraw surface, the filter must call **QueryInterface** on the returned [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object and request the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="c01fa-132">很明顯地，上游篩選器在將範例釋放回可用清單時，必須確保介面未鎖定。</span><span class="sxs-lookup"><span data-stu-id="c01fa-132">Obviously, the upstream filter must ensure that the surface is not locked when it releases the sample back to the free list.</span></span>

 

 



