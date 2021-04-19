---
description: 指定簡報的開始時間。
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: 'MF_TOPONODE_MEDIASTART 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981743"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="d2ab2-103">MF \_ TOPONODE \_ MEDIASTART 屬性</span><span class="sxs-lookup"><span data-stu-id="d2ab2-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="d2ab2-104">指定簡報的開始時間。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2ab2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d2ab2-105">Data type</span></span>

<span data-ttu-id="d2ab2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d2ab2-106">**UINT64**</span></span>

<span data-ttu-id="d2ab2-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="d2ab2-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="d2ab2-108">Get/set</span></span>

<span data-ttu-id="d2ab2-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="d2ab2-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2ab2-111">適用於</span><span class="sxs-lookup"><span data-stu-id="d2ab2-111">Applies to</span></span>

[<span data-ttu-id="d2ab2-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d2ab2-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="d2ab2-113">備註</span><span class="sxs-lookup"><span data-stu-id="d2ab2-113">Remarks</span></span>

<span data-ttu-id="d2ab2-114">這個屬性會指定來源中播放開始播放的位置，相對於啟動來源，則以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="d2ab2-115">如果未設定此屬性，播放會從零開始 () 檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="d2ab2-116">例如，若要在5秒的標記開始播放，請將此屬性設定為50000000。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="d2ab2-117">在拓撲 (節點（類型等於 **MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) ）的來源節點上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="d2ab2-118">呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="d2ab2-119">如果您以手動方式將解碼器插入拓撲，您也必須在 [解碼器] 節點上，將 [ [mf \_ TOPONODE \_ MARKIN \_ ](mf-toponode-markin-here-attribute.md) ] 和 [ [mf \_ TOPONODE \_ MARKOUT \_ ](mf-toponode-markout-here-attribute.md) ] 屬性設定為。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="d2ab2-120">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="d2ab2-121">不過，負值並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="d2ab2-122">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="d2ab2-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ab2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2ab2-123">Requirements</span></span>



| <span data-ttu-id="d2ab2-124">需求</span><span class="sxs-lookup"><span data-stu-id="d2ab2-124">Requirement</span></span> | <span data-ttu-id="d2ab2-125">值</span><span class="sxs-lookup"><span data-stu-id="d2ab2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ab2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2ab2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ab2-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2ab2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d2ab2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2ab2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ab2-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2ab2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d2ab2-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d2ab2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2ab2-131"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ab2-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ab2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2ab2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ab2-133">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d2ab2-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2ab2-134">順序呈現時間</span><span class="sxs-lookup"><span data-stu-id="d2ab2-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="d2ab2-135">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="d2ab2-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2ab2-136">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="d2ab2-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




