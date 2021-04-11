---
description: 包含媒體類型的 DirectShow 格式 GUID。
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: 'MF_MT_AM_FORMAT_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318804"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="28c11-103">MF \_ MT \_ \_ 格式 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="28c11-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="28c11-104">包含媒體類型的 DirectShow 格式 GUID。</span><span class="sxs-lookup"><span data-stu-id="28c11-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="28c11-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="28c11-105">Data type</span></span>

<span data-ttu-id="28c11-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="28c11-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="28c11-107">備註</span><span class="sxs-lookup"><span data-stu-id="28c11-107">Remarks</span></span>

<span data-ttu-id="28c11-108">當 DirectShow 媒體類型轉換成媒體基礎媒體類型時，可能會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="28c11-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="28c11-109">屬性工作表示原始的 DirectShow 格式類型。</span><span class="sxs-lookup"><span data-stu-id="28c11-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="28c11-110">值會對應至 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的 formattype 成員。</span><span class="sxs-lookup"><span data-stu-id="28c11-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="28c11-111">若是音訊格式，如果無法辨識 DirectShow 格式類型，則 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性可能會包含原始的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="28c11-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="28c11-112">除非您要轉換 DirectShow 格式結構，否則請勿在媒體類型上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="28c11-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="28c11-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="28c11-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c11-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="28c11-114">Requirements</span></span>



| <span data-ttu-id="28c11-115">需求</span><span class="sxs-lookup"><span data-stu-id="28c11-115">Requirement</span></span> | <span data-ttu-id="28c11-116">值</span><span class="sxs-lookup"><span data-stu-id="28c11-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28c11-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28c11-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28c11-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28c11-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28c11-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28c11-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28c11-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28c11-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28c11-121">標頭</span><span class="sxs-lookup"><span data-stu-id="28c11-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c11-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="28c11-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c11-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28c11-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c11-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="28c11-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28c11-125">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="28c11-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="28c11-126">媒體類型轉換</span><span class="sxs-lookup"><span data-stu-id="28c11-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="28c11-127">媒體類型</span><span class="sxs-lookup"><span data-stu-id="28c11-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="28c11-128">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="28c11-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="28c11-129">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="28c11-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="28c11-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="28c11-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="28c11-131">**MFCreateMediaTypeFromRepresentation**</span><span class="sxs-lookup"><span data-stu-id="28c11-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
