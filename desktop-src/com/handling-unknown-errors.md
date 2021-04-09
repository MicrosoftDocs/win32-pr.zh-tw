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
# <a name="handling-unknown-errors"></a><span data-ttu-id="1df95-103">處理未知的錯誤</span><span class="sxs-lookup"><span data-stu-id="1df95-103">Handling Unknown Errors</span></span>

<span data-ttu-id="1df95-104">只從實作為合法 returnable 的介面方法獲批准傳回狀態碼是合法的。</span><span class="sxs-lookup"><span data-stu-id="1df95-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="1df95-105">如果無法觀察到這項規則，就會讓傳回的錯誤碼值和應用程式所獲批准的值之間有衝突的可能性。</span><span class="sxs-lookup"><span data-stu-id="1df95-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="1df95-106">從內部呼叫的函式傳播錯誤碼時，請特別注意這個潛在問題。</span><span class="sxs-lookup"><span data-stu-id="1df95-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="1df95-107">呼叫介面的應用程式應該將任何未知的傳回錯誤碼視為 (，而不是成功的程式碼) 與 E 未預期的同義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1df95-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="1df95-108">COM 定義介面和函式的用戶端需要這種處理未知錯誤碼的做法。</span><span class="sxs-lookup"><span data-stu-id="1df95-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="1df95-109">由於一般的程式設計作法是要詳細地處理一些特定的錯誤碼，並以一般方式處理其餘的程式碼，因此很容易就能滿足這項處理非預期或不明錯誤碼的需求。</span><span class="sxs-lookup"><span data-stu-id="1df95-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="1df95-110">呼叫介面方法時，請務必處理所有可能的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1df95-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="1df95-111">若未這麼做，可能會導致您的應用程式損毀、損毀資料，或容易受到安全性攻擊。</span><span class="sxs-lookup"><span data-stu-id="1df95-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="1df95-112">下列程式碼範例顯示處理未知錯誤的建議方式：</span><span class="sxs-lookup"><span data-stu-id="1df95-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


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



<span data-ttu-id="1df95-113">下列錯誤檢查通常會與不會傳回任何特殊 (的常式（ \_ 確定或某些未預期的錯誤) ）搭配使用：</span><span class="sxs-lookup"><span data-stu-id="1df95-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1df95-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="1df95-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df95-115">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="1df95-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




