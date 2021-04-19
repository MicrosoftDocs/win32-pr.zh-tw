---
description: 在 IWordSink 物件中放置替代單字和其位置。
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: 'IWordSink：:P utAltWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971179"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="85f25-103">IWordSink：:P utAltWord 方法</span><span class="sxs-lookup"><span data-stu-id="85f25-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="85f25-104">在 [**IWordSink**](iwordsink.md) 物件中放置替代單字和其位置。</span><span class="sxs-lookup"><span data-stu-id="85f25-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f25-105">語法</span><span class="sxs-lookup"><span data-stu-id="85f25-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="85f25-106">參數</span><span class="sxs-lookup"><span data-stu-id="85f25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f25-107">*cwc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85f25-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f25-108">*PwcInBuf* 中的字元數。</span><span class="sxs-lookup"><span data-stu-id="85f25-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="85f25-109">*pwcInBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85f25-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f25-110">緩衝區的指標，此緩衝區包含來源文字的替代文字形式。</span><span class="sxs-lookup"><span data-stu-id="85f25-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="85f25-111">**PutAltWord** 不會修改這個參數。</span><span class="sxs-lookup"><span data-stu-id="85f25-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="85f25-112">您可以視需要從 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)傳遞 *pTextSource* 參數。</span><span class="sxs-lookup"><span data-stu-id="85f25-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="85f25-113">*cwcSrcLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85f25-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f25-114">來源文字緩衝區中的字元數 (由 *pTextSource* 參數指定為 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 對應至 *pwcInBuf* 中包含的單字。</span><span class="sxs-lookup"><span data-stu-id="85f25-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="85f25-115">*cwcSrcPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85f25-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f25-116">來源文字緩衝區中 *pwcInBuf* 文字的開始位置， (由 *pTextSource* 參數指定為 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 。</span><span class="sxs-lookup"><span data-stu-id="85f25-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f25-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="85f25-117">Return value</span></span>

<span data-ttu-id="85f25-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85f25-118">This method can return one of these values.</span></span>



| <span data-ttu-id="85f25-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="85f25-119">Return code</span></span>                                                                                              | <span data-ttu-id="85f25-120">Description</span><span class="sxs-lookup"><span data-stu-id="85f25-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85f25-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="85f25-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="85f25-122">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="85f25-122">The operation was completed successfully.</span></span> <span data-ttu-id="85f25-123">也指出不會再處理任何文字。</span><span class="sxs-lookup"><span data-stu-id="85f25-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="85f25-124"><dt>**語言 \_S \_ 大型 \_ 單字**</dt></span><span class="sxs-lookup"><span data-stu-id="85f25-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="85f25-125">*Cwc* 的值大於 [**IWordBreaker：： Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)中指定的 *ulMaxTokenSize* 值。</span><span class="sxs-lookup"><span data-stu-id="85f25-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="85f25-126">備註</span><span class="sxs-lookup"><span data-stu-id="85f25-126">Remarks</span></span>

<span data-ttu-id="85f25-127">**PutAltWord** 會將替代形式的單字放在 [**IWordSink**](iwordsink.md)中。</span><span class="sxs-lookup"><span data-stu-id="85f25-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="85f25-128">在 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 中，單字會放在與文字來源 (*pTextSource* 中原始單字相同的位置。</span><span class="sxs-lookup"><span data-stu-id="85f25-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="85f25-129">根據預設， **PutAltWord** 會使用 **WORDREP \_ break \_ EOW** break type from [**WORDREP \_ break \_ type**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) 列舉型別來終止單字。</span><span class="sxs-lookup"><span data-stu-id="85f25-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f25-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="85f25-130">Requirements</span></span>



| <span data-ttu-id="85f25-131">需求</span><span class="sxs-lookup"><span data-stu-id="85f25-131">Requirement</span></span> | <span data-ttu-id="85f25-132">值</span><span class="sxs-lookup"><span data-stu-id="85f25-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="85f25-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85f25-133">Minimum supported client</span></span><br/> | <span data-ttu-id="85f25-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85f25-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="85f25-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85f25-135">Minimum supported server</span></span><br/> | <span data-ttu-id="85f25-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85f25-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="85f25-137">標頭</span><span class="sxs-lookup"><span data-stu-id="85f25-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="85f25-138"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="85f25-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85f25-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85f25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f25-140">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="85f25-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
