---
description: 提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'IInkAnalyzer：： SearchWithLanguageId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690575"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="386cd-103">IInkAnalyzer：： SearchWithLanguageId 方法</span><span class="sxs-lookup"><span data-stu-id="386cd-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="386cd-104">提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。</span><span class="sxs-lookup"><span data-stu-id="386cd-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="386cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="386cd-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="386cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="386cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386cd-107">*bstrPhraseToMatch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="386cd-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386cd-108">將在替代中針對目前分析之筆劃找到的片語。</span><span class="sxs-lookup"><span data-stu-id="386cd-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="386cd-109">*lSearchStringLanguageId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="386cd-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386cd-110">與傳遞的字串相關聯的 LCID。</span><span class="sxs-lookup"><span data-stu-id="386cd-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="386cd-111">用來在內部轉換案例，以支援不區分大小寫的比較。</span><span class="sxs-lookup"><span data-stu-id="386cd-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="386cd-112">*pulSearchResultCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="386cd-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="386cd-113">從搜尋傳回的結果數目上限。</span><span class="sxs-lookup"><span data-stu-id="386cd-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="386cd-114">*ppulStrokeCountPerResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="386cd-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="386cd-115">每個搜尋結果中筆劃數目陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="386cd-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="386cd-116">*pulStrokeIdsCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="386cd-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="386cd-117">*PpulStrokeIds* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="386cd-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="386cd-118">*ppulStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="386cd-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="386cd-119">筆觸識別碼陣列的指標，代表一組筆觸。</span><span class="sxs-lookup"><span data-stu-id="386cd-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="386cd-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="386cd-120">Return value</span></span>

<span data-ttu-id="386cd-121">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="386cd-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="386cd-122">備註</span><span class="sxs-lookup"><span data-stu-id="386cd-122">Remarks</span></span>

<span data-ttu-id="386cd-123">此搜尋會尋找多單字和單一單字子字串。</span><span class="sxs-lookup"><span data-stu-id="386cd-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="386cd-124">系統會搜尋替代辨識結果和替代 segmentations。</span><span class="sxs-lookup"><span data-stu-id="386cd-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="386cd-125">所有傳入的字串都會轉換成單一大小寫，以利用目前線程的 LCID 來進行這項轉換，以遵循文化特性案例慣例。</span><span class="sxs-lookup"><span data-stu-id="386cd-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="386cd-126">傳遞的字串會被視為片語。</span><span class="sxs-lookup"><span data-stu-id="386cd-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="386cd-127">單字和字元必須以指定的順序出現在筆劃的 alterantes 中。</span><span class="sxs-lookup"><span data-stu-id="386cd-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="386cd-128">片語的第一個和最後一個單字可能會以子字串的形式來比對， (第一個出現在替代的單字和最後一個單字的 begginging 出現在其中一個) ，但是任何其他文字 (片語內的單字) 必須顯示為全字。</span><span class="sxs-lookup"><span data-stu-id="386cd-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="386cd-129">如果傳入的字串在字元之間沒有空白字元，則可以在替代的單一單字內的任何位置找到子字串。</span><span class="sxs-lookup"><span data-stu-id="386cd-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="386cd-130">只有字元之間存在空格才會變更搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="386cd-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="386cd-131">未以字元括住的空白字元會被忽略。</span><span class="sxs-lookup"><span data-stu-id="386cd-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="386cd-132">空白字元的類型會被忽略 (索引標籤或字元之間的空格會提供相同的結果) 。</span><span class="sxs-lookup"><span data-stu-id="386cd-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="386cd-133">空白字元的數量並不重要-字元之間的一個空格或兩個空格將提供相同的結果。</span><span class="sxs-lookup"><span data-stu-id="386cd-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="386cd-134">搜尋不會產生 PopulateCoNtextNode 事件。</span><span class="sxs-lookup"><span data-stu-id="386cd-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="386cd-135">只會搜尋已填入的筆劃。</span><span class="sxs-lookup"><span data-stu-id="386cd-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="386cd-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="386cd-136">Requirements</span></span>



| <span data-ttu-id="386cd-137">需求</span><span class="sxs-lookup"><span data-stu-id="386cd-137">Requirement</span></span> | <span data-ttu-id="386cd-138">值</span><span class="sxs-lookup"><span data-stu-id="386cd-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="386cd-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="386cd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="386cd-140">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="386cd-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="386cd-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="386cd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="386cd-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="386cd-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="386cd-143">標頭</span><span class="sxs-lookup"><span data-stu-id="386cd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="386cd-144"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="386cd-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="386cd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="386cd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="386cd-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="386cd-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="386cd-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="386cd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386cd-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="386cd-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




