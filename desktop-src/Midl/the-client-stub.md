---
title: 用戶端存根
description: 用戶端 stub 模組會針對輸入 IDL 檔案中定義的每個作業，在用戶端上提供代理的進入點。
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL 和 RPC MIDL、介面、用戶端 stub
- 介面 MIDL
- 介面 MIDL、MIDL 和 RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301567"
---
# <a name="the-client-stub"></a><span data-ttu-id="8bd68-106">用戶端存根</span><span class="sxs-lookup"><span data-stu-id="8bd68-106">The Client Stub</span></span>

<span data-ttu-id="8bd68-107">用戶端 stub 模組會針對輸入 IDL 檔案中定義的每個作業，在用戶端上提供代理的進入點。</span><span class="sxs-lookup"><span data-stu-id="8bd68-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="8bd68-108">當用戶端應用程式呼叫遠端程式時，其呼叫會先進入用戶端 stub 檔案中的代理常式。</span><span class="sxs-lookup"><span data-stu-id="8bd68-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="8bd68-109">用戶端 stub 常式會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="8bd68-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="8bd68-110">封送處理引數。</span><span class="sxs-lookup"><span data-stu-id="8bd68-110">Marshals arguments.</span></span> <span data-ttu-id="8bd68-111">用戶端存根會將輸入引數封裝到可傳送至伺服器的表單中。</span><span class="sxs-lookup"><span data-stu-id="8bd68-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="8bd68-112">呼叫用戶端執行時間程式庫，將引數傳送至遠端位址空間，並叫用伺服器位址空間中的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="8bd68-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="8bd68-113">拆收輸出引數。</span><span class="sxs-lookup"><span data-stu-id="8bd68-113">Unmarshals output arguments.</span></span> <span data-ttu-id="8bd68-114">用戶端存根解壓縮輸出引數，並傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="8bd68-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="8bd68-115">MIDL 編譯器會將 [**/client**](-client.md)、 [**/cstub**](-cstub.md)和 [**/out**](-out.md) 參數切換至用戶端存根檔案。</span><span class="sxs-lookup"><span data-stu-id="8bd68-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




