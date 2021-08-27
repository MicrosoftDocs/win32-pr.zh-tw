---
description: 此應用程式會示範如何建立簡單的手寫辨識應用程式。此程式會建立 InkCollector 物件，以啟用視窗和預設辨識器內容物件的筆墨。
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: 基本識別範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf45aa7695866e1cf413ea42b7c377b07ea84984ecf2cc3f44da93ff868072d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111138"
---
# <a name="basic-recognition-sample"></a>基本識別範例

此應用程式會示範如何建立簡單的 *手寫* 識別應用程式。

此程式會建立 [**InkCollector**](inkcollector-class.md)物件，以啟用視窗和預設辨識 *器內容* 物件的 *筆墨*。 收到「辨識！」時 從應用程式的功能表中引發的命令，系統會將所收集的筆墨筆觸傳遞給辨識器內容。 最佳的結果字串會顯示在訊息方塊中。

## <a name="creating-the-recognizercontext-object"></a>建立 RecognizerCoNtext 物件

在應用程式的 WndProc 程式中，如果在啟動時收到了 WM \_ 建立訊息，則會建立使用預設辨識器的新辨識器內容。 此內容用於應用程式中的所有辨識。


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a>辨識筆觸

當使用者按一下 [辨識] 時，就會收到辨識命令！ 功能表項目。 程式碼會取得筆墨 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 的指標， (PIInkStrokes 的 [**InkDisp**](inkdisp-class.md) 物件) ，然後使用 putref 筆劃的呼叫，將 **InkStrokes** 傳遞給辨識器內容 \_ 。


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



然後，程式碼會呼叫 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [**辨識**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)方法，並將指標傳入 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件來保存結果。


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



最後，此程式碼會使用 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件的 [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) 屬性，將最上層的辨識結果取出至字串變數、釋放 **IInkRecognitionResult** 物件，並在訊息方塊中顯示字串。


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



請務必重設使用方式之間的辨識器內容。


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
