---
description: 以斷詞工具在索引時間產生的替代片語順序表示最後一個片語的結尾。
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'IWordSink：： EndAltPhrase 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191192"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="90a69-103">IWordSink：： EndAltPhrase 方法</span><span class="sxs-lookup"><span data-stu-id="90a69-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="90a69-104">以斷詞工具在索引時間產生的替代片語順序表示最後一個片語的結尾。</span><span class="sxs-lookup"><span data-stu-id="90a69-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a69-105">語法</span><span class="sxs-lookup"><span data-stu-id="90a69-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="90a69-106">參數</span><span class="sxs-lookup"><span data-stu-id="90a69-106">Parameters</span></span>

<span data-ttu-id="90a69-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="90a69-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90a69-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="90a69-108">Return value</span></span>

<span data-ttu-id="90a69-109">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="90a69-109">This method can return one of these values.</span></span>



| <span data-ttu-id="90a69-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="90a69-110">Return code</span></span>                                                                                           | <span data-ttu-id="90a69-111">Description</span><span class="sxs-lookup"><span data-stu-id="90a69-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90a69-112"><dt>**\_ \_ 僅限 WBREAK E 查詢 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90a69-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="90a69-113">查詢期間會呼叫 [**EndAltPhrase**](iwordsink-endaltphrase.md) 。</span><span class="sxs-lookup"><span data-stu-id="90a69-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90a69-114">備註</span><span class="sxs-lookup"><span data-stu-id="90a69-114">Remarks</span></span>

<span data-ttu-id="90a69-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker)執行會從 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)方法呼叫 **IWordSink：： EndAltPhrase** ，以終止一系列的替代片語。</span><span class="sxs-lookup"><span data-stu-id="90a69-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="90a69-116">呼叫 [**IWordSink：： StartAltPhrase**](iwordsink-startaltphrase.md) 方法，以表示一個片語的結尾和另一個句子順序的開頭。</span><span class="sxs-lookup"><span data-stu-id="90a69-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="90a69-117">只有序列中的最後一個片語會透過呼叫 **EndAltPhrase** 來終止。</span><span class="sxs-lookup"><span data-stu-id="90a69-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a69-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="90a69-118">Requirements</span></span>



| <span data-ttu-id="90a69-119">需求</span><span class="sxs-lookup"><span data-stu-id="90a69-119">Requirement</span></span> | <span data-ttu-id="90a69-120">值</span><span class="sxs-lookup"><span data-stu-id="90a69-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90a69-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90a69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90a69-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90a69-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90a69-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90a69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90a69-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90a69-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="90a69-125">標頭</span><span class="sxs-lookup"><span data-stu-id="90a69-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90a69-126"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="90a69-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90a69-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90a69-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a69-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="90a69-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
