---
description: 包含簡報中播放清單元素的識別碼。
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: 'MF_PD_PLAYBACK_ELEMENT_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996975"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="5329d-103">MF \_ PD \_ 播放 \_ 元素 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="5329d-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="5329d-104">包含簡報中播放清單元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5329d-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="5329d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5329d-105">Data type</span></span>

<span data-ttu-id="5329d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5329d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5329d-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="5329d-107">Get/set</span></span>

<span data-ttu-id="5329d-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="5329d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5329d-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="5329d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5329d-110">適用於</span><span class="sxs-lookup"><span data-stu-id="5329d-110">Applies to</span></span>

[<span data-ttu-id="5329d-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5329d-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="5329d-112">備註</span><span class="sxs-lookup"><span data-stu-id="5329d-112">Remarks</span></span>

<span data-ttu-id="5329d-113">傳遞播放清單的媒體來源可以選擇性地在其展示描述項上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="5329d-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="5329d-114">當媒體來源傳遞播放清單時，它會在第一個播放清單元素之後傳送 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="5329d-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="5329d-115">此事件包含新播放清單元素的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="5329d-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="5329d-116">媒體來源可以將識別碼指派給元素，方法是 \_ \_ \_ \_ 在每個呈現描述項上設定 [MF PD 播放專案識別碼] 屬性，包括 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)所建立的描述項。</span><span class="sxs-lookup"><span data-stu-id="5329d-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="5329d-117">媒體來源可能也會傳送 [MENewPresentation](menewpresentation.md) 事件，因為動態資料流參數或資料流程數目有所變更。</span><span class="sxs-lookup"><span data-stu-id="5329d-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="5329d-118">在這種情況下， \_ 兩個簡報中的 MF PD \_ 播放專案識別碼值 \_ \_ 應該保持不變，表示兩個簡報都代表相同的播放清單元素。</span><span class="sxs-lookup"><span data-stu-id="5329d-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="5329d-119">如果兩個連續的簡報都有相同的屬性值，Microsoft 媒體基礎管線會預期時間戳記會在整個轉換期間保持連續。</span><span class="sxs-lookup"><span data-stu-id="5329d-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="5329d-120">因此，當媒體來源轉換至下一個簡報時，不能使用 [MF \_ 事件 \_ 來源 \_ 實際 \_ 開始](mf-event-source-actual-start-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5329d-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="5329d-121">執行 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 的媒體來源應該使用 [mf \_ TOPONODE \_ SEQUENCE \_ ELEMENTID](mf-toponode-sequence-elementid-attribute.md) 屬性，而不是使用 mf \_ PD \_ 播放 \_ 元素 \_ 識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="5329d-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="5329d-122">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5329d-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5329d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5329d-123">Requirements</span></span>



| <span data-ttu-id="5329d-124">需求</span><span class="sxs-lookup"><span data-stu-id="5329d-124">Requirement</span></span> | <span data-ttu-id="5329d-125">值</span><span class="sxs-lookup"><span data-stu-id="5329d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5329d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5329d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5329d-127">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5329d-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5329d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5329d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5329d-129">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5329d-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5329d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5329d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5329d-131"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5329d-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5329d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5329d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5329d-133">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5329d-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5329d-134">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="5329d-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




