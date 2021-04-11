---
description: 提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'IInkAnalyzer：： Search 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113325"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="554fa-103">IInkAnalyzer：： Search 方法</span><span class="sxs-lookup"><span data-stu-id="554fa-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="554fa-104">提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。</span><span class="sxs-lookup"><span data-stu-id="554fa-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="554fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="554fa-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="554fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="554fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554fa-107">*bstrPhraseToMatch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="554fa-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554fa-108">將在替代中針對目前分析之筆劃找到的片語。</span><span class="sxs-lookup"><span data-stu-id="554fa-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="554fa-109">*pulSearchResultCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="554fa-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="554fa-110">從搜尋傳回的結果數目上限。</span><span class="sxs-lookup"><span data-stu-id="554fa-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="554fa-111">*ppulStrokeCountPerResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="554fa-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="554fa-112">每個搜尋結果中筆劃數目陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="554fa-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="554fa-113">*pulStrokeIdsCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="554fa-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="554fa-114">*PpulStrokeIds* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="554fa-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="554fa-115">*ppulStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="554fa-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="554fa-116">筆觸識別碼陣列的指標，代表一組筆觸。</span><span class="sxs-lookup"><span data-stu-id="554fa-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="554fa-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="554fa-117">Return value</span></span>

<span data-ttu-id="554fa-118">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="554fa-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="554fa-119">備註</span><span class="sxs-lookup"><span data-stu-id="554fa-119">Remarks</span></span>

<span data-ttu-id="554fa-120">此搜尋會尋找多單字和單一單字子字串。</span><span class="sxs-lookup"><span data-stu-id="554fa-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="554fa-121">系統會搜尋替代辨識結果和替代 segmentations。</span><span class="sxs-lookup"><span data-stu-id="554fa-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="554fa-122">所有傳入的字串都會轉換成單一大小寫，以利用目前線程的 LCID 來進行這項轉換，以遵循文化特性案例慣例。</span><span class="sxs-lookup"><span data-stu-id="554fa-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="554fa-123">傳遞的字串會被視為片語。</span><span class="sxs-lookup"><span data-stu-id="554fa-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="554fa-124">單字和字元必須以指定的順序出現在筆劃的 alterantes 中。</span><span class="sxs-lookup"><span data-stu-id="554fa-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="554fa-125">片語的第一個和最後一個單字可能會以子字串的形式來比對， (第一個出現在替代的單字和最後一個單字的 begginging 出現在其中一個) ，但是任何其他文字 (片語內的單字) 必須顯示為全字。</span><span class="sxs-lookup"><span data-stu-id="554fa-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="554fa-126">如果傳入的字串在字元之間沒有空白字元，則可以在替代的單一單字內的任何位置找到子字串。</span><span class="sxs-lookup"><span data-stu-id="554fa-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="554fa-127">只有字元之間存在空格才會變更搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="554fa-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="554fa-128">未以字元括住的空白字元會被忽略。</span><span class="sxs-lookup"><span data-stu-id="554fa-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="554fa-129">空白字元的類型會被忽略 (索引標籤或字元之間的空格會提供相同的結果) 。</span><span class="sxs-lookup"><span data-stu-id="554fa-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="554fa-130">空白字元的數量並不重要-字元之間的一個空格或兩個空格將提供相同的結果。</span><span class="sxs-lookup"><span data-stu-id="554fa-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="554fa-131">搜尋不會產生 PopulateCoNtextNode 事件。</span><span class="sxs-lookup"><span data-stu-id="554fa-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="554fa-132">只會搜尋已填入的筆劃。</span><span class="sxs-lookup"><span data-stu-id="554fa-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="554fa-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="554fa-133">Requirements</span></span>



| <span data-ttu-id="554fa-134">需求</span><span class="sxs-lookup"><span data-stu-id="554fa-134">Requirement</span></span> | <span data-ttu-id="554fa-135">值</span><span class="sxs-lookup"><span data-stu-id="554fa-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="554fa-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="554fa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="554fa-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="554fa-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="554fa-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="554fa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="554fa-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="554fa-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="554fa-140">標頭</span><span class="sxs-lookup"><span data-stu-id="554fa-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="554fa-141"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="554fa-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="554fa-142">DLL</span><span class="sxs-lookup"><span data-stu-id="554fa-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="554fa-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="554fa-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="554fa-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="554fa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554fa-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="554fa-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




