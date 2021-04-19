---
description: 處理斷詞在索引時間和查詢期間所識別的文字。
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: 'IWordSink 介面 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984164"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="0b93d-103">IWordSink 介面</span><span class="sxs-lookup"><span data-stu-id="0b93d-103">IWordSink interface</span></span>

<span data-ttu-id="0b93d-104">處理斷詞在索引時間和查詢期間所識別的文字。</span><span class="sxs-lookup"><span data-stu-id="0b93d-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="0b93d-105">成員</span><span class="sxs-lookup"><span data-stu-id="0b93d-105">Members</span></span>

<span data-ttu-id="0b93d-106">**IWordSink** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0b93d-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b93d-107">**IWordSink** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b93d-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="0b93d-108">方法</span><span class="sxs-lookup"><span data-stu-id="0b93d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b93d-109">方法</span><span class="sxs-lookup"><span data-stu-id="0b93d-109">Methods</span></span>

<span data-ttu-id="0b93d-110">**IWordSink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0b93d-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="0b93d-111">方法</span><span class="sxs-lookup"><span data-stu-id="0b93d-111">Method</span></span>                                             | <span data-ttu-id="0b93d-112">描述</span><span class="sxs-lookup"><span data-stu-id="0b93d-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b93d-113">**EndAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="0b93d-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="0b93d-114">以斷詞工具在索引時間產生的替代片語順序表示最後一個片語的結尾。</span><span class="sxs-lookup"><span data-stu-id="0b93d-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="0b93d-115">**PutAltWord**</span><span class="sxs-lookup"><span data-stu-id="0b93d-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="0b93d-116">在 **IWordSink** 物件中放置替代單字和其位置。</span><span class="sxs-lookup"><span data-stu-id="0b93d-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="0b93d-117">**PutBreak**</span><span class="sxs-lookup"><span data-stu-id="0b93d-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="0b93d-118">將中斷點放在前面的單字後面。</span><span class="sxs-lookup"><span data-stu-id="0b93d-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="0b93d-119">**PutWord**</span><span class="sxs-lookup"><span data-stu-id="0b93d-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="0b93d-120">在 **IWordSink** 物件中放置單字和其位置。</span><span class="sxs-lookup"><span data-stu-id="0b93d-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="0b93d-121">**StartAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="0b93d-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="0b93d-122">表示在索引時間于斷詞工具產生的替代片語序列中，片語之間的界限。</span><span class="sxs-lookup"><span data-stu-id="0b93d-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b93d-123">備註</span><span class="sxs-lookup"><span data-stu-id="0b93d-123">Remarks</span></span>

<span data-ttu-id="0b93d-124">Windows Search 會建立並初始化 **IWordSink** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="0b93d-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="0b93d-125">**IWordSink** 物件會在初始化期間接收 *fQuery* 參數，並使用此參數來決定使用物件的斷詞內容。</span><span class="sxs-lookup"><span data-stu-id="0b93d-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="0b93d-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker)執行會在 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)方法中收到 **IWordSink** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0b93d-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b93d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b93d-127">Requirements</span></span>



| <span data-ttu-id="0b93d-128">需求</span><span class="sxs-lookup"><span data-stu-id="0b93d-128">Requirement</span></span> | <span data-ttu-id="0b93d-129">值</span><span class="sxs-lookup"><span data-stu-id="0b93d-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b93d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b93d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0b93d-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b93d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0b93d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b93d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0b93d-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b93d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b93d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="0b93d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b93d-135"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b93d-135"><dt>Search.h</dt></span></span> </dl> |



 

 
