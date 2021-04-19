---
description: 指定與此拓撲節點相關聯的媒體接收器是否 rateless。
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: 'MF_TOPONODE_RATELESS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988671"
---
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="441a8-103">MF \_ TOPONODE \_ RATELESS 屬性</span><span class="sxs-lookup"><span data-stu-id="441a8-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="441a8-104">指定與此拓撲節點相關聯的媒體接收器是否 rateless。</span><span class="sxs-lookup"><span data-stu-id="441a8-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="441a8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="441a8-105">Data type</span></span>

<span data-ttu-id="441a8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="441a8-106">**UINT32**</span></span>

<span data-ttu-id="441a8-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="441a8-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="441a8-108">備註</span><span class="sxs-lookup"><span data-stu-id="441a8-108">Remarks</span></span>

<span data-ttu-id="441a8-109">這個屬性會套用至 (**MF \_ 拓撲 \_ 輸出 \_ 節點**) 的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="441a8-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="441a8-110">如果這個屬性的值不是零，則不論媒體接收器是否傳回 **MEDIASINK \_ rateless** 特性，媒體會話都會將媒體接收器視為 rateless 接收。</span><span class="sxs-lookup"><span data-stu-id="441a8-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="441a8-111">如果未設定此屬性，則會假設媒體接收器不是 rateless。</span><span class="sxs-lookup"><span data-stu-id="441a8-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="441a8-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="441a8-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="441a8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="441a8-113">Requirements</span></span>



| <span data-ttu-id="441a8-114">需求</span><span class="sxs-lookup"><span data-stu-id="441a8-114">Requirement</span></span> | <span data-ttu-id="441a8-115">值</span><span class="sxs-lookup"><span data-stu-id="441a8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="441a8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="441a8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="441a8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="441a8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="441a8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="441a8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="441a8-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="441a8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="441a8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="441a8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="441a8-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="441a8-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441a8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="441a8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441a8-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="441a8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="441a8-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="441a8-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="441a8-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="441a8-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="441a8-126">**IMFMediaSink::GetCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="441a8-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="441a8-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="441a8-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="441a8-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="441a8-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




