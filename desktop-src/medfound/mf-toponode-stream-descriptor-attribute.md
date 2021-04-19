---
description: 包含媒體來源的資料流程描述元指標。
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: 'MF_TOPONODE_STREAM_DESCRIPTOR 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986389"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="04876-103">MF \_ TOPONODE \_ 資料流程 \_ 描述項屬性</span><span class="sxs-lookup"><span data-stu-id="04876-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="04876-104">包含媒體來源的資料流程描述元指標。</span><span class="sxs-lookup"><span data-stu-id="04876-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="04876-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="04876-105">Data type</span></span>

<span data-ttu-id="04876-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="04876-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="04876-107">備註</span><span class="sxs-lookup"><span data-stu-id="04876-107">Remarks</span></span>

<span data-ttu-id="04876-108">此屬性適用于 (_ \* MF \_ 拓撲 \_ SOURCESTREAM \_ 節點 \* \* ) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="04876-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="04876-109">屬性的值是資料流程描述項之 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="04876-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="04876-110">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="04876-110">This attribute is required.</span></span>

<span data-ttu-id="04876-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="04876-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="04876-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="04876-112">Requirements</span></span>



| <span data-ttu-id="04876-113">需求</span><span class="sxs-lookup"><span data-stu-id="04876-113">Requirement</span></span> | <span data-ttu-id="04876-114">值</span><span class="sxs-lookup"><span data-stu-id="04876-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04876-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04876-115">Minimum supported client</span></span><br/> | <span data-ttu-id="04876-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04876-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04876-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04876-117">Minimum supported server</span></span><br/> | <span data-ttu-id="04876-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04876-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="04876-119">標頭</span><span class="sxs-lookup"><span data-stu-id="04876-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="04876-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="04876-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04876-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04876-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04876-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="04876-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="04876-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="04876-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="04876-124">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="04876-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="04876-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="04876-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="04876-126">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="04876-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




