---
description: 將中斷點放在前面的單字後面。
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: 'IWordSink：:P utBreak 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318148"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="11230-103">IWordSink：:P utBreak 方法</span><span class="sxs-lookup"><span data-stu-id="11230-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="11230-104">將中斷點放在前面的單字後面。</span><span class="sxs-lookup"><span data-stu-id="11230-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="11230-105">語法</span><span class="sxs-lookup"><span data-stu-id="11230-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="11230-106">參數</span><span class="sxs-lookup"><span data-stu-id="11230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11230-107">*breakType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11230-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11230-108">[**WORDREP \_ 中斷 \_ 型**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85))別中的值，這個值表示 WordSink 在上一個字後面插入的中斷類型。</span><span class="sxs-lookup"><span data-stu-id="11230-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="11230-109">每個 break 都會佔用索引中的唯一位置。</span><span class="sxs-lookup"><span data-stu-id="11230-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="11230-110">因此，在單字之間插入中斷會變更單字之間的相對距離。</span><span class="sxs-lookup"><span data-stu-id="11230-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11230-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="11230-111">Return value</span></span>

<span data-ttu-id="11230-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="11230-112">This method can return one of these values.</span></span>



| <span data-ttu-id="11230-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="11230-113">Return code</span></span>                                                                          | <span data-ttu-id="11230-114">Description</span><span class="sxs-lookup"><span data-stu-id="11230-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="11230-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="11230-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="11230-116">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="11230-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11230-117">備註</span><span class="sxs-lookup"><span data-stu-id="11230-117">Remarks</span></span>

<span data-ttu-id="11230-118">[**IWordSinkPutWord**](iwordsink-putword.md)和 [**IWordSink：:P utaltword**](iwordsink-putaltword.md)方法會自動插入單字結尾 (EOW，以 \_ WORDREP break \_ [**\_ \_ 型**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85))別列舉型別在每個單字之後) 的 EOW break WORDREP 元素表示。</span><span class="sxs-lookup"><span data-stu-id="11230-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="11230-119">呼叫 **PutBreak** 方法，以插入除了單字結尾以外的分隔型別。</span><span class="sxs-lookup"><span data-stu-id="11230-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="11230-120">這個方法不會變更來源文字緩衝區 (*pSourceText*) 或遞增 (*cwc*) 的字元計數。</span><span class="sxs-lookup"><span data-stu-id="11230-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="11230-121">但是，它會遞增索引中的目前位置，並影響查詢結果。</span><span class="sxs-lookup"><span data-stu-id="11230-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="11230-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="11230-122">Requirements</span></span>



| <span data-ttu-id="11230-123">需求</span><span class="sxs-lookup"><span data-stu-id="11230-123">Requirement</span></span> | <span data-ttu-id="11230-124">值</span><span class="sxs-lookup"><span data-stu-id="11230-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11230-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11230-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11230-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11230-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="11230-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11230-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11230-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11230-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11230-129">標頭</span><span class="sxs-lookup"><span data-stu-id="11230-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="11230-130"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="11230-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11230-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11230-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11230-132">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="11230-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
