---
description: 包含與拓撲節點相關聯之媒體來源的指標。
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: 'MF_TOPONODE_SOURCE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512276"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="e8ac9-103">MF \_ TOPONODE \_ 來源屬性</span><span class="sxs-lookup"><span data-stu-id="e8ac9-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="e8ac9-104">包含與拓撲節點相關聯之媒體來源的指標。</span><span class="sxs-lookup"><span data-stu-id="e8ac9-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8ac9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e8ac9-105">Data type</span></span>

<span data-ttu-id="e8ac9-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e8ac9-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ac9-107">備註</span><span class="sxs-lookup"><span data-stu-id="e8ac9-107">Remarks</span></span>

<span data-ttu-id="e8ac9-108">此屬性適用于 (_ \* MF \_ 拓撲 \_ SOURCESTREAM \_ 節點 \* \* ) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="e8ac9-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="e8ac9-109">屬性的值是媒體來源 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e8ac9-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="e8ac9-110">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="e8ac9-110">This attribute is required.</span></span>

<span data-ttu-id="e8ac9-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e8ac9-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ac9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8ac9-112">Requirements</span></span>



| <span data-ttu-id="e8ac9-113">需求</span><span class="sxs-lookup"><span data-stu-id="e8ac9-113">Requirement</span></span> | <span data-ttu-id="e8ac9-114">值</span><span class="sxs-lookup"><span data-stu-id="e8ac9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ac9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8ac9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ac9-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8ac9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e8ac9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8ac9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ac9-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8ac9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8ac9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e8ac9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ac9-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ac9-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8ac9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8ac9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ac9-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e8ac9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e8ac9-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="e8ac9-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="e8ac9-124">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="e8ac9-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="e8ac9-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e8ac9-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e8ac9-126">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="e8ac9-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




