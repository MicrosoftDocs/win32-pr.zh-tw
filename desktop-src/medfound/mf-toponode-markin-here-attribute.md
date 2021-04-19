---
description: 指定管線是否在此節點套用標記。
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: 'MF_TOPONODE_MARKIN_HERE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983346"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="4919d-103">MF \_ TOPONODE \_ MARKIN \_ 這裡屬性</span><span class="sxs-lookup"><span data-stu-id="4919d-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="4919d-104">指定管線是否在此節點套用標記。</span><span class="sxs-lookup"><span data-stu-id="4919d-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="4919d-105">[標記] 是簡報開始的起點。</span><span class="sxs-lookup"><span data-stu-id="4919d-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="4919d-106">如果管線元件在標記點之前產生資料，則不會呈現資料。</span><span class="sxs-lookup"><span data-stu-id="4919d-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="4919d-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4919d-107">Data type</span></span>

<span data-ttu-id="4919d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4919d-108">**UINT32**</span></span>

<span data-ttu-id="4919d-109">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="4919d-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4919d-110">備註</span><span class="sxs-lookup"><span data-stu-id="4919d-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4919d-111">大部分的應用程式不需要使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="4919d-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="4919d-112">[媒體會話](media-session.md)會自動設定此屬性（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="4919d-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="4919d-113">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="4919d-113">This attribute applies to all node types.</span></span> <span data-ttu-id="4919d-114">如果屬性為 **TRUE**，媒體基礎管線會修剪這個節點的輸出範例，以符合簡報的開始時間。</span><span class="sxs-lookup"><span data-stu-id="4919d-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="4919d-115">拓撲載入器會在解析拓撲時設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4919d-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="4919d-116">建議將此屬性設定為 **TRUE** 時，拓撲的每個分支中必須只有一個節點。</span><span class="sxs-lookup"><span data-stu-id="4919d-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="4919d-117">拓撲分支會定義為從來源節點到輸出節點的路徑。</span><span class="sxs-lookup"><span data-stu-id="4919d-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="4919d-118">在分支中，您 [ \_ \_ \_ ](mf-toponode-markout-here-attribute.md) \_ \_ \_ 必須在分支中的相同節點上設定 [TOPONODE MARKOUT] 和 [mf TOPONODE MARKIN] 屬性。</span><span class="sxs-lookup"><span data-stu-id="4919d-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="4919d-119">它們無法在相同分支內的不同節點上設定。</span><span class="sxs-lookup"><span data-stu-id="4919d-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="4919d-120">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4919d-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4919d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4919d-121">Requirements</span></span>



| <span data-ttu-id="4919d-122">需求</span><span class="sxs-lookup"><span data-stu-id="4919d-122">Requirement</span></span> | <span data-ttu-id="4919d-123">值</span><span class="sxs-lookup"><span data-stu-id="4919d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4919d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4919d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4919d-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4919d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4919d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4919d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4919d-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4919d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4919d-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4919d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4919d-129"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4919d-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4919d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4919d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4919d-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4919d-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4919d-132">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4919d-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4919d-133">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4919d-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4919d-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="4919d-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4919d-135">**MF \_ TOPONODE \_ MARKOUT \_ 這裡**</span><span class="sxs-lookup"><span data-stu-id="4919d-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="4919d-136">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="4919d-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




