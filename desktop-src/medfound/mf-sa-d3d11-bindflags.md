---
description: 指定配置媒體範例的 Microsoft Direct3D 11 介面時所要使用的系結旗標。
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: 'MF_SA_D3D11_BINDFLAGS 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319311"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="25da9-103">MF \_ SA \_ D3D11 \_ BINDFLAGS 屬性</span><span class="sxs-lookup"><span data-stu-id="25da9-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="25da9-104">指定配置媒體範例的 Microsoft Direct3D 11 介面時所要使用的系結旗標。</span><span class="sxs-lookup"><span data-stu-id="25da9-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="25da9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="25da9-105">Data type</span></span>

<span data-ttu-id="25da9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="25da9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="25da9-107">備註</span><span class="sxs-lookup"><span data-stu-id="25da9-107">Remarks</span></span>

<span data-ttu-id="25da9-108">這個屬性的值是 D3D11 系結 [**\_ \_ 旗**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag)標旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="25da9-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="25da9-109">Microsoft 媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="25da9-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="25da9-110">在此內容中，只有當 Microsoft 媒體基礎轉換 (MFT) 針對 [MF \_ SA \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)屬性傳回 **TRUE** 時，才適用此屬性。</span><span class="sxs-lookup"><span data-stu-id="25da9-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="25da9-111">如果 MFT 支援 Direct3D 11，則在配置 Microsoft Direct3D 的輸出介面時，這個屬性會提供對 MFT 的提示。</span><span class="sxs-lookup"><span data-stu-id="25da9-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="25da9-112">設定屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="25da9-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="25da9-113">呼叫 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) 以取得 MFT 屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="25da9-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="25da9-114">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="25da9-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="25da9-115">在串流處理開始之前，媒體基礎管線會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="25da9-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="25da9-116">在配置介面時，MFT 應嘗試接受設定。</span><span class="sxs-lookup"><span data-stu-id="25da9-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="25da9-117">如果無法這麼做，則 MFT 可以忽略屬性，而不是失敗的配置。</span><span class="sxs-lookup"><span data-stu-id="25da9-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="25da9-118">此外，如果 MFT 需要 Direct3D 介面以進行輸入，則可以將此屬性公開為輸入介面如何配置的提示。</span><span class="sxs-lookup"><span data-stu-id="25da9-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="25da9-119">查詢屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="25da9-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="25da9-120">呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 來取得輸入資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="25da9-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="25da9-121">呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="25da9-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="25da9-122">範例配置器</span><span class="sxs-lookup"><span data-stu-id="25da9-122">Sample Allocator</span></span>

<span data-ttu-id="25da9-123">您可以在影片範例配置器的 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) 方法中設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="25da9-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25da9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="25da9-124">Requirements</span></span>



| <span data-ttu-id="25da9-125">需求</span><span class="sxs-lookup"><span data-stu-id="25da9-125">Requirement</span></span> | <span data-ttu-id="25da9-126">值</span><span class="sxs-lookup"><span data-stu-id="25da9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25da9-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25da9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="25da9-128">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25da9-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="25da9-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25da9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="25da9-130">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25da9-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="25da9-131">標頭</span><span class="sxs-lookup"><span data-stu-id="25da9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="25da9-132"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="25da9-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25da9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25da9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25da9-134">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="25da9-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
