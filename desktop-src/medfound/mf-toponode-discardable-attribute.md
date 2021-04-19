---
description: 指定管線是否可以從拓撲節點卸載範例。
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: 'MF_TOPONODE_DISCARDABLE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989001"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="5c154-103">MF \_ TOPONODE \_ DISCARDABLE 屬性</span><span class="sxs-lookup"><span data-stu-id="5c154-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="5c154-104">指定管線是否可以從拓撲節點卸載範例。</span><span class="sxs-lookup"><span data-stu-id="5c154-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c154-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5c154-105">Data type</span></span>

<span data-ttu-id="5c154-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="5c154-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5c154-107">備註</span><span class="sxs-lookup"><span data-stu-id="5c154-107">Remarks</span></span>

<span data-ttu-id="5c154-108">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="5c154-108">This attribute applies to all node types.</span></span> <span data-ttu-id="5c154-109">一般而言，您會在 t 節點上設定此屬性，以指出次要輸出並不重要。</span><span class="sxs-lookup"><span data-stu-id="5c154-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="5c154-110">屬性的值是在節點上輸出資料流程的索引陣列。</span><span class="sxs-lookup"><span data-stu-id="5c154-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="5c154-111">如果設定這個屬性，則如果資料流程落後，管線可能會從指定的輸出資料流程中卸載樣本。</span><span class="sxs-lookup"><span data-stu-id="5c154-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="5c154-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5c154-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c154-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c154-113">Requirements</span></span>



| <span data-ttu-id="5c154-114">需求</span><span class="sxs-lookup"><span data-stu-id="5c154-114">Requirement</span></span> | <span data-ttu-id="5c154-115">值</span><span class="sxs-lookup"><span data-stu-id="5c154-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c154-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c154-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c154-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c154-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c154-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c154-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c154-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c154-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c154-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5c154-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c154-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c154-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c154-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c154-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c154-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5c154-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c154-124">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="5c154-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5c154-125">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="5c154-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5c154-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="5c154-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="5c154-127">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="5c154-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




