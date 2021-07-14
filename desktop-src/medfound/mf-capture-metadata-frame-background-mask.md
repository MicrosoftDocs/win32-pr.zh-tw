---
description: 報告背景分割遮罩的中繼資料和遮罩緩衝區，以區分影片框架的背景和前景。
title: 'MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK 屬性 (Mfapi) '
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691841"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="a8460-103">MF \_ CAPTURE \_ 中繼資料 \_ 框架 \_ 背景 \_ 遮罩屬性</span><span class="sxs-lookup"><span data-stu-id="a8460-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="a8460-104">報告背景分割遮罩的中繼資料和遮罩緩衝區，以區分影片框架的背景和前景。</span><span class="sxs-lookup"><span data-stu-id="a8460-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8460-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a8460-105">Data type</span></span>

<span data-ttu-id="a8460-106">**Blob**</span><span class="sxs-lookup"><span data-stu-id="a8460-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="a8460-107">備註</span><span class="sxs-lookup"><span data-stu-id="a8460-107">Remarks</span></span>

<span data-ttu-id="a8460-108">這個屬性所傳送的資料是 [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) 結構，其中包含背景遮罩的維度及其推斷來源框架的涵蓋範圍的相關資訊，也就是資料流程輸出的框架。</span><span class="sxs-lookup"><span data-stu-id="a8460-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="a8460-109">它也會攜帶一個連續的緩衝區，代表取用應用程式所要使用的遮罩，以定義哪些圖元被視為前景或背景的一部分。</span><span class="sxs-lookup"><span data-stu-id="a8460-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="a8460-110">與框架相關之遮罩的縮放和影像座標相互關聯是由取用應用程式所處理。</span><span class="sxs-lookup"><span data-stu-id="a8460-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="a8460-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8460-111">Requirements</span></span>



| <span data-ttu-id="a8460-112">需求</span><span class="sxs-lookup"><span data-stu-id="a8460-112">Requirement</span></span> | <span data-ttu-id="a8460-113">值</span><span class="sxs-lookup"><span data-stu-id="a8460-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8460-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8460-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a8460-115">Windows組建22000t</span><span class="sxs-lookup"><span data-stu-id="a8460-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="a8460-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8460-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a8460-117">Windows組建22000</span><span class="sxs-lookup"><span data-stu-id="a8460-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="a8460-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a8460-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8460-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8460-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8460-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8460-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8460-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a8460-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8460-122">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a8460-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a8460-123">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a8460-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a8460-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a8460-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a8460-125">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="a8460-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




