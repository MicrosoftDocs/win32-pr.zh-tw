---
description: 提供手寫辨識器的存取權，以搭配筆墨分析使用。
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: 'IInkAnalysisRecognizer 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967146"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="1d2d3-103">IInkAnalysisRecognizer 介面</span><span class="sxs-lookup"><span data-stu-id="1d2d3-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="1d2d3-104">提供手寫辨識器的存取權，以搭配筆墨分析使用。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="1d2d3-105">成員</span><span class="sxs-lookup"><span data-stu-id="1d2d3-105">Members</span></span>

<span data-ttu-id="1d2d3-106">**IInkAnalysisRecognizer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1d2d3-107">**IInkAnalysisRecognizer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1d2d3-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="1d2d3-108">方法</span><span class="sxs-lookup"><span data-stu-id="1d2d3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1d2d3-109">方法</span><span class="sxs-lookup"><span data-stu-id="1d2d3-109">Methods</span></span>

<span data-ttu-id="1d2d3-110">**IInkAnalysisRecognizer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="1d2d3-111">方法</span><span class="sxs-lookup"><span data-stu-id="1d2d3-111">Method</span></span>                                                                          | <span data-ttu-id="1d2d3-112">描述</span><span class="sxs-lookup"><span data-stu-id="1d2d3-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d2d3-113">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="1d2d3-114">抓取辨識器的功能。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="1d2d3-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="1d2d3-116">抓取辨識器 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="1d2d3-117">**GetLanguages**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="1d2d3-118">抓取此 **IInkAnalysisRecognizer** 支援之地區設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="1d2d3-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="1d2d3-120">抓取辨識器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="1d2d3-121">**GetSupportedProperties**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="1d2d3-122">針對此 **IInkAnalysisRecognizer** 所支援的屬性，抓取 (guid) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="1d2d3-123">**GetVendor**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="1d2d3-124">抓取 **IInkAnalysisRecognizer** 的廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="1d2d3-125">備註</span><span class="sxs-lookup"><span data-stu-id="1d2d3-125">Remarks</span></span>

<span data-ttu-id="1d2d3-126">辨識器具有特定的屬性和屬性，可讓它執行辨識。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="1d2d3-127">辨識器的屬性必須先經過判斷，才能進行辨識。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="1d2d3-128">辨識器支援的屬性類型，會決定它可以執行的辨識類型。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="1d2d3-129">比方說，如果辨識器不支援草書手寫，當使用者以草書寫入時，就會傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="1d2d3-130">辨識器也有內建的功能，可自動管理手寫的許多層面。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="1d2d3-131">例如，它會判斷繪製筆劃之線條的度量。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="1d2d3-132">您可以傳回筆劃的行號，但由於辨識器的內建功能，您永遠不需要指定這些線條度量的判斷方式。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="1d2d3-133">[**IInkAnalyzer**](iinkanalyzer.md)會維護可用辨識器的清單。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="1d2d3-134">若要存取此清單，請使用 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1d2d3-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2d3-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d2d3-135">Requirements</span></span>



| <span data-ttu-id="1d2d3-136">需求</span><span class="sxs-lookup"><span data-stu-id="1d2d3-136">Requirement</span></span> | <span data-ttu-id="1d2d3-137">值</span><span class="sxs-lookup"><span data-stu-id="1d2d3-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2d3-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d2d3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2d3-139">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d2d3-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d2d3-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d2d3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2d3-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="1d2d3-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1d2d3-142">標頭</span><span class="sxs-lookup"><span data-stu-id="1d2d3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2d3-143"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1d2d3-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1d2d3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2d3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2d3-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2d3-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1d2d3-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d2d3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2d3-147">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="1d2d3-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1d2d3-149">**IInkAnalyzer：： CreateCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="1d2d3-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="1d2d3-150">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="1d2d3-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="1d2d3-151">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="1d2d3-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

