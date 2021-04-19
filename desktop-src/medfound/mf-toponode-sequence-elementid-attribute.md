---
description: 指定包含此來源節點的元素。
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: 'MF_TOPONODE_SEQUENCE_ELEMENTID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972279"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="b67ed-103">MF \_ TOPONODE \_ 序列 \_ ELEMENTID 屬性</span><span class="sxs-lookup"><span data-stu-id="b67ed-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="b67ed-104">指定包含此來源節點的元素。</span><span class="sxs-lookup"><span data-stu-id="b67ed-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="b67ed-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b67ed-105">Data type</span></span>

<span data-ttu-id="b67ed-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b67ed-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b67ed-107">備註</span><span class="sxs-lookup"><span data-stu-id="b67ed-107">Remarks</span></span>

<span data-ttu-id="b67ed-108">這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="b67ed-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="b67ed-109">媒體管線會使用這個屬性來探索媒體來源是否屬於相同元素的一部分。</span><span class="sxs-lookup"><span data-stu-id="b67ed-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="b67ed-110">管線會將屬於相同元素的所有來源節點視為具有相同的時鐘。</span><span class="sxs-lookup"><span data-stu-id="b67ed-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="b67ed-111">當管線將包含來源節點的新拓撲排入佇列，而這些來源節點屬於先前拓撲中的元素時，管線會將這些來源節點視為與先前拓撲中該專案的來源節點相同的時鐘。</span><span class="sxs-lookup"><span data-stu-id="b67ed-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="b67ed-112">媒體管線不會以不同的頻率速率來更正來源節點的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="b67ed-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="b67ed-113">可提供拓撲的媒體來源應該會執行 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 介面或 [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) 介面。</span><span class="sxs-lookup"><span data-stu-id="b67ed-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="b67ed-114">提供拓撲的媒體來源應該在其所建立的每個來源節點上設定 **MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b67ed-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="b67ed-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b67ed-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b67ed-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b67ed-116">Requirements</span></span>



| <span data-ttu-id="b67ed-117">需求</span><span class="sxs-lookup"><span data-stu-id="b67ed-117">Requirement</span></span> | <span data-ttu-id="b67ed-118">值</span><span class="sxs-lookup"><span data-stu-id="b67ed-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b67ed-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b67ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b67ed-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b67ed-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b67ed-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b67ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b67ed-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b67ed-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b67ed-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b67ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b67ed-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b67ed-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b67ed-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b67ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67ed-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b67ed-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b67ed-127">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b67ed-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b67ed-128">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b67ed-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b67ed-129">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="b67ed-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="b67ed-130">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="b67ed-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="b67ed-131">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b67ed-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b67ed-132">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="b67ed-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="b67ed-133">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="b67ed-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




