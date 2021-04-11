---
description: 此應用程式會示範如何建立簡單的手寫辨識應用程式。此程式會建立 InkCollector 物件，以啟用視窗和預設辨識器內容物件的筆墨。
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: 基本識別範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851623"
---
# <a name="basic-recognition-sample"></a><span data-ttu-id="781e4-103">基本識別範例</span><span class="sxs-lookup"><span data-stu-id="781e4-103">Basic Recognition Sample</span></span>

<span data-ttu-id="781e4-104">此應用程式會示範如何建立簡單的 *手寫* 識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="781e4-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="781e4-105">此程式會建立 [**InkCollector**](inkcollector-class.md)物件，以啟用視窗和預設辨識 *器內容* 物件的 *筆墨*。</span><span class="sxs-lookup"><span data-stu-id="781e4-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="781e4-106">收到「辨識！」時</span><span class="sxs-lookup"><span data-stu-id="781e4-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="781e4-107">從應用程式的功能表中引發的命令，系統會將所收集的筆墨筆觸傳遞給辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="781e4-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="781e4-108">最佳的結果字串會顯示在訊息方塊中。</span><span class="sxs-lookup"><span data-stu-id="781e4-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="781e4-109">建立 RecognizerCoNtext 物件</span><span class="sxs-lookup"><span data-stu-id="781e4-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="781e4-110">在應用程式的 WndProc 程式中，如果在啟動時收到了 WM \_ 建立訊息，則會建立使用預設辨識器的新辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="781e4-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="781e4-111">此內容用於應用程式中的所有辨識。</span><span class="sxs-lookup"><span data-stu-id="781e4-111">This context is used for all recognition in the application.</span></span>


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



## <a name="recognizing-the-strokes"></a><span data-ttu-id="781e4-112">辨識筆觸</span><span class="sxs-lookup"><span data-stu-id="781e4-112">Recognizing the Strokes</span></span>

<span data-ttu-id="781e4-113">當使用者按一下 [辨識] 時，就會收到辨識命令！</span><span class="sxs-lookup"><span data-stu-id="781e4-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="781e4-114">功能表項目。</span><span class="sxs-lookup"><span data-stu-id="781e4-114">menu item.</span></span> <span data-ttu-id="781e4-115">程式碼會取得筆墨 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 的指標， (PIInkStrokes 的 [**InkDisp**](inkdisp-class.md) 物件) ，然後使用 putref 筆劃的呼叫，將 **InkStrokes** 傳遞給辨識器內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="781e4-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


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



<span data-ttu-id="781e4-116">然後，程式碼會呼叫 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [**辨識**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)方法，並將指標傳入 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件來保存結果。</span><span class="sxs-lookup"><span data-stu-id="781e4-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="781e4-117">最後，此程式碼會使用 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件的 [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) 屬性，將最上層的辨識結果取出至字串變數、釋放 **IInkRecognitionResult** 物件，並在訊息方塊中顯示字串。</span><span class="sxs-lookup"><span data-stu-id="781e4-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


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



<span data-ttu-id="781e4-118">請務必重設使用方式之間的辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="781e4-118">Be sure to reset the recognizer context between usages.</span></span>


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



 

 
