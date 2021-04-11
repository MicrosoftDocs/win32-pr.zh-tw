---
description: 表示在索引時間于斷詞工具產生的替代片語序列中，片語之間的界限。
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'IWordSink：： StartAltPhrase 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191191"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="b778e-103">IWordSink：： StartAltPhrase 方法</span><span class="sxs-lookup"><span data-stu-id="b778e-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="b778e-104">表示在索引時間于斷詞工具產生的替代片語序列中，片語之間的界限。</span><span class="sxs-lookup"><span data-stu-id="b778e-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b778e-105">語法</span><span class="sxs-lookup"><span data-stu-id="b778e-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="b778e-106">參數</span><span class="sxs-lookup"><span data-stu-id="b778e-106">Parameters</span></span>

<span data-ttu-id="b778e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b778e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b778e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b778e-108">Return value</span></span>

<span data-ttu-id="b778e-109">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b778e-109">This method can return one of these values.</span></span>



| <span data-ttu-id="b778e-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b778e-110">Return code</span></span>                                                                                           | <span data-ttu-id="b778e-111">Description</span><span class="sxs-lookup"><span data-stu-id="b778e-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b778e-112"><dt>**\_ \_ 僅限 WBREAK E 查詢 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b778e-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="b778e-113">查詢期間會呼叫 [**StartAltPhrase**](iwordsink-startaltphrase.md) 。</span><span class="sxs-lookup"><span data-stu-id="b778e-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b778e-114">備註</span><span class="sxs-lookup"><span data-stu-id="b778e-114">Remarks</span></span>

<span data-ttu-id="b778e-115">每個替代片語的開頭都是 **StartAltPhrase** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="b778e-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="b778e-116">此片語會透過後續的 IWordSink 呼叫來放置在 [**IWordSink**](iwordsink.md) 物件中 [**：:P utword**](iwordsink-putword.md) 或 [**IWordSink：:P utaltword**](iwordsink-putaltword.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b778e-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="b778e-117">[**IWordSink：： EndAltPhrase**](iwordsink-endaltphrase.md)方法的呼叫會終止一系列片語中的最後一個替代片語。</span><span class="sxs-lookup"><span data-stu-id="b778e-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b778e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b778e-118">Requirements</span></span>



| <span data-ttu-id="b778e-119">需求</span><span class="sxs-lookup"><span data-stu-id="b778e-119">Requirement</span></span> | <span data-ttu-id="b778e-120">值</span><span class="sxs-lookup"><span data-stu-id="b778e-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b778e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b778e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b778e-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b778e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b778e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b778e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b778e-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b778e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b778e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b778e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b778e-126"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="b778e-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b778e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b778e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b778e-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="b778e-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




