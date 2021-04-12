---
description: 指定如何配置媒體範例的 Microsoft Direct3D 11 表面。
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: 'MF_SA_D3D11_USAGE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191629"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="31dda-103">MF \_ SA \_ D3D11 \_ 使用方式屬性</span><span class="sxs-lookup"><span data-stu-id="31dda-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="31dda-104">指定如何配置媒體範例的 Microsoft Direct3D 11 表面。</span><span class="sxs-lookup"><span data-stu-id="31dda-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="31dda-105">使用方式會直接反映範例是否可透過 CPU 或 GPU 來存取。</span><span class="sxs-lookup"><span data-stu-id="31dda-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="31dda-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="31dda-106">Data type</span></span>

<span data-ttu-id="31dda-107">**D3D11 \_使用** 方式儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="31dda-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="31dda-108">備註</span><span class="sxs-lookup"><span data-stu-id="31dda-108">Remarks</span></span>

<span data-ttu-id="31dda-109">這個屬性的值是 [**D3D11 \_ 使用**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) 值。</span><span class="sxs-lookup"><span data-stu-id="31dda-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="31dda-110">Microsoft 媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="31dda-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="31dda-111">在此內容中，只有當 Microsoft 媒體基礎轉換 (MFT) 針對 [MF \_ SA \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)屬性傳回 **TRUE** 時，才適用此屬性。</span><span class="sxs-lookup"><span data-stu-id="31dda-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="31dda-112">如果 MFT 支援 Direct3D 11，則在配置 Microsoft Direct3D 的輸出介面時，這個屬性會提供對 MFT 的提示。</span><span class="sxs-lookup"><span data-stu-id="31dda-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="31dda-113">設定屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="31dda-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="31dda-114">呼叫 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) 以取得 MFT 屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="31dda-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="31dda-115">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="31dda-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="31dda-116">在串流處理開始之前，媒體基礎管線會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="31dda-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="31dda-117">在配置介面時，MFT 應嘗試接受設定。</span><span class="sxs-lookup"><span data-stu-id="31dda-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="31dda-118">如果無法這麼做，則 MFT 可以忽略屬性，而不是失敗的配置。</span><span class="sxs-lookup"><span data-stu-id="31dda-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="31dda-119">此外，如果 MFT 需要 Direct3D 介面以進行輸入，則可以將此屬性公開為輸入介面如何配置的提示。</span><span class="sxs-lookup"><span data-stu-id="31dda-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="31dda-120">查詢屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="31dda-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="31dda-121">呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 來取得輸入資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="31dda-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="31dda-122">呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="31dda-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="31dda-123">範例配置器</span><span class="sxs-lookup"><span data-stu-id="31dda-123">Sample Allocator</span></span>

<span data-ttu-id="31dda-124">您可以在影片範例配置器的 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) 方法中設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="31dda-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31dda-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="31dda-125">Requirements</span></span>



| <span data-ttu-id="31dda-126">需求</span><span class="sxs-lookup"><span data-stu-id="31dda-126">Requirement</span></span> | <span data-ttu-id="31dda-127">值</span><span class="sxs-lookup"><span data-stu-id="31dda-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dda-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31dda-128">Minimum supported client</span></span><br/> | <span data-ttu-id="31dda-129">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31dda-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="31dda-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31dda-130">Minimum supported server</span></span><br/> | <span data-ttu-id="31dda-131">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31dda-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="31dda-132">標頭</span><span class="sxs-lookup"><span data-stu-id="31dda-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="31dda-133"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="31dda-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31dda-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31dda-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31dda-135">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="31dda-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
