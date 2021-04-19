---
description: 此範例示範 MicrosoftTablet PC Automation 應用程式開發介面的 advanced 功能 (API) 用於手寫辨識。
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: 多個辨識器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999917"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="0b67f-103">多個辨識器範例</span><span class="sxs-lookup"><span data-stu-id="0b67f-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="0b67f-104">此範例示範 MicrosoftTablet PC Automation 應用程式開發介面的 advanced 功能 (API) 用於 *手寫* 識別。</span><span class="sxs-lookup"><span data-stu-id="0b67f-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="0b67f-105">其中包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="0b67f-105">It includes the following:</span></span>

-   <span data-ttu-id="0b67f-106">列舉已安裝的辨識器</span><span class="sxs-lookup"><span data-stu-id="0b67f-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="0b67f-107">使用特定語言辨識器建立辨識 *器內容*</span><span class="sxs-lookup"><span data-stu-id="0b67f-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="0b67f-108">使用筆劃集合序列化辨識結果</span><span class="sxs-lookup"><span data-stu-id="0b67f-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="0b67f-109">將筆劃集合組織成 [**InkDisp**](inkdisp-class.md) 物件內的自訂集合</span><span class="sxs-lookup"><span data-stu-id="0b67f-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="0b67f-110">將 *筆墨* 物件 *序列化為 (ISF) 檔案的筆墨序列化格式* ，並加以抓取</span><span class="sxs-lookup"><span data-stu-id="0b67f-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="0b67f-111">設定辨識器輸入指南</span><span class="sxs-lookup"><span data-stu-id="0b67f-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="0b67f-112">使用同步和非同步識別</span><span class="sxs-lookup"><span data-stu-id="0b67f-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="0b67f-113">筆跡標頭</span><span class="sxs-lookup"><span data-stu-id="0b67f-113">Ink Headers</span></span>

<span data-ttu-id="0b67f-114">首先，請加入 Tablet PC 自動化介面的標頭。</span><span class="sxs-lookup"><span data-stu-id="0b67f-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="0b67f-115">這些會隨 Microsoft Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 一起安裝。</span><span class="sxs-lookup"><span data-stu-id="0b67f-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="0b67f-116">EventSinks .h 檔案會定義 IInkEventsImpl 和 IInkRecognitionEventsImpl 介面。</span><span class="sxs-lookup"><span data-stu-id="0b67f-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="0b67f-117">列舉已安裝的辨識器</span><span class="sxs-lookup"><span data-stu-id="0b67f-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="0b67f-118">應用程式的 LoadMenu 方法會在 [建立新的筆觸] 功能表中填入可用的辨識器。</span><span class="sxs-lookup"><span data-stu-id="0b67f-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="0b67f-119">系統會建立 [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="0b67f-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="0b67f-120">如果 **InkRecognizers** 物件的 [[**語言**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages)] 屬性不是空的，則辨識器會是 *文字辨識器*，並將其 [[**名稱**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name)] 屬性的值加入功能表中。</span><span class="sxs-lookup"><span data-stu-id="0b67f-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a><span data-ttu-id="0b67f-121">建立筆墨收集器</span><span class="sxs-lookup"><span data-stu-id="0b67f-121">Creating an Ink Collector</span></span>

<span data-ttu-id="0b67f-122">應用程式的 >oncreate 方法會建立 [**InkCollector**](inkcollector-class.md) 物件、將它連接至其事件來源，以及啟用筆墨收集。</span><span class="sxs-lookup"><span data-stu-id="0b67f-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="0b67f-123">建立辨識器內容</span><span class="sxs-lookup"><span data-stu-id="0b67f-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="0b67f-124">應用程式的 CreateRecoCoNtext 方法會建立並初始化新的辨識器內容，並設定相關聯語言所支援的指南。</span><span class="sxs-lookup"><span data-stu-id="0b67f-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="0b67f-125">[**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件的 [**CreateRecognizerCoNtext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext)方法會建立語言的 [**IInkRecognizerCoNtext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2)物件。</span><span class="sxs-lookup"><span data-stu-id="0b67f-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="0b67f-126">必要時，會取代舊的辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="0b67f-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="0b67f-127">內容會連接到其事件來源。</span><span class="sxs-lookup"><span data-stu-id="0b67f-127">The context is connected to its event source.</span></span> <span data-ttu-id="0b67f-128">最後，會針對辨識器內容所支援的輔助線，檢查辨識器內容的 [ [**功能**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="0b67f-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="0b67f-129">收集筆劃並顯示辨識結果</span><span class="sxs-lookup"><span data-stu-id="0b67f-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="0b67f-130">應用程式的 OnStroke 方法會更新筆墨收集器的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 、取消現有的非同步識別要求，並在辨識器內容上建立辨識要求。</span><span class="sxs-lookup"><span data-stu-id="0b67f-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



<span data-ttu-id="0b67f-131">應用程式的 `OnRecognition` 方法會將識別要求的結果傳送至輸出視窗的 `UpdateString` 方法。</span><span class="sxs-lookup"><span data-stu-id="0b67f-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="0b67f-132">刪除筆劃和辨識結果</span><span class="sxs-lookup"><span data-stu-id="0b67f-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="0b67f-133">應用程式的 OnClear 方法會刪除 [**InkDisp**](inkdisp-class.md) 物件中的所有筆劃和辨識結果，並清除視窗。</span><span class="sxs-lookup"><span data-stu-id="0b67f-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="0b67f-134">已移除辨識器內容與其 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的關聯。</span><span class="sxs-lookup"><span data-stu-id="0b67f-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="0b67f-135">變更辨識器內容</span><span class="sxs-lookup"><span data-stu-id="0b67f-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="0b67f-136">當使用者在 [建立新的筆觸] 功能表中選取辨識器時，會呼叫應用程式的 OnNewStrokes 方法。</span><span class="sxs-lookup"><span data-stu-id="0b67f-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="0b67f-137">儲存目前的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="0b67f-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="0b67f-138">如果選取不同的語言辨識器，則會建立新的辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="0b67f-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="0b67f-139">然後，新的 **InkStrokes** 會附加至新的辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="0b67f-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



<span data-ttu-id="0b67f-140">然後，它會呼叫 StartNewStrokeCollection，它會建立空的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ，並將它附加至辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="0b67f-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="0b67f-141">儲存辨識器內容的筆劃集合</span><span class="sxs-lookup"><span data-stu-id="0b67f-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="0b67f-142">應用程式的 `SaveStrokeCollection` 方法會檢查現有的辨識器內容，並完成目前筆劃集合的辨識。</span><span class="sxs-lookup"><span data-stu-id="0b67f-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="0b67f-143">然後， [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合就會加入至筆墨物件的 [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) 。</span><span class="sxs-lookup"><span data-stu-id="0b67f-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 
