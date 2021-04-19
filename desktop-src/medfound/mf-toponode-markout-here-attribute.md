---
description: 指定管線是否在此節點套用標記。 標記為展示結束的點。 如果管線元件在標記輸出點之後產生資料，則不會呈現資料。
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: 'MF_TOPONODE_MARKOUT_HERE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971053"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="d87ea-105">MF \_ TOPONODE \_ MARKOUT \_ 這裡屬性</span><span class="sxs-lookup"><span data-stu-id="d87ea-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="d87ea-106">指定管線是否在此節點套用標記。</span><span class="sxs-lookup"><span data-stu-id="d87ea-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="d87ea-107">標記為展示結束的點。</span><span class="sxs-lookup"><span data-stu-id="d87ea-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="d87ea-108">如果管線元件在標記輸出點之後產生資料，則不會呈現資料。</span><span class="sxs-lookup"><span data-stu-id="d87ea-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="d87ea-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="d87ea-109">Data type</span></span>

<span data-ttu-id="d87ea-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d87ea-110">**UINT32**</span></span>

<span data-ttu-id="d87ea-111">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="d87ea-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d87ea-112">備註</span><span class="sxs-lookup"><span data-stu-id="d87ea-112">Remarks</span></span>

<span data-ttu-id="d87ea-113">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="d87ea-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="d87ea-114">如果這個屬性為 **TRUE**，媒體基礎管線會修剪這個節點的輸出範例，以符合簡報的停止時間。</span><span class="sxs-lookup"><span data-stu-id="d87ea-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="d87ea-115">拓撲載入器會在解析拓撲時設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d87ea-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="d87ea-116">大部分的應用程式都不需要設定或抓取此屬性。</span><span class="sxs-lookup"><span data-stu-id="d87ea-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="d87ea-117">建議將此屬性設定為 **TRUE** 時，拓撲的每個分支中必須只有一個節點。</span><span class="sxs-lookup"><span data-stu-id="d87ea-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="d87ea-118">拓撲分支會定義為從來源節點到輸出節點的路徑。</span><span class="sxs-lookup"><span data-stu-id="d87ea-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="d87ea-119">在分支中，您 \_ \_ \_ 必須在分支中的相同節點上設定 [TOPONODE MARKOUT] 和 [ [mf \_ TOPONODE \_ \_ MARKIN](mf-toponode-markin-here-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="d87ea-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="d87ea-120">它們無法在相同分支內的不同節點上設定。</span><span class="sxs-lookup"><span data-stu-id="d87ea-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="d87ea-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="d87ea-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87ea-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d87ea-122">Requirements</span></span>



| <span data-ttu-id="d87ea-123">需求</span><span class="sxs-lookup"><span data-stu-id="d87ea-123">Requirement</span></span> | <span data-ttu-id="d87ea-124">值</span><span class="sxs-lookup"><span data-stu-id="d87ea-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d87ea-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d87ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d87ea-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d87ea-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d87ea-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d87ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d87ea-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d87ea-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d87ea-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d87ea-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d87ea-130"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d87ea-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d87ea-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d87ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87ea-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d87ea-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d87ea-133">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d87ea-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d87ea-134">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d87ea-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d87ea-135">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d87ea-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d87ea-136">**MF \_ TOPONODE \_ MARKIN \_ 這裡**</span><span class="sxs-lookup"><span data-stu-id="d87ea-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="d87ea-137">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="d87ea-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




