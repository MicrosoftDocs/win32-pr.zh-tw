---
title: 處理未知的錯誤
description: 處理未知的錯誤
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022011"
---
# <a name="handling-unknown-errors"></a>處理未知的錯誤

只從實作為合法 returnable 的介面方法獲批准傳回狀態碼是合法的。 如果無法觀察到這項規則，就會讓傳回的錯誤碼值和應用程式所獲批准的值之間有衝突的可能性。 從內部呼叫的函式傳播錯誤碼時，請特別注意這個潛在問題。

呼叫介面的應用程式應該將任何未知的傳回錯誤碼視為 (，而不是成功的程式碼) 與 E 未預期的同義 \_ 。 COM 定義介面和函式的用戶端需要這種處理未知錯誤碼的做法。 由於一般的程式設計作法是要詳細地處理一些特定的錯誤碼，並以一般方式處理其餘的程式碼，因此很容易就能滿足這項處理非預期或不明錯誤碼的需求。

呼叫介面方法時，請務必處理所有可能的錯誤。 若未這麼做，可能會導致您的應用程式損毀、損毀資料，或容易受到安全性攻擊。 下列程式碼範例顯示處理未知錯誤的建議方式：


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



下列錯誤檢查通常會與不會傳回任何特殊 (的常式（ \_ 確定或某些未預期的錯誤) ）搭配使用：


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的錯誤處理](error-handling-in-com.md)
</dt> </dl>

 

 




