---
description: 指定筆跡分析期間可能發生的可用警告集。
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: 'AnalysisWarningCode 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980910"
---
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="7ae63-103">AnalysisWarningCode 列舉</span><span class="sxs-lookup"><span data-stu-id="7ae63-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="7ae63-104">指定筆跡分析期間可能發生的可用警告集。</span><span class="sxs-lookup"><span data-stu-id="7ae63-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ae63-105">Syntax</span></span>


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a><span data-ttu-id="7ae63-106">常數</span><span class="sxs-lookup"><span data-stu-id="7ae63-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7ae63-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode 已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="7ae63-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-108">分析作業已中止。</span><span class="sxs-lookup"><span data-stu-id="7ae63-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="7ae63-109">只有在呼叫同步分析作業時才會傳回。</span><span class="sxs-lookup"><span data-stu-id="7ae63-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="7ae63-110">中止非同步作業並不會引發 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件。</span><span class="sxs-lookup"><span data-stu-id="7ae63-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**</span><span class="sxs-lookup"><span data-stu-id="7ae63-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-112">[**IInkAnalyzer**](iinkanalyzer.md)找不到符合執行分析作業所需之語言或功能需求的筆墨辨識器。</span><span class="sxs-lookup"><span data-stu-id="7ae63-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-114">筆墨辨識器無法遵循分析提示節點上指定的模擬程式集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-116">筆墨辨識器無法將其結果強制轉換為分析提示節點上指定的模擬程式集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-118">筆墨辨識器無法遵循分析提示節點上的指定指南集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-120">筆墨辨識器無法遵循分析提示節點上指定的單字清單集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-122">筆墨辨識器無法遵循在分析提示節點上設定的指定 word 模式 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-124">表示無法從 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)傳回部分字典詞彙。</span><span class="sxs-lookup"><span data-stu-id="7ae63-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**</span><span class="sxs-lookup"><span data-stu-id="7ae63-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-126">指出文字辨識進程失敗。</span><span class="sxs-lookup"><span data-stu-id="7ae63-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**</span><span class="sxs-lookup"><span data-stu-id="7ae63-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-128">無法將筆墨新增至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)。</span><span class="sxs-lookup"><span data-stu-id="7ae63-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="7ae63-129">例如，在筆勢辨識器上將從滑鼠收集的筆劃新增至會失敗，因為手勢辨識器需要從數位板收集的筆觸。</span><span class="sxs-lookup"><span data-stu-id="7ae63-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**</span><span class="sxs-lookup"><span data-stu-id="7ae63-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-131">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)無法遵守分析提示節點的指定前置詞或後置詞文字 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)和 [analysis 提示屬性](analysis-hint-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**</span><span class="sxs-lookup"><span data-stu-id="7ae63-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-133">[**IInkAnalyzer**](iinkanalyzer.md)無法在 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)上具現化、複製或設定筆觸。</span><span class="sxs-lookup"><span data-stu-id="7ae63-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**</span><span class="sxs-lookup"><span data-stu-id="7ae63-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-135">指出使用者已確認 [**ICoNtextNode**](icontextnode.md) 物件，但未針對該節點計算任何辨識值。</span><span class="sxs-lookup"><span data-stu-id="7ae63-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**</span><span class="sxs-lookup"><span data-stu-id="7ae63-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-137">背景作業未完成，因為發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7ae63-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="7ae63-138">這是嚴重的錯誤，需要重新具現化 [**IInkAnalyzer**](iinkanalyzer.md) ，然後再進一步使用。</span><span class="sxs-lookup"><span data-stu-id="7ae63-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ CoNtextNodeLocationNotSet**</span><span class="sxs-lookup"><span data-stu-id="7ae63-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-140">指出 [**ICoNtextNode**](icontextnode.md) 物件沒有適當的位置集 (請參閱 [**ICoNtextNode：： SetLocation**](icontextnode-setlocation.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7ae63-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="7ae63-141">除非 **ICoNtextNode** 物件標示為部分填入，否則 [**ICoNtextNode：： GetLocation**](icontextnode-getlocation.md)方法必須傳回非空白值。</span><span class="sxs-lookup"><span data-stu-id="7ae63-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**</span><span class="sxs-lookup"><span data-stu-id="7ae63-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-143">在與自訂辨識器節點相關聯的筆劃上設定的語言識別項 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 不符合所使用之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="7ae63-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="7ae63-144">具有指定 **IInkAnalysisRecognizer** 的筆墨仍能辨識。</span><span class="sxs-lookup"><span data-stu-id="7ae63-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-146">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援依照指定啟用 Unicode 字元範圍。</span><span class="sxs-lookup"><span data-stu-id="7ae63-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**</span><span class="sxs-lookup"><span data-stu-id="7ae63-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-148">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)只會支援 TopInkBreaks，即使提示只包含 TopInkBreaks 的要求也是一樣。</span><span class="sxs-lookup"><span data-stu-id="7ae63-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="7ae63-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**</span><span class="sxs-lookup"><span data-stu-id="7ae63-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="7ae63-150">[**IInkAnalyzer**](iinkanalyzer.md)已在執行背景分析。</span><span class="sxs-lookup"><span data-stu-id="7ae63-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ae63-151">備註</span><span class="sxs-lookup"><span data-stu-id="7ae63-151">Remarks</span></span>

<span data-ttu-id="7ae63-152">**AnalysisWarningCode \_BackgroundException** 是唯一需要先重新具現化 [**IInkAnalyzer**](iinkanalyzer.md) 物件，再進一步使用的警告程式碼值。</span><span class="sxs-lookup"><span data-stu-id="7ae63-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="7ae63-153">其他警告程式碼值（例如 **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** 和 **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**）可能需要 [**IInkAnalyzer**](iinkanalyzer.md) 物件使用不同的辨識器。</span><span class="sxs-lookup"><span data-stu-id="7ae63-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae63-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ae63-154">Requirements</span></span>



| <span data-ttu-id="7ae63-155">需求</span><span class="sxs-lookup"><span data-stu-id="7ae63-155">Requirement</span></span> | <span data-ttu-id="7ae63-156">值</span><span class="sxs-lookup"><span data-stu-id="7ae63-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae63-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ae63-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae63-158">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ae63-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7ae63-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ae63-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae63-160">都不支援</span><span class="sxs-lookup"><span data-stu-id="7ae63-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7ae63-161">標頭</span><span class="sxs-lookup"><span data-stu-id="7ae63-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ae63-162"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7ae63-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae63-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ae63-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae63-164">**IAnalysisWarning::GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="7ae63-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="7ae63-165">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7ae63-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




