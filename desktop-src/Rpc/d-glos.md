---
title: 'D (RPC) '
description: 在遠端程序呼叫中，以 D 開頭的單字會 (RPC) 詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a983860b-39af-4195-8b02-caac38cf42d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495b78157870e8e3de9ed55c56e6bb3d0bfcccdc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685415"
---
# <a name="d-rpc"></a><span data-ttu-id="746b9-103">D (RPC) </span><span class="sxs-lookup"><span data-stu-id="746b9-103">D (RPC)</span></span>

<span data-ttu-id="746b9-104">[](a-glos.md) [B](b-glos.md) [C](c-glos.md) D [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [](u-glos.md) [](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="746b9-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) D [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="746b9-105"><span id="_rpc_datagram_glos"></span><span id="_RPC_DATAGRAM_GLOS"></span>**傳送**</span><span class="sxs-lookup"><span data-stu-id="746b9-105"><span id="_rpc_datagram_glos"></span><span id="_RPC_DATAGRAM_GLOS"></span>**datagram**</span></span>
</dt> <dd>

<span data-ttu-id="746b9-106">通訊協定或傳輸，其中的資料封包會獨立路由傳送。</span><span class="sxs-lookup"><span data-stu-id="746b9-106">Communications protocol or transport in which data packets are routed independently.</span></span> <span data-ttu-id="746b9-107">它們可能會遵循不同的路由，並以與其傳送的不同順序抵達。</span><span class="sxs-lookup"><span data-stu-id="746b9-107">They may follow different routes and arrive in a different order from which they were sent.</span></span> <span data-ttu-id="746b9-108">[*UDP*](u-glos.md) 和 [*IPX*](i-glos.md) 是傳輸層-資料包通訊協定的範例。</span><span class="sxs-lookup"><span data-stu-id="746b9-108">[*UDP*](u-glos.md) and [*IPX*](i-glos.md) are examples of transport layer–datagram protocols.</span></span> <span data-ttu-id="746b9-109">另請參閱 [*連線導向*](c-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="746b9-109">See also [*connection-oriented*](c-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="746b9-110"><span id="_rpc_discriminant_glos"></span><span id="_RPC_DISCRIMINANT_GLOS"></span>**判別**</span><span class="sxs-lookup"><span data-stu-id="746b9-110"><span id="_rpc_discriminant_glos"></span><span id="_RPC_DISCRIMINANT_GLOS"></span>**discriminant**</span></span>
</dt> <dd>

<span data-ttu-id="746b9-111">變數，指定可以儲存在聯集內的資料類型。</span><span class="sxs-lookup"><span data-stu-id="746b9-111">Variable that specifies the data types that can be stored in a union.</span></span>

</dd> <dt>

<span data-ttu-id="746b9-112"><span id="_rpc_discriminated_union_glos"></span><span id="_RPC_DISCRIMINATED_UNION_GLOS"></span>**區分聯集**</span><span class="sxs-lookup"><span data-stu-id="746b9-112"><span id="_rpc_discriminated_union_glos"></span><span id="_RPC_DISCRIMINATED_UNION_GLOS"></span>**discriminated union**</span></span>
</dt> <dd>

<span data-ttu-id="746b9-113"> (或 *變異記錄*) 聯集，其中包含做為資料結構一部分的鑒別子，如此一來，目前有效的資料類型會與聯集一起傳送。</span><span class="sxs-lookup"><span data-stu-id="746b9-113">(or *variant record*) Union that includes a discriminator as part of the data structure so that the currently valid data type is transmitted along with the union.</span></span> <span data-ttu-id="746b9-114">另請參閱 [*封裝聯集*](e-glos.md)、nonencapsulated 聯 [*集*](n-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="746b9-114">See also [*encapsulated union*](e-glos.md), [*nonencapsulated union*](n-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="746b9-115"><span id="_rpc_dce_glos"></span><span id="_RPC_DCE_GLOS"></span>**(DCE) 的分散式運算環境**</span><span class="sxs-lookup"><span data-stu-id="746b9-115"><span id="_rpc_dce_glos"></span><span id="_RPC_DCE_GLOS"></span>**Distributed Computing Environment (DCE)**</span></span>
</dt> <dd>

<span data-ttu-id="746b9-116">為一組整合式服務（包括遠端程序呼叫、分散式檔案系統和安全性服務）提供開放式 Software Foundation 的規格。</span><span class="sxs-lookup"><span data-stu-id="746b9-116">Specification of the Open Software Foundation for a set of integrated services, including remote procedure calls, distributed file systems, and security services.</span></span> <span data-ttu-id="746b9-117">憑證-DCE RPC standard 是 Microsoft RPC 的基礎。</span><span class="sxs-lookup"><span data-stu-id="746b9-117">The OSF-DCE RPC standard is the basis for Microsoft RPC.</span></span>

</dd> <dt>

<span data-ttu-id="746b9-118"><span id="_rpc_dynamic_endpoint_glos"></span><span id="_RPC_DYNAMIC_ENDPOINT_GLOS"></span>**動態端點**</span><span class="sxs-lookup"><span data-stu-id="746b9-118"><span id="_rpc_dynamic_endpoint_glos"></span><span id="_RPC_DYNAMIC_ENDPOINT_GLOS"></span>**dynamic endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="746b9-119">網路專用–在執行時間要求並指派的伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="746b9-119">Network specific–server address that is requested and assigned at run time.</span></span> <span data-ttu-id="746b9-120">另請參閱 [*知名的端點*](w-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="746b9-120">See also [*well-known endpoint*](w-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="746b9-121"><span id="_rpc_dynamic_identity_tracking_glos"></span><span id="_RPC_DYNAMIC_IDENTITY_TRACKING_GLOS"></span>**動態身分識別追蹤**</span><span class="sxs-lookup"><span data-stu-id="746b9-121"><span id="_rpc_dynamic_identity_tracking_glos"></span><span id="_RPC_DYNAMIC_IDENTITY_TRACKING_GLOS"></span>**dynamic identity tracking**</span></span>
</dt> <dd>

<span data-ttu-id="746b9-122">規格：每當用戶端呼叫遠端程式時，RPC 執行時間程式庫會使用呼叫執行緒的認證，而不是系結控制碼，以便進行驗證。</span><span class="sxs-lookup"><span data-stu-id="746b9-122">Specification that the RPC run-time library will use the credentials of the calling thread, rather than the binding handle, for authentication each time the client calls a remote procedure.</span></span> <span data-ttu-id="746b9-123">另請參閱 [*靜態身分識別追蹤*](s-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="746b9-123">See also [*static identity tracking*](s-glos.md).</span></span>

</dd> </dl>

 

 




