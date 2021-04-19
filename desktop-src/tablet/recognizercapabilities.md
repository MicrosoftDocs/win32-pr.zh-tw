---
description: 指定 IInkAnalysisRecognizer 的屬性。
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: 'RecognizerCapabilities 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971854"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="859e1-103">RecognizerCapabilities 列舉</span><span class="sxs-lookup"><span data-stu-id="859e1-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="859e1-104">指定 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的屬性。</span><span class="sxs-lookup"><span data-stu-id="859e1-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="859e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="859e1-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="859e1-106">常數</span><span class="sxs-lookup"><span data-stu-id="859e1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="859e1-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ 無**</span><span class="sxs-lookup"><span data-stu-id="859e1-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-108">未指定任何功能。</span><span class="sxs-lookup"><span data-stu-id="859e1-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**</span><span class="sxs-lookup"><span data-stu-id="859e1-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-110">忽略所有其他已設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="859e1-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="859e1-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-112">支持對象識別;否則，只會辨識文字。</span><span class="sxs-lookup"><span data-stu-id="859e1-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**</span><span class="sxs-lookup"><span data-stu-id="859e1-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-114">支援自由輸入，其中輸入筆墨時，不需使用辨識指南，例如線條或方塊。</span><span class="sxs-lookup"><span data-stu-id="859e1-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**</span><span class="sxs-lookup"><span data-stu-id="859e1-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-116">支援線條輸入，這類似于書寫線條紙。</span><span class="sxs-lookup"><span data-stu-id="859e1-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**</span><span class="sxs-lookup"><span data-stu-id="859e1-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-118">支援在方塊中輸入每個字元或單字的已框輸入。</span><span class="sxs-lookup"><span data-stu-id="859e1-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**</span><span class="sxs-lookup"><span data-stu-id="859e1-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-120">支援字元自動完成。</span><span class="sxs-lookup"><span data-stu-id="859e1-120">Supports character Autocomplete.</span></span> <span data-ttu-id="859e1-121">支援字元自動完成的辨識器需要有已裝箱的輸入。</span><span class="sxs-lookup"><span data-stu-id="859e1-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**</span><span class="sxs-lookup"><span data-stu-id="859e1-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-123">支援向右和向下訂購的手寫輸入，例如西方語言和某些東亞語言。</span><span class="sxs-lookup"><span data-stu-id="859e1-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**</span><span class="sxs-lookup"><span data-stu-id="859e1-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-125">支援以左方和向下順序書寫輸入，例如在希伯來文和阿拉伯文語言中。</span><span class="sxs-lookup"><span data-stu-id="859e1-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**</span><span class="sxs-lookup"><span data-stu-id="859e1-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-127">支援以向下和向下順序書寫輸入，例如在某些東亞語言中。</span><span class="sxs-lookup"><span data-stu-id="859e1-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**</span><span class="sxs-lookup"><span data-stu-id="859e1-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-129">支援以向下和向右書寫的手寫輸入，例如在某些東亞語言中。</span><span class="sxs-lookup"><span data-stu-id="859e1-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**</span><span class="sxs-lookup"><span data-stu-id="859e1-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-131">支援以任意角度書寫的文字。</span><span class="sxs-lookup"><span data-stu-id="859e1-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ >lattice**</span><span class="sxs-lookup"><span data-stu-id="859e1-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-133">支援傳回 >lattice 做為手寫辨識結果的替代字串。</span><span class="sxs-lookup"><span data-stu-id="859e1-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**</span><span class="sxs-lookup"><span data-stu-id="859e1-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-135">支援中斷背景識別，例如當筆墨變更時。</span><span class="sxs-lookup"><span data-stu-id="859e1-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**</span><span class="sxs-lookup"><span data-stu-id="859e1-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-137">支援將筆劃順序（空間和時態性）視為辨識作業的一部分來處理。</span><span class="sxs-lookup"><span data-stu-id="859e1-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="859e1-138">在將筆墨傳送至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)之前， [**IInkAnalyzer**](iinkanalyzer.md)不會重新排列筆劃的順序。</span><span class="sxs-lookup"><span data-stu-id="859e1-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="859e1-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC 可 \_ 個人化**</span><span class="sxs-lookup"><span data-stu-id="859e1-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-140">支援個人化手寫，辨識器會在一段時間內公開給相同的手寫時，改善辨識。</span><span class="sxs-lookup"><span data-stu-id="859e1-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**</span><span class="sxs-lookup"><span data-stu-id="859e1-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-142">在將筆墨傳送至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)之前， [**IInkAnalyzer**](iinkanalyzer.md)不需要將手寫旋轉為水準方向。</span><span class="sxs-lookup"><span data-stu-id="859e1-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="859e1-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**</span><span class="sxs-lookup"><span data-stu-id="859e1-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-144">[**IInkAnalyzer**](iinkanalyzer.md)應該將筆跡的整個段落傳送至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)，讓 **IInkAnalysisRecognizer** 能夠進行斷詞和單字 (或字元) 中斷。</span><span class="sxs-lookup"><span data-stu-id="859e1-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="859e1-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**</span><span class="sxs-lookup"><span data-stu-id="859e1-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="859e1-146">每次辨識作業只能辨識一個單字或字元。</span><span class="sxs-lookup"><span data-stu-id="859e1-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="859e1-147">[**IInkAnalyzer**](iinkanalyzer.md)會對手寫執行分割，並且一次只傳送一個區段給 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)。</span><span class="sxs-lookup"><span data-stu-id="859e1-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="859e1-148">備註</span><span class="sxs-lookup"><span data-stu-id="859e1-148">Remarks</span></span>

<span data-ttu-id="859e1-149">此列舉允許其成員值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="859e1-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="859e1-150">使用這個列舉來尋找已安裝的筆跡辨識器，以支援您需要的屬性。</span><span class="sxs-lookup"><span data-stu-id="859e1-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="859e1-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="859e1-151">Requirements</span></span>



| <span data-ttu-id="859e1-152">需求</span><span class="sxs-lookup"><span data-stu-id="859e1-152">Requirement</span></span> | <span data-ttu-id="859e1-153">值</span><span class="sxs-lookup"><span data-stu-id="859e1-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859e1-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="859e1-154">Minimum supported client</span></span><br/> | <span data-ttu-id="859e1-155">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="859e1-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="859e1-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="859e1-156">Minimum supported server</span></span><br/> | <span data-ttu-id="859e1-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="859e1-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="859e1-158">標頭</span><span class="sxs-lookup"><span data-stu-id="859e1-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="859e1-159"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="859e1-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="859e1-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="859e1-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="859e1-161">**IInkAnalysisRecognizer::GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="859e1-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="859e1-162">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="859e1-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




