---
description: 指定拓撲節點的基礎物件是否為解碼器。
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: 'MF_TOPONODE_DECODER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194859"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="c9325-103">MF \_ TOPONODE \_ 解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="c9325-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="c9325-104">指定拓撲節點的基礎物件是否為解碼器。</span><span class="sxs-lookup"><span data-stu-id="c9325-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9325-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c9325-105">Data type</span></span>

<span data-ttu-id="c9325-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c9325-106">**UINT32**</span></span>

<span data-ttu-id="c9325-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="c9325-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9325-108">備註</span><span class="sxs-lookup"><span data-stu-id="c9325-108">Remarks</span></span>

<span data-ttu-id="c9325-109">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="c9325-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="c9325-110">如果這個屬性的值為非零值，則節點的基礎物件為一個解碼器。</span><span class="sxs-lookup"><span data-stu-id="c9325-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="c9325-111">拓撲載入器會在建立一個解碼器節點時設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c9325-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="c9325-112">如果應用程式手動將解碼器加入拓撲中，應用程式應該設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c9325-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="c9325-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c9325-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9325-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9325-114">Requirements</span></span>



| <span data-ttu-id="c9325-115">需求</span><span class="sxs-lookup"><span data-stu-id="c9325-115">Requirement</span></span> | <span data-ttu-id="c9325-116">值</span><span class="sxs-lookup"><span data-stu-id="c9325-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9325-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9325-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9325-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9325-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9325-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9325-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c9325-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9325-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9325-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c9325-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9325-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9325-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9325-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9325-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9325-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c9325-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9325-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c9325-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c9325-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c9325-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c9325-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c9325-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="c9325-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="c9325-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




