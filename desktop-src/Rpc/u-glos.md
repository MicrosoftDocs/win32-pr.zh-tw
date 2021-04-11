---
title: 'U (RPC) '
description: 在遠端程序呼叫中，從 U 開始的單字 (RPC) 詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b74acb87-030a-4263-9399-5fab6f239d02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be321a420b31fdebffc8175a917dd599755f7492
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842963"
---
# <a name="u-rpc"></a><span data-ttu-id="6c460-103">U (RPC) </span><span class="sxs-lookup"><span data-stu-id="6c460-103">U (RPC)</span></span>

<span data-ttu-id="6c460-104">[](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="6c460-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) U [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="6c460-105"><span id="_rpc_udp_glos"></span><span id="_RPC_UDP_GLOS"></span>**使用者資料包協定 (UDP)**</span><span class="sxs-lookup"><span data-stu-id="6c460-105"><span id="_rpc_udp_glos"></span><span id="_RPC_UDP_GLOS"></span>**User Datagram Protocol (UDP)**</span></span>
</dt> <dd>

<span data-ttu-id="6c460-106">使用無連接 [*資料包*](d-glos.md) 通訊端且在網際網路通訊協定上階層式網路傳輸 ([*IP)*](i-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="6c460-106">Network transport that uses connectionless [*datagram*](d-glos.md) sockets and is layered on top of the Internet Protocol ([*IP)*](i-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c460-107"><span id="_rpc_unbind_glos"></span><span id="_RPC_UNBIND_GLOS"></span>**先**</span><span class="sxs-lookup"><span data-stu-id="6c460-107"><span id="_rpc_unbind_glos"></span><span id="_RPC_UNBIND_GLOS"></span>**unbind**</span></span>
</dt> <dd>

<span data-ttu-id="6c460-108">終止用戶端與伺服器之間邏輯連接的進程。</span><span class="sxs-lookup"><span data-stu-id="6c460-108">Process of terminating the logical connection between a client and server.</span></span>

</dd> <dt>

<span data-ttu-id="6c460-109"><span id="_rpc_unique_pointer_glos"></span><span id="_RPC_UNIQUE_POINTER_GLOS"></span>**唯一指標**</span><span class="sxs-lookup"><span data-stu-id="6c460-109"><span id="_rpc_unique_pointer_glos"></span><span id="_RPC_UNIQUE_POINTER_GLOS"></span>**unique pointer**</span></span>
</dt> <dd>

<span data-ttu-id="6c460-110">可以是 null 或指向現有資料的指標，其值可以在遠端程序呼叫期間變更。</span><span class="sxs-lookup"><span data-stu-id="6c460-110">Pointer that can be null or point to existing data, whose value can change during a remote procedure call.</span></span> <span data-ttu-id="6c460-111">唯一的指標不能有別名。</span><span class="sxs-lookup"><span data-stu-id="6c460-111">A unique pointer cannot be aliased.</span></span> <span data-ttu-id="6c460-112">\[ [Unique](/windows/desktop/Midl/unique) \] 屬性指定唯一指標。</span><span class="sxs-lookup"><span data-stu-id="6c460-112">The \[ [unique](/windows/desktop/Midl/unique)\] attribute designates a unique pointer.</span></span> <span data-ttu-id="6c460-113">另請參閱 [*完整指標*](f-glos.md)、 [*參考指標*](r-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="6c460-113">See also [*full pointer*](f-glos.md), [*reference pointer*](r-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c460-114"><span id="_rpc_uuid_glos"></span><span id="_RPC_UUID_GLOS"></span>**通用唯一識別碼 (UUID)**</span><span class="sxs-lookup"><span data-stu-id="6c460-114"><span id="_rpc_uuid_glos"></span><span id="_RPC_UUID_GLOS"></span>**Universal Unique Identifier (UUID)**</span></span>
</dt> <dd>

<span data-ttu-id="6c460-115"> (或 [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)) 128 位值，用於跨進程通訊以識別實體，例如用戶端和伺服器介面、管理員進入點向量和 RPC 物件。</span><span class="sxs-lookup"><span data-stu-id="6c460-115">(or [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)) 128-bit value used in cross-process communication to identify entities such as client and server interfaces, manager entry-point vectors, and RPC objects.</span></span> <span data-ttu-id="6c460-116">另請參閱 [uuidgen.exe](/windows)。</span><span class="sxs-lookup"><span data-stu-id="6c460-116">See also [uuidgen](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="6c460-117"><span id="_rpc_unmarshaling_glos"></span><span id="_RPC_UNMARSHALING_GLOS"></span>**送**</span><span class="sxs-lookup"><span data-stu-id="6c460-117"><span id="_rpc_unmarshaling_glos"></span><span id="_RPC_UNMARSHALING_GLOS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="6c460-118">跨進程界限傳送的解除封裝參數的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6c460-118">Process of unpackaging parameters that have been sent across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="6c460-119"><span id="_rpc_uuidgen_glos"></span><span id="_RPC_UUIDGEN_GLOS"></span>**uuidgen.exe**</span><span class="sxs-lookup"><span data-stu-id="6c460-119"><span id="_rpc_uuidgen_glos"></span><span id="_RPC_UUIDGEN_GLOS"></span>**uuidgen**</span></span>
</dt> <dd>

<span data-ttu-id="6c460-120">隨附于平臺軟體發展工具組 (SDK) 的公用程式，它會使用時間值和電腦的網路介面卡識別碼來產生保證是唯一的 [uuid](/windows) 。</span><span class="sxs-lookup"><span data-stu-id="6c460-120">Utility program, provided with the Platform Software Development Kit (SDK), that uses a time value and your machine's network card ID to generate [UUIDs](/windows) that are guaranteed to be unique.</span></span>

</dd> </dl>

 

 
