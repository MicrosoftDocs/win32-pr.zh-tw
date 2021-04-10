---
title: 'C (RPC) '
description: 在遠端程序呼叫中，以 C 為開頭的單字 (RPC) 詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: da1ee843-c33e-42a1-bcaf-6cdb4834e70b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15eb37af87fd36dd31f3e9e106904b4ce734c15
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933852"
---
# <a name="c-rpc"></a><span data-ttu-id="9a2d0-103">C (RPC) </span><span class="sxs-lookup"><span data-stu-id="9a2d0-103">C (RPC)</span></span>

<span data-ttu-id="9a2d0-104">[](a-glos.md) [B](b-glos.md) [](v-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [](u-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="9a2d0-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="9a2d0-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Cell Directory 服務 (CD)**</span><span class="sxs-lookup"><span data-stu-id="9a2d0-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Cell Directory Service (CDS)**</span></span>
</dt> <dd>

<span data-ttu-id="9a2d0-106">Open Software Foundation 分散式運算環境的名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-106">Name-service provider for the Open Software Foundation's Distributed Computing Environment.</span></span>

</dd> <dt>

<span data-ttu-id="9a2d0-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**用戶端存根**</span><span class="sxs-lookup"><span data-stu-id="9a2d0-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**client stub**</span></span>
</dt> <dd>

<span data-ttu-id="9a2d0-108">MIDL 產生的 C 語言原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-108">MIDL-generated C-language source code.</span></span> <span data-ttu-id="9a2d0-109">它包含用戶端應用程式在獨立應用程式中使用傳統函式呼叫的模型進行遠端程序呼叫所需的所有功能。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-109">It contains all the functions necessary for the client application to make remote procedure calls using the model of a traditional function call in a standalone application.</span></span> <span data-ttu-id="9a2d0-110">用戶端存根負責封送處理輸入參數和封送處理輸出參數。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-110">The client stub is responsible for marshaling input parameters and unmarshaling output parameters.</span></span> <span data-ttu-id="9a2d0-111">另請參閱 [*伺服器 stub*](s-glos.md)、 [*proxy 存根*](p-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-111">See also [*server stub*](s-glos.md), [*proxy stub*](p-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a2d0-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**符合標準的陣列**</span><span class="sxs-lookup"><span data-stu-id="9a2d0-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**conformant array**</span></span>
</dt> <dd>

<span data-ttu-id="9a2d0-113">大小是由另一個參數、結構欄位或運算式在執行時間決定其大小的陣列。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-113">Array whose size is determined at run time by another parameter, structure field, or expression.</span></span>

</dd> <dt>

<span data-ttu-id="9a2d0-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**連線導向**</span><span class="sxs-lookup"><span data-stu-id="9a2d0-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**connection-oriented**</span></span>
</dt> <dd>

<span data-ttu-id="9a2d0-115">通訊協定或傳輸提供虛擬電路，資料封包會以傳輸的相同順序接收。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-115">Communications protocol or transport that provides a virtual circuit through which data packets are received in the same order as they were transmitted.</span></span> <span data-ttu-id="9a2d0-116">如果電腦之間的連接失敗，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-116">If the connection between computers fails, the application is notified.</span></span> <span data-ttu-id="9a2d0-117">[*TCP*](t-glos.md) 和 [*SPX*](s-glos.md) 是連接導向通訊協定的範例。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-117">[*TCP*](t-glos.md) and [*SPX*](s-glos.md) are examples of connection-oriented protocols.</span></span> <span data-ttu-id="9a2d0-118">另請參閱 [*資料包*](d-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-118">See also [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a2d0-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**連接**</span><span class="sxs-lookup"><span data-stu-id="9a2d0-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**connectionless**</span></span>
</dt> <dd>

<span data-ttu-id="9a2d0-120">請參閱 [*資料包*](d-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-120">See [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a2d0-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**內容取消**</span><span class="sxs-lookup"><span data-stu-id="9a2d0-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**context rundown**</span></span>
</dt> <dd>

<span data-ttu-id="9a2d0-122">從用戶端與伺服器應用程式之間的系結非預期終止所產生的伺服器通知。</span><span class="sxs-lookup"><span data-stu-id="9a2d0-122">Server notification that results from an unexpected termination of the binding between client and server applications.</span></span>

</dd> </dl>

 

 




