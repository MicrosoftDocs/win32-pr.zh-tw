---
title: 'TS_ATTR_ 常數 (Textstor) '
description: TS \_ ATTR \_ \ 常數可用來取得和變更檔案屬性的值。 這些常數會在 ITextStoreACP 和 ITextStoreAnchor 方法中形成可能的等位旗標值。
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466161"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="91207-104">TS \_ ATTR \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="91207-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="91207-105">TS \_ ATTR \_ \* 常數可用來取得和變更 document 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="91207-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="91207-106">這些常數會在 [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) 和 [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) 方法中形成可能的等位旗標值。</span><span class="sxs-lookup"><span data-stu-id="91207-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="91207-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="91207-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="91207-108">Description</span><span class="sxs-lookup"><span data-stu-id="91207-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="91207-109"><dt>**TS \_ATTR \_ 找到 \_**</dt>回溯 <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="91207-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="91207-110">從開始字元或錨點位置向後搜尋，以取得轉換在檔案屬性值中發生的位置。</span><span class="sxs-lookup"><span data-stu-id="91207-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="91207-111">預設值為「向前搜尋」。</span><span class="sxs-lookup"><span data-stu-id="91207-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="91207-112"><dt>**TS \_ATTR \_ FIND \_ 需要 \_ OFFSET**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="91207-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="91207-113">傳回開始字元或錨點位置之間的字元數 (**acpStart** 在 [ITextStoreACP：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) 或 **PaStart** in [ITextStoreAnchor：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) 和發生屬性轉換的位置。</span><span class="sxs-lookup"><span data-stu-id="91207-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="91207-114"><dt>**TS \_ATTR \_ FIND \_ UPDATESTART**</dt> <dt> ( 0x4 )</dt></span><span class="sxs-lookup"><span data-stu-id="91207-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="91207-115">供 [ITextStoreAnchor：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) 在下一個屬性轉換時放置輸入錨點（如果找到的話）。</span><span class="sxs-lookup"><span data-stu-id="91207-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="91207-116">否則，不會修改輸入錨點。</span><span class="sxs-lookup"><span data-stu-id="91207-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="91207-117"><dt>**TS \_ATTR \_ 尋找 \_ 想要的 \_ 值**</dt> <dt> ( 0x8 )</dt></span><span class="sxs-lookup"><span data-stu-id="91207-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="91207-118">將支援的檔案屬性值載入 [TS \_ ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) 結構。</span><span class="sxs-lookup"><span data-stu-id="91207-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="91207-119"><dt>**TS \_ATTR \_ FIND \_ 需要 \_ END**</dt> <dt> ( 0x10 )</dt></span><span class="sxs-lookup"><span data-stu-id="91207-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="91207-120">供 [ITextStoreACP：： RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) 和 [ITextStoreAnchor：： RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) 用來取得以指定的字元或錨點位置結尾的檔案屬性值。</span><span class="sxs-lookup"><span data-stu-id="91207-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="91207-121"><dt>**TS \_ATTR \_ FIND \_ HIDDEN**</dt> <dt> ( 0x20 )</dt></span><span class="sxs-lookup"><span data-stu-id="91207-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="91207-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="91207-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="91207-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="91207-123">Requirements</span></span>



| <span data-ttu-id="91207-124">需求</span><span class="sxs-lookup"><span data-stu-id="91207-124">Requirement</span></span> | <span data-ttu-id="91207-125">值</span><span class="sxs-lookup"><span data-stu-id="91207-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91207-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91207-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91207-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91207-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="91207-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91207-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91207-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91207-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91207-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="91207-130">Redistributable</span></span><br/>          | <span data-ttu-id="91207-131">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="91207-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="91207-132">標頭</span><span class="sxs-lookup"><span data-stu-id="91207-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="91207-133"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="91207-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="91207-134">Idl</span><span class="sxs-lookup"><span data-stu-id="91207-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91207-135"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="91207-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91207-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91207-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91207-137">TS \_ ATTRID</span><span class="sxs-lookup"><span data-stu-id="91207-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="91207-138">TS \_ ATTRVAL</span><span class="sxs-lookup"><span data-stu-id="91207-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="91207-139">ITextStoreACP：： FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="91207-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="91207-140">ITextStoreACP：： RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="91207-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="91207-141">ITextStoreAnchor::FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="91207-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="91207-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="91207-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





