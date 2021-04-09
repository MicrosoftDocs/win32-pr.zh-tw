---
description: 包含適用于來源讀取器的 Microsoft Direct3D 裝置管理員的指標。
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: 'MF_SOURCE_READER_D3D_MANAGER 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849521"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="ee3b2-103">MF \_ 來源 \_ 讀取器 \_ D3D \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="ee3b2-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="ee3b2-104">包含適用于[來源讀取器](source-reader.md)的 Microsoft [Direct3D 裝置管理員](direct3d-device-manager.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="ee3b2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ee3b2-105">Data type</span></span>

<span data-ttu-id="ee3b2-106">**IDirect3DDeviceManager9 \* 或 IMFDXGIDeviceManager \*** 儲存為 \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="ee3b2-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="ee3b2-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="ee3b2-107">Get/set</span></span>

<span data-ttu-id="ee3b2-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="ee3b2-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee3b2-110">備註</span><span class="sxs-lookup"><span data-stu-id="ee3b2-110">Remarks</span></span>

<span data-ttu-id="ee3b2-111">這個屬性的值可以是 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標或 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="ee3b2-112">使用此屬性可為來源讀取器所載入的任何影片解碼器提供 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="ee3b2-113">如果您設定此屬性，且解碼器支援 Microsoft DirectX Video 加速 (DXVA) ，則來源讀取器會使用 Direct3D 裝置來配置影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="ee3b2-114">這些緩衝區與 DXVA 2 video 處理器相容。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="ee3b2-115"> (參閱 [DXVA Video 處理](dxva-video-processing.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="ee3b2-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="ee3b2-116">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="ee3b2-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="ee3b2-117">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="ee3b2-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="ee3b2-118">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="ee3b2-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="ee3b2-119">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="ee3b2-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="ee3b2-120">如果您要使用來源讀取器來取得已解碼的影片畫面，並使用 Direct3D 來顯示畫面格，通常會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="ee3b2-121">設定此屬性可讓解碼器使用 DXVA。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="ee3b2-122">如果有下列情況，您就不會設定這個屬性：</span><span class="sxs-lookup"><span data-stu-id="ee3b2-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="ee3b2-123">您使用來源讀取器來處理音訊，而非影片。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="ee3b2-124">您正在從來源讀取程式取得壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="ee3b2-125">在此情況下，來源讀取器不會建立解碼器。</span><span class="sxs-lookup"><span data-stu-id="ee3b2-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3b2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee3b2-126">Requirements</span></span>



| <span data-ttu-id="ee3b2-127">需求</span><span class="sxs-lookup"><span data-stu-id="ee3b2-127">Requirement</span></span> | <span data-ttu-id="ee3b2-128">值</span><span class="sxs-lookup"><span data-stu-id="ee3b2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3b2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee3b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3b2-130">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee3b2-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ee3b2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee3b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3b2-132">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee3b2-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ee3b2-133">標頭</span><span class="sxs-lookup"><span data-stu-id="ee3b2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee3b2-134"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee3b2-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee3b2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee3b2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3b2-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ee3b2-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee3b2-137">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="ee3b2-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="ee3b2-138">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="ee3b2-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




