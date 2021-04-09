---
title: 固定陣列
description: 如果您的介面指定具有特定元素數目的陣列做為參數，則會使用固定陣列。 使用 MIDL 時，您會以 C 中定義的相同方式定義固定陣列。您可以指定陣列的類型、名稱和大小。
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673820"
---
# <a name="fixed-arrays"></a><span data-ttu-id="0b106-104">固定陣列</span><span class="sxs-lookup"><span data-stu-id="0b106-104">Fixed Arrays</span></span>

<span data-ttu-id="0b106-105">如果您的介面指定具有特定元素數目的陣列做為參數，則會使用固定陣列。</span><span class="sxs-lookup"><span data-stu-id="0b106-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="0b106-106">使用 MIDL 時，您會以 C 中定義的相同方式定義固定陣列。您可以指定陣列的類型、名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="0b106-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="0b106-107">下列範例示範如何定義固定陣列。</span><span class="sxs-lookup"><span data-stu-id="0b106-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="0b106-108">當用戶端程式將固定陣列傳遞至伺服器程式時，用戶端存根會將整個陣列傳送至伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="0b106-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="0b106-109">伺服器 stub 會為數組配置記憶體，並將其在網路上收到的陣列資料儲存至配置的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="0b106-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="0b106-110">然後，它會將陣列傳遞至伺服器上的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="0b106-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="0b106-111">伺服器可能會修改陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="0b106-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="0b106-112">當遠端程式終止時，伺服器存根會將陣列的內容傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b106-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="0b106-113">用戶端存根會將它從伺服器 stub 收到的資料複製到原始陣列中。</span><span class="sxs-lookup"><span data-stu-id="0b106-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="0b106-114">然後，用戶端程式就可以使用資料，就像從本機程序呼叫接收資料一樣。</span><span class="sxs-lookup"><span data-stu-id="0b106-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 




