---
title: 'TF_IAS_ 常數 (Msctf) '
description: TF \_ IAS \_ \ 常數是在方法中用來做為位旗標，這些旗標會在選取範圍或插入點插入文字或內嵌的物件。
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999813"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="92b21-103">TF \_ IAS \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="92b21-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="92b21-104">TF \_ IAS \_ \* 常數是在方法中用來做為位旗標，這些旗標會在選取範圍或插入點插入文字或內嵌的物件。</span><span class="sxs-lookup"><span data-stu-id="92b21-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="92b21-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="92b21-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="92b21-106">Description</span><span class="sxs-lookup"><span data-stu-id="92b21-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="92b21-107"><dt>**TF \_IAS \_ NOQUERY**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="92b21-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="92b21-108">在結束時插入文字，範圍指標會設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="92b21-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="92b21-109">無法與 TF \_ IAS QUERYONLY 旗標合併使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92b21-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="92b21-110"><dt>**TF \_IAS \_ QUERYONLY**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="92b21-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="92b21-111">請勿執行插入。</span><span class="sxs-lookup"><span data-stu-id="92b21-111">Do not perform the insert.</span></span> <span data-ttu-id="92b21-112">呼叫端只需要設定範圍指標。</span><span class="sxs-lookup"><span data-stu-id="92b21-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="92b21-113">無法與 TF \_ IAS NOQUERY 旗標合併使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92b21-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="92b21-114"><dt>**TF \_IAS \_ 沒有 \_ 預設 \_ 組合**</dt> <dt> ( 0x80000000 )</dt></span><span class="sxs-lookup"><span data-stu-id="92b21-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="92b21-115">如果需要組合，TSF 將不會建立預設的組合。</span><span class="sxs-lookup"><span data-stu-id="92b21-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="92b21-116">呼叫端必須在範圍內開始撰寫。</span><span class="sxs-lookup"><span data-stu-id="92b21-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="92b21-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="92b21-117">Requirements</span></span>



| <span data-ttu-id="92b21-118">需求</span><span class="sxs-lookup"><span data-stu-id="92b21-118">Requirement</span></span> | <span data-ttu-id="92b21-119">值</span><span class="sxs-lookup"><span data-stu-id="92b21-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92b21-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92b21-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92b21-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92b21-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="92b21-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92b21-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92b21-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92b21-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="92b21-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="92b21-124">Redistributable</span></span><br/>          | <span data-ttu-id="92b21-125">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="92b21-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="92b21-126">標頭</span><span class="sxs-lookup"><span data-stu-id="92b21-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92b21-127"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="92b21-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="92b21-128">Idl</span><span class="sxs-lookup"><span data-stu-id="92b21-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92b21-129"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="92b21-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b21-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92b21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b21-131">ITextStoreACP：： InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="92b21-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="92b21-132">ITextStoreACP：： InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="92b21-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="92b21-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="92b21-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="92b21-134">ITextStoreAnchor::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="92b21-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="92b21-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="92b21-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="92b21-136">ITfInsertAtSelection::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="92b21-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





