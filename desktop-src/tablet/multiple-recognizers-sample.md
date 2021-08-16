---
description: 此範例示範 MicrosoftTablet PC Automation 應用程式開發介面的 advanced 功能 (API) 用於手寫辨識。
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: 多個辨識器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d687f1bddd1f3c57cc482070b8e5826126b6e5b0f716fa3649df01ad6eab30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856547"
---
# <a name="multiple-recognizers-sample"></a>多個辨識器範例

此範例示範 MicrosoftTablet PC Automation 應用程式開發介面的 advanced 功能 (API) 用於 *手寫* 識別。

其中包括下列各項：

-   列舉已安裝的辨識器
-   使用特定語言辨識器建立辨識 *器內容*
-   使用筆劃集合序列化辨識結果
-   將筆劃集合組織成 [**InkDisp**](inkdisp-class.md) 物件內的自訂集合
-   將 *筆墨* 物件 *序列化為 (ISF) 檔案的筆墨序列化格式* ，並加以抓取
-   設定辨識器輸入指南
-   使用同步和非同步識別

## <a name="ink-headers"></a>筆跡標頭

首先，請加入 Tablet PC 自動化介面的標頭。 這些會隨 Microsoft Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 一起安裝。


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



EventSinks .h 檔案會定義 IInkEventsImpl 和 IInkRecognitionEventsImpl 介面。


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>列舉已安裝的辨識器

應用程式的 LoadMenu 方法會在 [建立新的筆觸] 功能表中填入可用的辨識器。 系統會建立 [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) 。 如果 **InkRecognizers** 物件的 [[**語言**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages)] 屬性不是空的，則辨識器會是 *文字辨識器*，並將其 [[**名稱**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name)] 屬性的值加入功能表中。


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



## <a name="creating-an-ink-collector"></a>建立筆墨收集器

應用程式的 >oncreate 方法會建立 [**InkCollector**](inkcollector-class.md) 物件、將它連接至其事件來源，以及啟用筆墨收集。


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>建立辨識器內容

應用程式的 CreateRecoCoNtext 方法會建立並初始化新的辨識器內容，並設定相關聯語言所支援的指南。 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件的 [**CreateRecognizerCoNtext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext)方法會建立語言的 [**IInkRecognizerCoNtext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2)物件。 必要時，會取代舊的辨識器內容。 內容會連接到其事件來源。 最後，會針對辨識器內容所支援的輔助線，檢查辨識器內容的 [ [**功能**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) ] 屬性。


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>收集筆劃並顯示辨識結果

應用程式的 OnStroke 方法會更新筆墨收集器的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 、取消現有的非同步識別要求，並在辨識器內容上建立辨識要求。


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



應用程式的 `OnRecognition` 方法會將識別要求的結果傳送至輸出視窗的 `UpdateString` 方法。


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>刪除筆劃和辨識結果

應用程式的 OnClear 方法會刪除 [**InkDisp**](inkdisp-class.md) 物件中的所有筆劃和辨識結果，並清除視窗。 已移除辨識器內容與其 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合的關聯。


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



## <a name="changing-recognizer-contexts"></a>變更辨識器內容

當使用者在 [建立新的筆觸] 功能表中選取辨識器時，會呼叫應用程式的 OnNewStrokes 方法。 儲存目前的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 。 如果選取不同的語言辨識器，則會建立新的辨識器內容。 然後，新的 **InkStrokes** 會附加至新的辨識器內容。


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



然後，它會呼叫 StartNewStrokeCollection，它會建立空的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ，並將它附加至辨識器內容。

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>儲存辨識器內容的筆劃集合

應用程式的 `SaveStrokeCollection` 方法會檢查現有的辨識器內容，並完成目前筆劃集合的辨識。 然後， [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合就會加入至筆墨物件的 [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) 。


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



 

 
