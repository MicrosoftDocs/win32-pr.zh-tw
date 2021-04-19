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
# <a name="typical-calling-sequence"></a>一般呼叫順序

您必須用來建立筆跡辨識器的方法是由 Tablet PC 平臺 Api 呼叫，而不是直接由啟用筆墨的應用程式所呼叫。

下列步驟代表用來執行這些方法的一般呼叫順序：

1.  已載入 DLL。
2.  系統會建立 [HRECOGNIZER](hrecognizer-handle.md) 控制碼。
3.  系統會建立 [HRECOCONTEXT](hrecocontext-handle.md) 控制碼。
4.  此內容已設定辨識器選項和模式。
5.  筆劃會加入筆墨資料中。
6.  輸入已結束。
7.  可以辨認筆墨。
8.  會傳回辨識結果。
9.  [HRECOCONTEXT](hrecocontext-handle.md)控制碼已損毀。
10. [HRECOGNIZER](hrecognizer-handle.md)控制碼已損毀。

下列程式碼大綱也會說明呼叫順序：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[辨識器 Api](recognizer-apis.md)
</dt> <dt>

[辨識 API 架構](recognition-api-architecture.md)
</dt> </dl>

 

 



