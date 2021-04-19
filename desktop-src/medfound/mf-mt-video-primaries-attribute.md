---
description: 指定影片媒體類型的色彩主要複本。
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: 'MF_MT_VIDEO_PRIMARIES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981039"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="73d2a-103">MF \_ MT \_ 影片 \_ 主要複本屬性</span><span class="sxs-lookup"><span data-stu-id="73d2a-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="73d2a-104">指定影片媒體類型的色彩主要複本。</span><span class="sxs-lookup"><span data-stu-id="73d2a-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="73d2a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="73d2a-105">Data type</span></span>

<span data-ttu-id="73d2a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73d2a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="73d2a-107">備註</span><span class="sxs-lookup"><span data-stu-id="73d2a-107">Remarks</span></span>

<span data-ttu-id="73d2a-108">這個屬性的值是 [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="73d2a-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="73d2a-109">[**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries)列舉會識別與特定常見影片標準相關聯的色彩主要複本。</span><span class="sxs-lookup"><span data-stu-id="73d2a-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="73d2a-110">如果媒體類型使用 **MFVideoPrimaries** 列舉中未識別的色彩主要複本，請設定 [ [**MF \_ MT \_ 自訂 \_ 影片 \_ 主要複本**](mf-mt-custom-video-primaries-attribute.md) ] 屬性，而不要設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="73d2a-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="73d2a-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="73d2a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d2a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="73d2a-112">Requirements</span></span>



| <span data-ttu-id="73d2a-113">需求</span><span class="sxs-lookup"><span data-stu-id="73d2a-113">Requirement</span></span> | <span data-ttu-id="73d2a-114">值</span><span class="sxs-lookup"><span data-stu-id="73d2a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73d2a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73d2a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="73d2a-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73d2a-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="73d2a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73d2a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="73d2a-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73d2a-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="73d2a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="73d2a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="73d2a-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="73d2a-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d2a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73d2a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d2a-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="73d2a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73d2a-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73d2a-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="73d2a-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73d2a-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="73d2a-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="73d2a-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="73d2a-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="73d2a-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="73d2a-127">擴充的色彩資訊</span><span class="sxs-lookup"><span data-stu-id="73d2a-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




