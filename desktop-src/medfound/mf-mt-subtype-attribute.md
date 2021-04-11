---
description: 媒體類型的子類型 GUID。
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: 'MF_MT_SUBTYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026825"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="6b6e0-103">MF \_ MT \_ 子類型屬性</span><span class="sxs-lookup"><span data-stu-id="6b6e0-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="6b6e0-104">媒體類型的子類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="6b6e0-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b6e0-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6b6e0-105">Data type</span></span>

<span data-ttu-id="6b6e0-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="6b6e0-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="6b6e0-107">備註</span><span class="sxs-lookup"><span data-stu-id="6b6e0-107">Remarks</span></span>

<span data-ttu-id="6b6e0-108">子類型 GUID 會定義主要類型內的特定媒體格式類型。</span><span class="sxs-lookup"><span data-stu-id="6b6e0-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="6b6e0-109">例如，在影片中，子類型包括 RGB-24、RGB-32、UYVY、AYUV 等等。</span><span class="sxs-lookup"><span data-stu-id="6b6e0-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="6b6e0-110">在音訊內，子類型包含 PCM 音訊、Windows Media 音訊9等等。</span><span class="sxs-lookup"><span data-stu-id="6b6e0-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="6b6e0-111">如需可能的值，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="6b6e0-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="6b6e0-112">音訊子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="6b6e0-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="6b6e0-113">影片子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="6b6e0-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="6b6e0-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="6b6e0-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6e0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b6e0-115">Requirements</span></span>



| <span data-ttu-id="6b6e0-116">需求</span><span class="sxs-lookup"><span data-stu-id="6b6e0-116">Requirement</span></span> | <span data-ttu-id="6b6e0-117">值</span><span class="sxs-lookup"><span data-stu-id="6b6e0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6e0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b6e0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6e0-119">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b6e0-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6b6e0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b6e0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6e0-121">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b6e0-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6b6e0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6b6e0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b6e0-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b6e0-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b6e0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b6e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6e0-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6b6e0-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6b6e0-126">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="6b6e0-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="6b6e0-127">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="6b6e0-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="6b6e0-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6b6e0-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6b6e0-129">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="6b6e0-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




