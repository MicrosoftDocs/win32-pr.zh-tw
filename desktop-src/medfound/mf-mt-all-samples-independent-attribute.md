---
description: 指定每個範例是否與資料流程中的其他範例無關的媒體類型。
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: 'MF_MT_ALL_SAMPLES_INDEPENDENT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986822"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="7a94b-103">MF \_ MT \_ 所有 \_ 範例 \_ 獨立屬性</span><span class="sxs-lookup"><span data-stu-id="7a94b-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="7a94b-104">指定每個範例是否與資料流程中的其他範例無關的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7a94b-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="7a94b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7a94b-105">Data type</span></span>

<span data-ttu-id="7a94b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7a94b-106">**UINT32**</span></span>

<span data-ttu-id="7a94b-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="7a94b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a94b-108">備註</span><span class="sxs-lookup"><span data-stu-id="7a94b-108">Remarks</span></span>

<span data-ttu-id="7a94b-109">如果這個屬性為 **FALSE**，則無法使用某些範例，而不需要參考資料流中的其他範例。</span><span class="sxs-lookup"><span data-stu-id="7a94b-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="7a94b-110">例如，如果影片格式包含 delta 框架，則此屬性應為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7a94b-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="7a94b-111">這個屬性會對應至 DirectShow [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構中的 **bTemporalCompression** 欄位。</span><span class="sxs-lookup"><span data-stu-id="7a94b-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="7a94b-112">針對所有未壓縮的媒體類型，將這個屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7a94b-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="7a94b-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7a94b-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a94b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a94b-114">Requirements</span></span>



| <span data-ttu-id="7a94b-115">需求</span><span class="sxs-lookup"><span data-stu-id="7a94b-115">Requirement</span></span> | <span data-ttu-id="7a94b-116">值</span><span class="sxs-lookup"><span data-stu-id="7a94b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a94b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a94b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7a94b-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a94b-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7a94b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a94b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7a94b-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a94b-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7a94b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7a94b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a94b-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a94b-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a94b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a94b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a94b-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7a94b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7a94b-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7a94b-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7a94b-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7a94b-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7a94b-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7a94b-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7a94b-128">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="7a94b-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
