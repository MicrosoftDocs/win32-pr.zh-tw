---
description: 啟用執行筆跡辨識、取出辨識結果，以及取得替代項的能力。 InkRecognizerCoNtext 可讓安裝在系統上的各種辨識器使用筆墨辨識來適當地處理輸入。
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: 'InkRecognizerCoNtext 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: afe5469cabf6764ed9b02fdcffcc8c1bedaca1d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193155"
---
# <a name="inkrecognizercontext-class"></a><span data-ttu-id="6f161-104">InkRecognizerCoNtext 類別</span><span class="sxs-lookup"><span data-stu-id="6f161-104">InkRecognizerContext class</span></span>

<span data-ttu-id="6f161-105">啟用執行筆跡辨識、取出辨識結果，以及取得替代項的能力。</span><span class="sxs-lookup"><span data-stu-id="6f161-105">Enables the ability to perform ink recognition, retrieve the recognition result, and retrieve alternates.</span></span> <span data-ttu-id="6f161-106">**InkRecognizerCoNtext** 可讓安裝在系統上的各種辨識器使用筆墨辨識來適當地處理輸入。</span><span class="sxs-lookup"><span data-stu-id="6f161-106">The **InkRecognizerContext** enables the various recognizer that are installed on a system to use ink recognition to process input appropriately.</span></span>

<span data-ttu-id="6f161-107">**InkRecognizerCoNtext** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f161-107">**InkRecognizerContext** has these types of members:</span></span>

