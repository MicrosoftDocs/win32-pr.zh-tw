---
description: 傳回指定之筆劃的地區設定識別碼。
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'IInkAnalyzer：： GetStrokeLanguageId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690579"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="6727e-103">IInkAnalyzer：： GetStrokeLanguageId 方法</span><span class="sxs-lookup"><span data-stu-id="6727e-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="6727e-104">傳回指定之筆劃的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6727e-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="6727e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6727e-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="6727e-106">參數</span><span class="sxs-lookup"><span data-stu-id="6727e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6727e-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6727e-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6727e-108">筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="6727e-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6727e-109">*lStrokeLCID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6727e-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6727e-110">指定之筆劃的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6727e-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6727e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6727e-111">Return value</span></span>

<span data-ttu-id="6727e-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6727e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6727e-113">備註</span><span class="sxs-lookup"><span data-stu-id="6727e-113">Remarks</span></span>

<span data-ttu-id="6727e-114">當您藉由呼叫 [**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)、 [**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)、 [**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)或 [**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)來加入筆劃時，會設定筆觸的地區設定。</span><span class="sxs-lookup"><span data-stu-id="6727e-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="6727e-115">若要變更筆觸的地區設定，請使用 [**IInkAnalyzer：： SetStrokeLanguageId 方法**](iinkanalyzer-setstrokelanguageid.md) 或 [**IInkAnalyzer：： SetStrokesLanguageId 方法**](iinkanalyzer-setstrokeslanguageid.md)。</span><span class="sxs-lookup"><span data-stu-id="6727e-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6727e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6727e-116">Requirements</span></span>



| <span data-ttu-id="6727e-117">需求</span><span class="sxs-lookup"><span data-stu-id="6727e-117">Requirement</span></span> | <span data-ttu-id="6727e-118">值</span><span class="sxs-lookup"><span data-stu-id="6727e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6727e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6727e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6727e-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6727e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6727e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6727e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6727e-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="6727e-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6727e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6727e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6727e-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6727e-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6727e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6727e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6727e-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6727e-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6727e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6727e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6727e-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6727e-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6727e-129">**IInkAnalyzer：： SetStrokeLanguageId 方法**</span><span class="sxs-lookup"><span data-stu-id="6727e-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="6727e-130">**IInkAnalyzer：： SetStrokesLanguageId 方法**</span><span class="sxs-lookup"><span data-stu-id="6727e-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="6727e-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="6727e-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




