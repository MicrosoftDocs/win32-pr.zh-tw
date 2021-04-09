---
description: 在 IWordFormSink 物件中放置替代的單字形式。
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: 'IWordFormSink：:P utAltWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689856"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="326b8-103">IWordFormSink：:P utAltWord 方法</span><span class="sxs-lookup"><span data-stu-id="326b8-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="326b8-104">在 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) 物件中放置替代的單字形式。</span><span class="sxs-lookup"><span data-stu-id="326b8-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="326b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="326b8-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="326b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="326b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="326b8-107">*pwcInBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="326b8-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="326b8-108">包含單字替代形式的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="326b8-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="326b8-109">*cwc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="326b8-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="326b8-110">*PwcInBuf* 中的字元數。</span><span class="sxs-lookup"><span data-stu-id="326b8-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="326b8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="326b8-111">Return value</span></span>

<span data-ttu-id="326b8-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="326b8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="326b8-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="326b8-113">Return code</span></span>                                                                                              | <span data-ttu-id="326b8-114">Description</span><span class="sxs-lookup"><span data-stu-id="326b8-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="326b8-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="326b8-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="326b8-116">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="326b8-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="326b8-117"><dt>**語言 \_S \_ 大型 \_ 單字**</dt></span><span class="sxs-lookup"><span data-stu-id="326b8-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="326b8-118">*Cwc* 的值大於 [**IStemmer：： Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init)中指定的 *ulMaxTokenSize* 值。</span><span class="sxs-lookup"><span data-stu-id="326b8-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="326b8-119">備註</span><span class="sxs-lookup"><span data-stu-id="326b8-119">Remarks</span></span>

<span data-ttu-id="326b8-120">這個方法是從 [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer)執行的 [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms)方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="326b8-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="326b8-121">單字的所有替代形式（最後一個除外）都會藉由呼叫 **IWordFormSink：:P utaltword** 放置在 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)物件中。</span><span class="sxs-lookup"><span data-stu-id="326b8-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="326b8-122">單字的最後一個替代形式（一律是單字的原始形式）是藉由呼叫 [**IWordFormSink：:P utword**](iwordformsink-putword.md)來處理。</span><span class="sxs-lookup"><span data-stu-id="326b8-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="326b8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="326b8-123">Requirements</span></span>



| <span data-ttu-id="326b8-124">需求</span><span class="sxs-lookup"><span data-stu-id="326b8-124">Requirement</span></span> | <span data-ttu-id="326b8-125">值</span><span class="sxs-lookup"><span data-stu-id="326b8-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="326b8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="326b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="326b8-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="326b8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="326b8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="326b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="326b8-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="326b8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="326b8-130">標頭</span><span class="sxs-lookup"><span data-stu-id="326b8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="326b8-131"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="326b8-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="326b8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="326b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="326b8-133">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="326b8-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
