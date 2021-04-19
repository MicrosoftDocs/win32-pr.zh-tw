---
title: 明確的系結控制碼
description: 為了充分掌控系結程式，用戶端/伺服器應用程式可能會使用明確的系結控制碼。
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965589"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="c80e1-103">明確的系結控制碼</span><span class="sxs-lookup"><span data-stu-id="c80e1-103">Explicit Binding Handles</span></span>

<span data-ttu-id="c80e1-104">為了充分掌控系結程式，用戶端/伺服器應用程式可能會使用明確的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="c80e1-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="c80e1-105">和隱含的控制碼一樣，明確的系結控制碼可讓您的用戶端應用程式選取伺服器來執行其呼叫。</span><span class="sxs-lookup"><span data-stu-id="c80e1-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="c80e1-106">此外，明確的系結控制碼可讓您的用戶端/伺服器應用程式建立已驗證的 RPC 通訊會話。</span><span class="sxs-lookup"><span data-stu-id="c80e1-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="c80e1-107">使用明確的控制碼時，您的用戶端可以連接到多部伺服器，並在多部伺服器上執行遠端程式。</span><span class="sxs-lookup"><span data-stu-id="c80e1-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="c80e1-108">多執行緒和非同步用戶端應用程式甚至可以連接至多部伺服器，並同時執行多個遠端程式。</span><span class="sxs-lookup"><span data-stu-id="c80e1-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="c80e1-109">您的用戶端應用程式必須將明確控制碼作為參數傳遞給每個遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="c80e1-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="c80e1-110">為了符合憑證標準，應將控制碼指定為每個遠端程式上的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="c80e1-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="c80e1-111">不過，Microsoft 的 RPC 擴充功能可讓您指定其他位置的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="c80e1-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="c80e1-112">如需詳細資訊，請參閱 [MICROSOFT RPC Binding-Handle 擴充](microsoft-rpc-binding-handle-extensions.md)功能。</span><span class="sxs-lookup"><span data-stu-id="c80e1-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="c80e1-113">若要建立明確的控制碼，請將控制碼宣告為 IDL 檔案中遠端作業的參數。</span><span class="sxs-lookup"><span data-stu-id="c80e1-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="c80e1-114">您可以重新定義 [Hello，World 範例](tutorial.md) 以使用明確的控制碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c80e1-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="c80e1-115">您可以在單一介面中結合明確和隱含控制碼。</span><span class="sxs-lookup"><span data-stu-id="c80e1-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="c80e1-116">如果函式在其參數清單中有明確的控制碼，則會使用該控制碼。</span><span class="sxs-lookup"><span data-stu-id="c80e1-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="c80e1-117">如果使用隱含控制碼之介面中的函式未指定明確的控制碼，則會使用預設的隱含控制碼。</span><span class="sxs-lookup"><span data-stu-id="c80e1-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