-   [<span data-ttu-id="6f161-108">事件</span><span class="sxs-lookup"><span data-stu-id="6f161-108">Events</span></span>](#events)
-   [<span data-ttu-id="6f161-109">介面</span><span class="sxs-lookup"><span data-stu-id="6f161-109">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="6f161-110">方法</span><span class="sxs-lookup"><span data-stu-id="6f161-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f161-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6f161-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="6f161-112">事件</span><span class="sxs-lookup"><span data-stu-id="6f161-112">Events</span></span>

<span data-ttu-id="6f161-113">**InkRecognizerCoNtext** 類別具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="6f161-113">The **InkRecognizerContext** class has these events.</span></span>



| <span data-ttu-id="6f161-114">事件</span><span class="sxs-lookup"><span data-stu-id="6f161-114">Event</span></span>                                                                               | <span data-ttu-id="6f161-115">描述</span><span class="sxs-lookup"><span data-stu-id="6f161-115">Description</span></span>                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f161-116">**辨識**</span><span class="sxs-lookup"><span data-stu-id="6f161-116">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="6f161-117">當 InkRecognizerCoNtext 從 BackgroundRecognize 方法產生結果時發生。</span><span class="sxs-lookup"><span data-stu-id="6f161-117">Occurs when the InkRecognizerContext has generated results from the BackgroundRecognize method.</span></span><br/>                                                                                             |
| [<span data-ttu-id="6f161-118">**RecognitionWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="6f161-118">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="6f161-119">**InkRecognizerCoNtext** 在呼叫 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法之後產生結果時發生</span><span class="sxs-lookup"><span data-stu-id="6f161-119">Occurs when the **InkRecognizerContext** has generated results after calling the [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="6f161-120">介面</span><span class="sxs-lookup"><span data-stu-id="6f161-120">Interfaces</span></span>

<span data-ttu-id="6f161-121">**InkRecognizerCoNtext** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="6f161-121">The **InkRecognizerContext** class defines these interfaces.</span></span>



| <span data-ttu-id="6f161-122">介面</span><span class="sxs-lookup"><span data-stu-id="6f161-122">Interface</span></span>                 | <span data-ttu-id="6f161-123">描述</span><span class="sxs-lookup"><span data-stu-id="6f161-123">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="6f161-124">**IInkRecognizerCoNtext**</span><span class="sxs-lookup"><span data-stu-id="6f161-124">**IInkRecognizerContext**</span></span> | <span data-ttu-id="6f161-125">這個物件會實 **IInkRecognizerCoNtext** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="6f161-125">This object implements the **IInkRecognizerContext** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="6f161-126">方法</span><span class="sxs-lookup"><span data-stu-id="6f161-126">Methods</span></span>

<span data-ttu-id="6f161-127">**InkRecognizerCoNtext** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6f161-127">The **InkRecognizerContext** class has these methods.</span></span>



| <span data-ttu-id="6f161-128">方法</span><span class="sxs-lookup"><span data-stu-id="6f161-128">Method</span></span>                                                                                              | <span data-ttu-id="6f161-129">描述</span><span class="sxs-lookup"><span data-stu-id="6f161-129">Description</span></span>                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f161-130">**BackgroundRecognize**</span><span class="sxs-lookup"><span data-stu-id="6f161-130">**BackgroundRecognize**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | <span data-ttu-id="6f161-131">指定辨識器應該在辨識完成時，辨識相關聯 [**的筆劃**](inkrecognizercontext-recognition.md) 並引發辨識事件。</span><span class="sxs-lookup"><span data-stu-id="6f161-131">Specifies that the recognizer should recognize the associated strokes and fire a [**Recognition**](inkrecognizercontext-recognition.md) event when recognition is complete.</span></span><br/>                                                                |
| [<span data-ttu-id="6f161-132">**BackgroundRecognizeWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="6f161-132">**BackgroundRecognizeWithAlternates**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | <span data-ttu-id="6f161-133">指定辨識器應該在辨識完成時，辨識相關聯的筆劃並引發 [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6f161-133">Specifies that the recognizer should recognize the associated strokes and fire a [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event when recognition is complete.</span></span><br/>                                    |
| [<span data-ttu-id="6f161-134">**克隆**</span><span class="sxs-lookup"><span data-stu-id="6f161-134">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | <span data-ttu-id="6f161-135">建立重複的 **InkRecognizerCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="6f161-135">Creates a duplicate **InkRecognizerContext**.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="6f161-136">**EndInkInput**</span><span class="sxs-lookup"><span data-stu-id="6f161-136">**EndInkInput**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | <span data-ttu-id="6f161-137">結束筆墨輸入至 **InkRecognizerCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="6f161-137">Ends ink input to the **InkRecognizerContext**.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="6f161-138">**IsStringSupported**</span><span class="sxs-lookup"><span data-stu-id="6f161-138">**IsStringSupported**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | <span data-ttu-id="6f161-139">指出系統字典、使用者字典或 [**單字清單**](inkwordlist-class.md) 是否包含指定的字串。</span><span class="sxs-lookup"><span data-stu-id="6f161-139">Indicates whether the system dictionary, user dictionary, or [**word list**](inkwordlist-class.md) contain a specified string.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="6f161-140">**Recognize**</span><span class="sxs-lookup"><span data-stu-id="6f161-140">**Recognize**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | <span data-ttu-id="6f161-141">在 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合上執行辨識，並傳回辨識結果。</span><span class="sxs-lookup"><span data-stu-id="6f161-141">Performs recognition on an [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and returns recognition results.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="6f161-142">**StopBackgroundRecognition**</span><span class="sxs-lookup"><span data-stu-id="6f161-142">**StopBackgroundRecognition**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | <span data-ttu-id="6f161-143">結束對 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) 或 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)的呼叫所開始的背景識別。</span><span class="sxs-lookup"><span data-stu-id="6f161-143">Ends background recognition that was started with a call to [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) or [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6f161-144">屬性</span><span class="sxs-lookup"><span data-stu-id="6f161-144">Properties</span></span>

<span data-ttu-id="6f161-145">**InkRecognizerCoNtext** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6f161-145">The **InkRecognizerContext** class has these properties.</span></span>



| <span data-ttu-id="6f161-146">屬性</span><span class="sxs-lookup"><span data-stu-id="6f161-146">Property</span></span>                                                                                   | <span data-ttu-id="6f161-147">存取類型</span><span class="sxs-lookup"><span data-stu-id="6f161-147">Access type</span></span>           | <span data-ttu-id="6f161-148">Description</span><span class="sxs-lookup"><span data-stu-id="6f161-148">Description</span></span>                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f161-149">**CharacterAutoCompletion**</span><span class="sxs-lookup"><span data-stu-id="6f161-149">**CharacterAutoCompletion**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | <span data-ttu-id="6f161-150">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-150">Read/write</span></span><br/> | <span data-ttu-id="6f161-151">取得或設定字元自動完成模式，這個模式會決定何時辨識字元或文字。</span><span class="sxs-lookup"><span data-stu-id="6f161-151">Gets or sets the character Autocomplete mode, which determines when characters or words are recognized.</span></span><br/>                                         |
| [<span data-ttu-id="6f161-152">**標記**</span><span class="sxs-lookup"><span data-stu-id="6f161-152">**Factoid**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | <span data-ttu-id="6f161-153">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-153">Read/write</span></span><br/> | <span data-ttu-id="6f161-154">取得或設定 **InkRecognizerCoNtext** 物件所使用之模擬的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="6f161-154">Gets or sets the string name of the factoid used by the **InkRecognizerContext** object.</span></span><br/>                                                        |
| [<span data-ttu-id="6f161-155">**指南**</span><span class="sxs-lookup"><span data-stu-id="6f161-155">**Guide**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | <span data-ttu-id="6f161-156">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-156">Read/write</span></span><br/> | <span data-ttu-id="6f161-157">取得或設定要用於筆墨輸入的 [**InkRecognizerGuide**](inkrecognizerguide-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="6f161-157">Gets or sets the [**InkRecognizerGuide**](inkrecognizerguide-class.md) to use for ink input.</span></span><br/>                                                   |
| [<span data-ttu-id="6f161-158">**PrefixText**</span><span class="sxs-lookup"><span data-stu-id="6f161-158">**PrefixText**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | <span data-ttu-id="6f161-159">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-159">Read/write</span></span><br/> | <span data-ttu-id="6f161-160">取得或設定 **InkRecognizerCoNtext** 物件中 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合之前的字元。</span><span class="sxs-lookup"><span data-stu-id="6f161-160">Gets or sets the characters that come before the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection in the **InkRecognizerContext** object.</span></span><br/> |
| [<span data-ttu-id="6f161-161">**RecognitionFlags**</span><span class="sxs-lookup"><span data-stu-id="6f161-161">**RecognitionFlags**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | <span data-ttu-id="6f161-162">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-162">Read/write</span></span><br/> | <span data-ttu-id="6f161-163">取得或設定旗標，指定辨識器如何解讀筆墨並決定結果字串。</span><span class="sxs-lookup"><span data-stu-id="6f161-163">Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string.</span></span><br/>                                     |
| [<span data-ttu-id="6f161-164">**辨識器**</span><span class="sxs-lookup"><span data-stu-id="6f161-164">**Recognizer**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | <span data-ttu-id="6f161-165">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-165">Read/write</span></span><br/> | <span data-ttu-id="6f161-166">取得或設定 **InkRecognizerCoNtext** 物件所使用的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件。</span><span class="sxs-lookup"><span data-stu-id="6f161-166">Gets or sets the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object used by the **InkRecognizerContext** object.</span></span><br/>                                   |
| [<span data-ttu-id="6f161-167">**中風**</span><span class="sxs-lookup"><span data-stu-id="6f161-167">**Strokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | <span data-ttu-id="6f161-168">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-168">Read/write</span></span><br/> | <span data-ttu-id="6f161-169">取得或設定與 **InkRecognizerCoNtext** 物件相關聯的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。</span><span class="sxs-lookup"><span data-stu-id="6f161-169">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection associated with the **InkRecognizerContext** object.</span></span><br/>                    |
| [<span data-ttu-id="6f161-170">**SuffixText**</span><span class="sxs-lookup"><span data-stu-id="6f161-170">**SuffixText**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | <span data-ttu-id="6f161-171">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-171">Read/write</span></span><br/> | <span data-ttu-id="6f161-172">取得或設定在 **InkRecognizerCoNtext** 物件中 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合之後的字元。</span><span class="sxs-lookup"><span data-stu-id="6f161-172">Gets or sets the characters that come after the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection in the **InkRecognizerContext** object.</span></span><br/>  |
| [<span data-ttu-id="6f161-173">**單詞表**</span><span class="sxs-lookup"><span data-stu-id="6f161-173">**WordList**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | <span data-ttu-id="6f161-174">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f161-174">Read/write</span></span><br/> | <span data-ttu-id="6f161-175">取得或設定用來改善辨識結果的 [**InkWordList**](inkwordlist-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6f161-175">Gets or sets the [**InkWordList**](inkwordlist-class.md) object that is used to improve the recognition results.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="6f161-176">備註</span><span class="sxs-lookup"><span data-stu-id="6f161-176">Remarks</span></span>

<span data-ttu-id="6f161-177">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="6f161-177">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="6f161-178">有兩種類型的辨識：背景 (非同步) 或前景 (同步) 。</span><span class="sxs-lookup"><span data-stu-id="6f161-178">There are two types of recognition: background (asynchronous) or foreground (synchronous).</span></span> <span data-ttu-id="6f161-179">背景辨識是透過呼叫 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) 或 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) 方法來啟動，在背景執行緒上發生，並透過事件機制將結果回報給應用程式。</span><span class="sxs-lookup"><span data-stu-id="6f161-179">Background recognition is started by a call to the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) or [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) methods, occurs on a background thread, and reports results to the application through an event mechanism.</span></span> <span data-ttu-id="6f161-180">在所有辨識完成之前都不會傳回前景辨識，因此可在呼叫執行緒中使用辨識結果，而不需接聽辨識事件。</span><span class="sxs-lookup"><span data-stu-id="6f161-180">Foreground recognition does not return until all recognition is completed, thus making recognition results available to the calling thread without listening for the recognition event.</span></span>

<span data-ttu-id="6f161-181">筆墨會在背景中持續處理。</span><span class="sxs-lookup"><span data-stu-id="6f161-181">Ink is processed continuously in the background.</span></span> <span data-ttu-id="6f161-182">如果將 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)新增至 **InkRecognizerCoNtext** 所參考的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合，則會立即辨識該 **IInkStrokeDisp** 。</span><span class="sxs-lookup"><span data-stu-id="6f161-182">If an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to which the **InkRecognizerContext** refers, then the **IInkStrokeDisp** is then recognized immediately.</span></span> <span data-ttu-id="6f161-183">如需詳細資訊，請參閱 [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) 方法主題中的備註。</span><span class="sxs-lookup"><span data-stu-id="6f161-183">See remarks in the [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) method topic for more details.</span></span>

<span data-ttu-id="6f161-184">所有辨識都會透過辨識器內容進行。</span><span class="sxs-lookup"><span data-stu-id="6f161-184">All recognition occurs through a recognizer context.</span></span> <span data-ttu-id="6f161-185">內容會定義單一識別會話的設定。</span><span class="sxs-lookup"><span data-stu-id="6f161-185">The context defines the settings for a single recognition session.</span></span> <span data-ttu-id="6f161-186">它會接收必須辨識的筆墨，並且在筆跡輸入和辨識輸出上定義條件約束。</span><span class="sxs-lookup"><span data-stu-id="6f161-186">It receives the ink that must be recognized and defines the constraints on the ink input and on the recognition output.</span></span> <span data-ttu-id="6f161-187">可以在內容上設定的條件約束，包括所使用的語言、字典和文法。</span><span class="sxs-lookup"><span data-stu-id="6f161-187">The constraints that can be set on the context include the language, the dictionary, and grammar that is being used.</span></span>

> [!Note]  
> <span data-ttu-id="6f161-188">只有當 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合是 **Null** 時，才會成功設定 [**筆劃**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)或 [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)屬性以外的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f161-188">Setting properties other than the [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) or [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) properties succeeds only if the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is **NULL**.</span></span> <span data-ttu-id="6f161-189">您必須先設定其他屬性，才能將 InkStrokes 集合附加至 **InkRecognizerCoNtext**，或必須將 InkStrokes 集合設定為 **Null** ，然後再設定其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6f161-189">You must set the other properties before you attach the InkStrokes collection to the **InkRecognizerContext**, or you must set the InkStrokes collection to **NULL** and then set the other properties.</span></span> <span data-ttu-id="6f161-190">如果您將 InkStrokes 集合設為 **Null** ，然後再設定其他屬性，您可能必須重新附加 InkStrokes 集合。</span><span class="sxs-lookup"><span data-stu-id="6f161-190">If you set the InkStrokes collection to **NULL** and then set the other properties, you may have to reattach the InkStrokes collection.</span></span> <span data-ttu-id="6f161-191">這是因為當您將 InkStrokes 指派給 **InkRecognizerCoNtext** 之後，就會開始進行辨識。</span><span class="sxs-lookup"><span data-stu-id="6f161-191">This is because the recognition starts right after you assign the InkStrokes to the **InkRecognizerContext**.</span></span> <span data-ttu-id="6f161-192">進行呼叫以 [**辨識方法 \[ InkRecognizeCoNtext 類別 \]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)或 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)時，可能已經有呼叫結果可供使用。</span><span class="sxs-lookup"><span data-stu-id="6f161-192">When a call is made to [**Recognize Method \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) or [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize), call results might be available already.</span></span>

 

<span data-ttu-id="6f161-193">若要改善應用程式的效能，請在不再需要時處置您的 **InkRecognizerCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f161-193">To improve your application's performance, dispose of your **InkRecognizerContext** object when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f161-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f161-194">Requirements</span></span>



| <span data-ttu-id="6f161-195">需求</span><span class="sxs-lookup"><span data-stu-id="6f161-195">Requirement</span></span> | <span data-ttu-id="6f161-196">值</span><span class="sxs-lookup"><span data-stu-id="6f161-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f161-197">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f161-197">Minimum supported client</span></span><br/> | <span data-ttu-id="6f161-198">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f161-198">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6f161-199">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f161-199">Minimum supported server</span></span><br/> | <span data-ttu-id="6f161-200">都不支援</span><span class="sxs-lookup"><span data-stu-id="6f161-200">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6f161-201">標頭</span><span class="sxs-lookup"><span data-stu-id="6f161-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f161-202"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6f161-202"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f161-203">程式庫</span><span class="sxs-lookup"><span data-stu-id="6f161-203">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f161-204"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f161-204"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6f161-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f161-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f161-206">**IInkRecognizer 介面**</span><span class="sxs-lookup"><span data-stu-id="6f161-206">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

<span data-ttu-id="6f161-207">[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f161-207">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

