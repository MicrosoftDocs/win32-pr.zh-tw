---
description: 使用 DirectX Video 加速 (DXVA) 1.0 版，啟用從 Direct3D 9 裝置進行硬體加速解碼。
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: 'IDirect3DVideoDevice9 介面 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114224"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="f33c5-103">IDirect3DVideoDevice9 介面</span><span class="sxs-lookup"><span data-stu-id="f33c5-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="f33c5-104">使用 DirectX Video 加速 (DXVA) 1.0 版，啟用從 Direct3D 9 裝置進行硬體加速解碼。</span><span class="sxs-lookup"><span data-stu-id="f33c5-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f33c5-105">使用時機</span><span class="sxs-lookup"><span data-stu-id="f33c5-105">When to use</span></span>

<span data-ttu-id="f33c5-106">此介面不適用於一般應用程式用途。</span><span class="sxs-lookup"><span data-stu-id="f33c5-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="f33c5-107">DirectShow 解碼篩選器應該使用 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 介面，而不是 **IDirect3DVideoDevice9**。</span><span class="sxs-lookup"><span data-stu-id="f33c5-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="f33c5-108">影片混合轉譯器的輸入釘 (VMR) 濾波器和覆迭混音器篩選器會公開 **IAMVideoAccelerator**。</span><span class="sxs-lookup"><span data-stu-id="f33c5-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="f33c5-109">成員</span><span class="sxs-lookup"><span data-stu-id="f33c5-109">Members</span></span>

<span data-ttu-id="f33c5-110">**IDirect3DVideoDevice9** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f33c5-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f33c5-111">**IDirect3DVideoDevice9** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f33c5-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="f33c5-112">方法</span><span class="sxs-lookup"><span data-stu-id="f33c5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f33c5-113">方法</span><span class="sxs-lookup"><span data-stu-id="f33c5-113">Methods</span></span>

<span data-ttu-id="f33c5-114">**IDirect3DVideoDevice9** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f33c5-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="f33c5-115">方法</span><span class="sxs-lookup"><span data-stu-id="f33c5-115">Method</span></span>                                                                                   | <span data-ttu-id="f33c5-116">描述</span><span class="sxs-lookup"><span data-stu-id="f33c5-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f33c5-117">**CreateDXVADevice**</span><span class="sxs-lookup"><span data-stu-id="f33c5-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="f33c5-118">建立 DXVA 解碼器裝置。</span><span class="sxs-lookup"><span data-stu-id="f33c5-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f33c5-119">**CreateSurface**</span><span class="sxs-lookup"><span data-stu-id="f33c5-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="f33c5-120">建立 DXVA 解碼的壓縮表面。</span><span class="sxs-lookup"><span data-stu-id="f33c5-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="f33c5-121">**GetDXVACompressedBufferInfo**</span><span class="sxs-lookup"><span data-stu-id="f33c5-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="f33c5-122">取得硬體加速解碼所需之壓縮緩衝區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f33c5-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="f33c5-123">**GetDXVAGuids**</span><span class="sxs-lookup"><span data-stu-id="f33c5-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="f33c5-124">取得顯示驅動程式支援的 DXVA 配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="f33c5-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="f33c5-125">**GetDXVAInternalInfo**</span><span class="sxs-lookup"><span data-stu-id="f33c5-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="f33c5-126">查詢硬體抽象層 (HAL) 將配置給其私用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="f33c5-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="f33c5-127">**GetUncompressedDXVAFormats**</span><span class="sxs-lookup"><span data-stu-id="f33c5-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="f33c5-128">取得未壓縮像素格式的清單，這些格式可使用指定的 DXVA 設定檔來呈現。</span><span class="sxs-lookup"><span data-stu-id="f33c5-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="f33c5-129">備註</span><span class="sxs-lookup"><span data-stu-id="f33c5-129">Remarks</span></span>

<span data-ttu-id="f33c5-130">若要取得這個介面的指標，請在 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)或 [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex)指標上呼叫 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="f33c5-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="f33c5-131">這個介面僅支援 DXVA 1.0。</span><span class="sxs-lookup"><span data-stu-id="f33c5-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="f33c5-132">它不支援 DXVA 2.0。</span><span class="sxs-lookup"><span data-stu-id="f33c5-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33c5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="f33c5-133">Requirements</span></span>



| <span data-ttu-id="f33c5-134">需求</span><span class="sxs-lookup"><span data-stu-id="f33c5-134">Requirement</span></span> | <span data-ttu-id="f33c5-135">值</span><span class="sxs-lookup"><span data-stu-id="f33c5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f33c5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f33c5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f33c5-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f33c5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f33c5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f33c5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f33c5-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f33c5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f33c5-140">標頭</span><span class="sxs-lookup"><span data-stu-id="f33c5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f33c5-141"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="f33c5-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33c5-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f33c5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33c5-143">Direct3D Video 介面</span><span class="sxs-lookup"><span data-stu-id="f33c5-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f33c5-144">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="f33c5-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="f33c5-145">DXVA 1.0 規格</span><span class="sxs-lookup"><span data-stu-id="f33c5-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
