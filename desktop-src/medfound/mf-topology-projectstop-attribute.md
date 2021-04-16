---
description: 指定拓撲的開始時間（相對於序列中第一個拓撲的開頭）。
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: 'MF_TOPOLOGY_PROJECTSTOP 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512816"
---
# <a name="mf_topology_projectstop-attribute"></a><span data-ttu-id="43f22-103">MF \_ 拓撲 \_ PROJECTSTOP 屬性</span><span class="sxs-lookup"><span data-stu-id="43f22-103">MF\_TOPOLOGY\_PROJECTSTOP attribute</span></span>

<span data-ttu-id="43f22-104">指定拓撲的開始時間（相對於序列中第一個拓撲的開頭）。</span><span class="sxs-lookup"><span data-stu-id="43f22-104">Specifies the start time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="43f22-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="43f22-105">Data type</span></span>

<span data-ttu-id="43f22-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="43f22-106">**UINT64**</span></span>

<span data-ttu-id="43f22-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="43f22-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f22-108">備註</span><span class="sxs-lookup"><span data-stu-id="43f22-108">Remarks</span></span>

<span data-ttu-id="43f22-109">此值是以100毫微秒的單位來提供。</span><span class="sxs-lookup"><span data-stu-id="43f22-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="43f22-110">如果媒體會話是使用等於 **TRUE** 的 [**mf \_ 會話 \_ GLOBAL \_ TIME**](mf-session-global-time-attribute.md)屬性所建立，則所有拓撲都必須包含 **MF \_ 拓撲 \_ PROJECTSTOP** 屬性。</span><span class="sxs-lookup"><span data-stu-id="43f22-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="43f22-111">否則，拓撲不得包含 **MF \_ 拓撲 \_ PROJECTSTOP** 屬性。</span><span class="sxs-lookup"><span data-stu-id="43f22-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="43f22-112">如需詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。</span><span class="sxs-lookup"><span data-stu-id="43f22-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="43f22-113">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="43f22-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="43f22-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="43f22-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f22-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="43f22-115">Requirements</span></span>



| <span data-ttu-id="43f22-116">需求</span><span class="sxs-lookup"><span data-stu-id="43f22-116">Requirement</span></span> | <span data-ttu-id="43f22-117">值</span><span class="sxs-lookup"><span data-stu-id="43f22-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43f22-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43f22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43f22-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43f22-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43f22-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43f22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43f22-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43f22-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43f22-122">標頭</span><span class="sxs-lookup"><span data-stu-id="43f22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f22-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="43f22-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f22-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43f22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f22-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="43f22-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="43f22-126">順序呈現時間</span><span class="sxs-lookup"><span data-stu-id="43f22-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="43f22-127">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="43f22-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="43f22-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="43f22-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="43f22-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="43f22-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="43f22-130">**MF \_ 拓撲 \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="43f22-130">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




