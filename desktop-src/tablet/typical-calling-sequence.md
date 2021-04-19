---
description: 您必須用來建立筆跡辨識器的方法是由 Tablet PC 平臺 Api 呼叫，而不是直接由啟用筆墨的應用程式所呼叫。下列步驟代表執行這些方法的一般呼叫順序：載入 DLL。&\# 160;已建立 HRECOGNIZER 控制碼。&\# 160;已建立 HRECOCONTEXT 控制碼。此內容已設定辨識器選項和模式。筆劃會加入筆墨資料中。輸入已結束。可以辨認筆墨。會傳回辨識結果。HRECOCONTEXT 控制碼已損毀。HRECOGNIZER 控制碼已損毀。下列程式碼大綱也會說明呼叫順序： C + + CreateRecognizer (CLSID，&hrec) ;雖然 (更多的筆墨來辨識 ... ) {//Create a coNtext，每一次要辨識的筆墨都能辨識 hrc = CreateCoNtext (hrec，&hrc) ;//函式來設定這個內容 SetGuide 的選項和模式 (hrc、pGuide、0) ;SetFactoid (hrc，5，PHONE) ;只有在使用 forms SetFlags 的應用程式中 (hrc、RECOFLAG \_ WORDMODE) ;//罕見的情況下，只有在需要 word 模式、不是字典或單一分割 SetWordList (hrc、hwl) ;//在這一段筆墨中加入所有筆劃，同時 (更多筆觸 ... ) {AddStroke (hrc、Null、800、pPacket、pXForm) ; 每個筆劃一個//一個呼叫} EndInkInput (hrc) ;//這會取得筆跡辨識的進程 (hrc) ;//如果這是簡單的應用程式，則會呼叫此程式以取得簡單的回應 GetBestResultString (hrc、長度、緩衝區) ;/如果這是複雜的應用程式，它會呼叫此程式以取得完整的答案 GetLatticePtr (hrc、&pLattice) ;//終結內容 DestroyCoNtext (hrc) ;}//在應用程式關閉 DestroyRecognizer (hrec) 之前呼叫。
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: 一般呼叫順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983742"
---
# <a name="typical-calling-sequence"></a><span data-ttu-id="c18f3-103">一般呼叫順序</span><span class="sxs-lookup"><span data-stu-id="c18f3-103">Typical Calling Sequence</span></span>

<span data-ttu-id="c18f3-104">您必須用來建立筆跡辨識器的方法是由 Tablet PC 平臺 Api 呼叫，而不是直接由啟用筆墨的應用程式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="c18f3-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="c18f3-105">下列步驟代表用來執行這些方法的一般呼叫順序：</span><span class="sxs-lookup"><span data-stu-id="c18f3-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="c18f3-106">已載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="c18f3-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="c18f3-107">系統會建立 [HRECOGNIZER](hrecognizer-handle.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="c18f3-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="c18f3-108">系統會建立 [HRECOCONTEXT](hrecocontext-handle.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="c18f3-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="c18f3-109">此內容已設定辨識器選項和模式。</span><span class="sxs-lookup"><span data-stu-id="c18f3-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="c18f3-110">筆劃會加入筆墨資料中。</span><span class="sxs-lookup"><span data-stu-id="c18f3-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="c18f3-111">輸入已結束。</span><span class="sxs-lookup"><span data-stu-id="c18f3-111">Input is ended.</span></span>
7.  <span data-ttu-id="c18f3-112">可以辨認筆墨。</span><span class="sxs-lookup"><span data-stu-id="c18f3-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="c18f3-113">會傳回辨識結果。</span><span class="sxs-lookup"><span data-stu-id="c18f3-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="c18f3-114">[HRECOCONTEXT](hrecocontext-handle.md)控制碼已損毀。</span><span class="sxs-lookup"><span data-stu-id="c18f3-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="c18f3-115">[HRECOGNIZER](hrecognizer-handle.md)控制碼已損毀。</span><span class="sxs-lookup"><span data-stu-id="c18f3-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="c18f3-116">下列程式碼大綱也會說明呼叫順序：</span><span class="sxs-lookup"><span data-stu-id="c18f3-116">The calling sequence is also illustrated in the following code outline:</span></span>


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a><span data-ttu-id="c18f3-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c18f3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c18f3-118">辨識器 Api</span><span class="sxs-lookup"><span data-stu-id="c18f3-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="c18f3-119">辨識 API 架構</span><span class="sxs-lookup"><span data-stu-id="c18f3-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



