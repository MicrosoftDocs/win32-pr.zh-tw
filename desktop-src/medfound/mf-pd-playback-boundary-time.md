---
description: 會將時間 (以 100-毫微秒) 單位來儲存，表示必須開始的時間，相對於媒體來源的開頭。
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: 'MF_PD_PLAYBACK_BOUNDARY_TIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027468"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="8acde-103">MF \_ PD \_ 播放 \_ 界限 \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="8acde-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="8acde-104">會將時間 (以 100-毫微秒) 單位來儲存，表示必須開始的時間，相對於媒體來源的開頭。</span><span class="sxs-lookup"><span data-stu-id="8acde-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="8acde-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8acde-105">Data type</span></span>

<span data-ttu-id="8acde-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="8acde-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="8acde-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="8acde-107">Get/set</span></span>

<span data-ttu-id="8acde-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="8acde-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="8acde-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="8acde-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8acde-110">適用於</span><span class="sxs-lookup"><span data-stu-id="8acde-110">Applies to</span></span>

[<span data-ttu-id="8acde-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8acde-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="8acde-112">備註</span><span class="sxs-lookup"><span data-stu-id="8acde-112">Remarks</span></span>

<span data-ttu-id="8acde-113">在 \_ \_ 播放清單中，媒體來源的 [MF PD 播放 \_ 界限時間] \_ 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8acde-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="8acde-114">此值表示簡報的實際開始時間。</span><span class="sxs-lookup"><span data-stu-id="8acde-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="8acde-115">假設有一個播放清單包含媒體來源 *Element1*、 *Element2* 和 *Element3* 的順序。</span><span class="sxs-lookup"><span data-stu-id="8acde-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="8acde-116">*Element1* 開始播放後的15秒，就會發生動態資料流變更。</span><span class="sxs-lookup"><span data-stu-id="8acde-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="8acde-117">新的資料流程必須在簡報中開始15秒的時間。</span><span class="sxs-lookup"><span data-stu-id="8acde-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="8acde-118">不過，最接近15秒呈現時間的主要畫面格為新資料流程的12秒。</span><span class="sxs-lookup"><span data-stu-id="8acde-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="8acde-119">若要在15秒內啟動新的簡報，需要 markin，以便將解碼的樣本從12秒降至15秒。</span><span class="sxs-lookup"><span data-stu-id="8acde-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="8acde-120">在轉換之前，媒體來源會引發 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8acde-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="8acde-121">這會傳回包含 *Element1* 的 [MF \_ PD 播放專案 \_ \_ \_ 識別碼](mf-pd-playback-element-id.md)屬性的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="8acde-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="8acde-122">此外，它還包含 [MF \_ PD \_ 播放 \_ 界限時間] \_ 屬性（設定為15秒），以表示發生轉換的時間。</span><span class="sxs-lookup"><span data-stu-id="8acde-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="8acde-123">媒體來源會在解碼後的15秒執行 markin，以防止畫面格顯示12秒到15秒。</span><span class="sxs-lookup"><span data-stu-id="8acde-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="8acde-124">此值只會影響 markin 時間，不會影響媒體會話調整時間戳記的方式。</span><span class="sxs-lookup"><span data-stu-id="8acde-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="8acde-125">除非媒體來源透過 [ [MF \_ PD \_ 播放專案 \_ \_ 識別碼](mf-pd-playback-element-id.md) ] 屬性工作表示此簡報與上一個播放元素相同，否則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8acde-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="8acde-126">[MF \_ PD \_ 播放 \_ 界限 \_ 時間] 屬性類似于 [拓撲] 節點上設定的 [ [mf \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8acde-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="8acde-127">針對在 Windows Vista 上執行的應用程式，執行 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 的媒體來源應該使用 **mf \_ TOPONODE \_ MEDIASTART** ，而不是使用 mf \_ PD \_ 播放 \_ 界限 \_ 時間。</span><span class="sxs-lookup"><span data-stu-id="8acde-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="8acde-128">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="8acde-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acde-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8acde-129">Requirements</span></span>



| <span data-ttu-id="8acde-130">需求</span><span class="sxs-lookup"><span data-stu-id="8acde-130">Requirement</span></span> | <span data-ttu-id="8acde-131">值</span><span class="sxs-lookup"><span data-stu-id="8acde-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8acde-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8acde-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8acde-133">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8acde-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8acde-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8acde-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8acde-135">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8acde-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8acde-136">標頭</span><span class="sxs-lookup"><span data-stu-id="8acde-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8acde-137"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8acde-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8acde-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8acde-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acde-139">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8acde-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8acde-140">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="8acde-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




