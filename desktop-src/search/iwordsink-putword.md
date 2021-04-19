---
description: 在 IWordSink 物件中放置單字和其位置。
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: 'IWordSink：:P utWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973612"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="952ad-103">IWordSink：:P utWord 方法</span><span class="sxs-lookup"><span data-stu-id="952ad-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="952ad-104">在 [**IWordSink**](iwordsink.md) 物件中放置單字和其位置。</span><span class="sxs-lookup"><span data-stu-id="952ad-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="952ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="952ad-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="952ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="952ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="952ad-107">*cwc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952ad-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952ad-108">*PwcInBuf* 中的字元數。</span><span class="sxs-lookup"><span data-stu-id="952ad-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="952ad-109">*pwcInBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952ad-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952ad-110">緩衝區的指標，此緩衝區包含來源文字的替代文字形式。</span><span class="sxs-lookup"><span data-stu-id="952ad-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="952ad-111">**PutWord** 不會修改這個參數。</span><span class="sxs-lookup"><span data-stu-id="952ad-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="952ad-112">您可以視需要從 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)傳遞 *pTextSource* 參數。</span><span class="sxs-lookup"><span data-stu-id="952ad-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="952ad-113">*cwcSrcLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952ad-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952ad-114">來源文字緩衝區中的字元數 (由 *pTextSource* 參數指定為 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 對應至 *pwcInBuf* 中包含的單字。</span><span class="sxs-lookup"><span data-stu-id="952ad-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="952ad-115">*cwcSrcPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952ad-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952ad-116">來源文字緩衝區中 *pwcInBuf* 文字的開始位置， (由 *pTextSource* 參數指定為 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 。</span><span class="sxs-lookup"><span data-stu-id="952ad-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="952ad-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="952ad-117">Return value</span></span>

<span data-ttu-id="952ad-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="952ad-118">This method can return one of these values.</span></span>



| <span data-ttu-id="952ad-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="952ad-119">Return code</span></span>                                                                                              | <span data-ttu-id="952ad-120">Description</span><span class="sxs-lookup"><span data-stu-id="952ad-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="952ad-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="952ad-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="952ad-122">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="952ad-122">The operation was completed successfully.</span></span> <span data-ttu-id="952ad-123">也指出沒有其他文字可用來重填緩衝區。</span><span class="sxs-lookup"><span data-stu-id="952ad-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="952ad-124"><dt>**語言 \_S \_ 大型 \_ 單字**</dt></span><span class="sxs-lookup"><span data-stu-id="952ad-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="952ad-125">*Cwc* 的值大於 [**IWordBreaker：： Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)中指定的 *ulMaxTokenSize* 值。</span><span class="sxs-lookup"><span data-stu-id="952ad-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="952ad-126">備註</span><span class="sxs-lookup"><span data-stu-id="952ad-126">Remarks</span></span>

<span data-ttu-id="952ad-127">我們建議 **IWordSink：:P utword** 方法一律包含在 *pTextSource* 中找到的原始文字。</span><span class="sxs-lookup"><span data-stu-id="952ad-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="952ad-128">單字的替代形式會使用 [**IWordSink：:P utaltword**](iwordsink-putaltword.md)傳遞至 WordSink。</span><span class="sxs-lookup"><span data-stu-id="952ad-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="952ad-129">我們也建議 *pwcInBuf* 中的單字盡可能符合來源文字。</span><span class="sxs-lookup"><span data-stu-id="952ad-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="952ad-130">例如，盡可能保留大小寫和重音。</span><span class="sxs-lookup"><span data-stu-id="952ad-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="952ad-131">您必須對每個從 *pTextSource* 抓取的單字進行此呼叫，但已建立 [**IWordSink：:P utaltword**](iwordsink-putaltword.md) 呼叫的單字除外。</span><span class="sxs-lookup"><span data-stu-id="952ad-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="952ad-132">當單字儲存至 WordSink 時，會以 EOW 字元終止。</span><span class="sxs-lookup"><span data-stu-id="952ad-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="952ad-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="952ad-133">Requirements</span></span>



| <span data-ttu-id="952ad-134">需求</span><span class="sxs-lookup"><span data-stu-id="952ad-134">Requirement</span></span> | <span data-ttu-id="952ad-135">值</span><span class="sxs-lookup"><span data-stu-id="952ad-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="952ad-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="952ad-136">Minimum supported client</span></span><br/> | <span data-ttu-id="952ad-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952ad-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="952ad-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="952ad-138">Minimum supported server</span></span><br/> | <span data-ttu-id="952ad-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952ad-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="952ad-140">標頭</span><span class="sxs-lookup"><span data-stu-id="952ad-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="952ad-141"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="952ad-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="952ad-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="952ad-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952ad-143">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="952ad-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
