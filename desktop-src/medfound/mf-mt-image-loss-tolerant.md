---
description: 指定 ASF 影像資料流程是否為 degradable JPEG 類型。
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: 'MF_MT_IMAGE_LOSS_TOLERANT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848105"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="883fd-103">MF \_ MT \_ 影像 \_ 遺失 \_ 容錯屬性</span><span class="sxs-lookup"><span data-stu-id="883fd-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="883fd-104">指定 ASF 影像資料流程是否為 degradable JPEG 類型。</span><span class="sxs-lookup"><span data-stu-id="883fd-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="883fd-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="883fd-105">Data type</span></span>

<span data-ttu-id="883fd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="883fd-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="883fd-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="883fd-107">Get/set</span></span>

<span data-ttu-id="883fd-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="883fd-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="883fd-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="883fd-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="883fd-110">適用於</span><span class="sxs-lookup"><span data-stu-id="883fd-110">Applies to</span></span>

[<span data-ttu-id="883fd-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="883fd-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="883fd-112">備註</span><span class="sxs-lookup"><span data-stu-id="883fd-112">Remarks</span></span>

<span data-ttu-id="883fd-113">此屬性適用于 ASF 中影像資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="883fd-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="883fd-114">如果值為 **TRUE**，則資料流程是 degradable JPEG 影像類型。</span><span class="sxs-lookup"><span data-stu-id="883fd-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="883fd-115">否則，資料流程是 JFIF 影像類型。</span><span class="sxs-lookup"><span data-stu-id="883fd-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="883fd-116">如需這些資料流程類型的詳細資訊，請參閱 ASF 規格。</span><span class="sxs-lookup"><span data-stu-id="883fd-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="883fd-117">除了 MF \_ MT \_ 影像 \_ 遺失 \_ 容錯屬性之外，ASF 映射資料流程的媒體類型還包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="883fd-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="883fd-118">屬性</span><span class="sxs-lookup"><span data-stu-id="883fd-118">Attribute</span></span>                                                 | <span data-ttu-id="883fd-119">描述</span><span class="sxs-lookup"><span data-stu-id="883fd-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="883fd-120">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="883fd-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="883fd-121">包含值 **MFMediaType \_ 影像**。</span><span class="sxs-lookup"><span data-stu-id="883fd-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="883fd-122">**MF \_ MT \_ 框架 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="883fd-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="883fd-123">提供影像大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="883fd-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="883fd-124">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="883fd-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="883fd-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="883fd-125">Requirements</span></span>



| <span data-ttu-id="883fd-126">需求</span><span class="sxs-lookup"><span data-stu-id="883fd-126">Requirement</span></span> | <span data-ttu-id="883fd-127">值</span><span class="sxs-lookup"><span data-stu-id="883fd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="883fd-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="883fd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="883fd-129">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="883fd-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="883fd-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="883fd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="883fd-131">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="883fd-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="883fd-132">標頭</span><span class="sxs-lookup"><span data-stu-id="883fd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="883fd-133"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="883fd-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883fd-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="883fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883fd-135">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="883fd-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="883fd-136">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="883fd-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




