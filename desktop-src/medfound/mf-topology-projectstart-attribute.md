---
description: 指定拓撲的停止時間（相對於序列中第一個拓撲的開頭）。
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: 'MF_TOPOLOGY_PROJECTSTART 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848522"
---
# <a name="mf_topology_projectstart-attribute"></a><span data-ttu-id="5f03d-103">MF \_ 拓撲 \_ PROJECTSTART 屬性</span><span class="sxs-lookup"><span data-stu-id="5f03d-103">MF\_TOPOLOGY\_PROJECTSTART attribute</span></span>

<span data-ttu-id="5f03d-104">指定拓撲的停止時間（相對於序列中第一個拓撲的開頭）。</span><span class="sxs-lookup"><span data-stu-id="5f03d-104">Specifies the stop time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f03d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5f03d-105">Data type</span></span>

<span data-ttu-id="5f03d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5f03d-106">**UINT64**</span></span>

<span data-ttu-id="5f03d-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="5f03d-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f03d-108">備註</span><span class="sxs-lookup"><span data-stu-id="5f03d-108">Remarks</span></span>

<span data-ttu-id="5f03d-109">此值是以100毫微秒的單位來提供。</span><span class="sxs-lookup"><span data-stu-id="5f03d-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="5f03d-110">如果媒體會話是使用等於 **TRUE** 的 [**mf \_ 會話 \_ GLOBAL \_ TIME**](mf-session-global-time-attribute.md)屬性所建立，則所有拓撲都必須包含 **MF \_ 拓撲 \_ PROJECTSTART** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5f03d-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="5f03d-111">否則，拓撲不得包含 **MF \_ 拓撲 \_ PROJECTSTART** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5f03d-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="5f03d-112">如需詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。</span><span class="sxs-lookup"><span data-stu-id="5f03d-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="5f03d-113">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="5f03d-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="5f03d-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5f03d-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f03d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f03d-115">Requirements</span></span>



| <span data-ttu-id="5f03d-116">需求</span><span class="sxs-lookup"><span data-stu-id="5f03d-116">Requirement</span></span> | <span data-ttu-id="5f03d-117">值</span><span class="sxs-lookup"><span data-stu-id="5f03d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f03d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f03d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f03d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f03d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5f03d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f03d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f03d-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f03d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5f03d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5f03d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f03d-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f03d-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f03d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f03d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f03d-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5f03d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f03d-126">順序呈現時間</span><span class="sxs-lookup"><span data-stu-id="5f03d-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="5f03d-127">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="5f03d-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f03d-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5f03d-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="5f03d-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5f03d-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="5f03d-130">**MF \_ 拓撲 \_ PROJECTSTOP**</span><span class="sxs-lookup"><span data-stu-id="5f03d-130">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




