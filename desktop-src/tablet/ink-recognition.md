---
description: 並非所有應用程式都需要使用辨識，但因為大部分的應用程式都是以文字作為其主要資料類型來設計，所以將筆墨轉換成文字的能力非常重要。
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: 筆跡辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550706"
---
# <a name="ink-recognition"></a><span data-ttu-id="2ba47-103">筆跡辨識</span><span class="sxs-lookup"><span data-stu-id="2ba47-103">Ink Recognition</span></span>

<span data-ttu-id="2ba47-104">並非所有應用程式都需要使用辨識，但因為大部分的應用程式都是以文字作為其主要資料類型來設計，所以將筆墨轉換成文字的能力非常重要。</span><span class="sxs-lookup"><span data-stu-id="2ba47-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="2ba47-105">您可以使用 Tablet PC 平臺 API 的辨識功能來查詢可用辨識引擎的相關資訊，例如它們所辨識的語言。</span><span class="sxs-lookup"><span data-stu-id="2ba47-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="2ba47-106">然後，您可以從 [**筆墨**](inkdisp-class.md)物件將 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合傳送到辨識引擎，並讓它傳回 [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件。</span><span class="sxs-lookup"><span data-stu-id="2ba47-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="2ba47-107">RecognizerCoNtext 物件</span><span class="sxs-lookup"><span data-stu-id="2ba47-107">RecognizerContext Object</span></span>

<span data-ttu-id="2ba47-108">[**RecognizerCoNtext**](inkrecognizercontext-class.md)物件是指定辨識器的具現化。</span><span class="sxs-lookup"><span data-stu-id="2ba47-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="2ba47-109">**RecognizerCoNtext** 物件可讓您以同步或非同步方式辨識指定的筆劃集合。</span><span class="sxs-lookup"><span data-stu-id="2ba47-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="2ba47-110">以非同步方式辨識時， **RecognizerCoNtext** 物件會將事件回呼中的 [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="2ba47-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="2ba47-111">辨識器和辨識器物件</span><span class="sxs-lookup"><span data-stu-id="2ba47-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="2ba47-112">單一 Tablet PC 可能會有一或多個辨識器可用。</span><span class="sxs-lookup"><span data-stu-id="2ba47-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="2ba47-113">您可以查詢辨識器的集合，以判斷要使用哪一個辨識器。</span><span class="sxs-lookup"><span data-stu-id="2ba47-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="2ba47-114">辨識器提供有關其功能的特定資訊，例如可辨識的語言和製造商。</span><span class="sxs-lookup"><span data-stu-id="2ba47-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="2ba47-115">若要判斷是否至少安裝了一個辨識器，請將 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件具現化，如下列 c + + 和 c 程式 \# 代碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="2ba47-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="2ba47-116">如果找不到辨識器，則這個對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="2ba47-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="2ba47-117">RecognitionResult 和 RecognitionAlternate 物件</span><span class="sxs-lookup"><span data-stu-id="2ba47-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="2ba47-118">辨識的結果會在 [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件中傳回。</span><span class="sxs-lookup"><span data-stu-id="2ba47-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="2ba47-119">結果包含 [TopString](/previous-versions/ms829602(v=msdn.10)) 屬性中的最佳結果字串，以及 [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) 集合中替代結果的集合。</span><span class="sxs-lookup"><span data-stu-id="2ba47-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="2ba47-120">**RecognitionResult** 物件可以使用產生它的原始 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合來保存。</span><span class="sxs-lookup"><span data-stu-id="2ba47-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="2ba47-121">RecognizerGuide 結構</span><span class="sxs-lookup"><span data-stu-id="2ba47-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="2ba47-122">辨識器指南可以包含資料列和資料行，並為辨識器提供較佳的內容以執行辨識。</span><span class="sxs-lookup"><span data-stu-id="2ba47-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="2ba47-123">例如，您可以在使用者畫面上繪製水平線，就像是一段紙紙，顯示手寫的出現位置 (這種類型的指南只會包含資料列，而且沒有任何資料行) 。</span><span class="sxs-lookup"><span data-stu-id="2ba47-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="2ba47-124">如果使用者在行上進行寫入，而不是使用某些任意空間，則辨識精確度會有所改善。</span><span class="sxs-lookup"><span data-stu-id="2ba47-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="2ba47-125">下圖顯示具有兩行輸入的 [**RecognizerGuide**](inkrecognizerguide-class.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2ba47-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![顯示兩行辨識器指南的圖例](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="2ba47-127">下圖顯示具有四個數據行和三個數據列的 [**RecognizerGuide**](inkrecognizerguide-class.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2ba47-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![顯示三四個辨識器指南的圖例](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="2ba47-129">如需有關使用 [**RecognizerGuide**](inkrecognizerguide-class.md) 結構的詳細資訊，請參閱 **RecognizerGuide** 參考主題。</span><span class="sxs-lookup"><span data-stu-id="2ba47-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
