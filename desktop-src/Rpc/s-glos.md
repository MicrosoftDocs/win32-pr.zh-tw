---
title: 'S (RPC) '
description: 在遠端程序呼叫中，以 S 開頭的單字 (RPC) 詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba3c7959-2acd-4a38-b996-cfe7dac20241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89ceb4c5d1b6aae6de71e813f09e45dc3765479e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317000"
---
# <a name="s-rpc"></a><span data-ttu-id="375e6-103">S (RPC) </span><span class="sxs-lookup"><span data-stu-id="375e6-103">S (RPC)</span></span>

<span data-ttu-id="375e6-104">[](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G [](u-glos.md) [](v-glos.md) H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) S [T](t-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="375e6-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) S [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="375e6-105"><span id="rpc.s_glos_1_gly"></span><span id="RPC.S_GLOS_1_GLY"></span>**可 伸縮 性**</span><span class="sxs-lookup"><span data-stu-id="375e6-105"><span id="rpc.s_glos_1_gly"></span><span id="RPC.S_GLOS_1_GLY"></span>**scalability**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-106">能夠在多處理器系統上充分利用額外的處理能力， (2、4、8、32或更多處理器) 。</span><span class="sxs-lookup"><span data-stu-id="375e6-106">Ability to fully utilize the additional processing power on a multiprocessor system (2, 4, 8, 32, or more processors).</span></span> <span data-ttu-id="375e6-107">擴充性也是服務大量用戶端的能力。</span><span class="sxs-lookup"><span data-stu-id="375e6-107">Scalability is also the ability to service a large number of clients.</span></span>

</dd> <dt>

<span data-ttu-id="375e6-108"><span id="_rpcl_spp_glos"></span><span id="_RPCL_SPP_GLOS"></span>**排序的封包通訊協定 (SPP)**</span><span class="sxs-lookup"><span data-stu-id="375e6-108"><span id="_rpcl_spp_glos"></span><span id="_RPCL_SPP_GLOS"></span>**Sequenced Packet Protocol (SPP)**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-109">Banyan Vines 以 [*連接導向*](c-glos.md) 的通訊協定，用於透過區域網路的路由資訊封包。</span><span class="sxs-lookup"><span data-stu-id="375e6-109">Banyan Vines [*connection-oriented*](c-glos.md) communication protocol for routing information packets over local area networks.</span></span>

</dd> <dt>

<span data-ttu-id="375e6-110"><span id="_rpc_spx_glos"></span><span id="_RPC_SPX_GLOS"></span>**已排序的封包交換 (SPX)**</span><span class="sxs-lookup"><span data-stu-id="375e6-110"><span id="_rpc_spx_glos"></span><span id="_RPC_SPX_GLOS"></span>**Sequenced Packet Exchange (SPX)**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-111">Novell NetWare [*連接導向*](c-glos.md) 通訊協定，可透過區域網路和廣域網路來路由傳送資訊封包。</span><span class="sxs-lookup"><span data-stu-id="375e6-111">Novell NetWare [*connection-oriented*](c-glos.md) communication protocol for routing information packets over local area networks and wide area networks.</span></span>

</dd> <dt>

<span data-ttu-id="375e6-112"><span id="_rpc_serialization_glos"></span><span id="_RPC_SERIALIZATION_GLOS"></span>**序列 化**</span><span class="sxs-lookup"><span data-stu-id="375e6-112"><span id="_rpc_serialization_glos"></span><span id="_RPC_SERIALIZATION_GLOS"></span>**serialization**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-113">將資料封送處理至 (編碼的程式) 和將資料從 (解碼) 緩衝區進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="375e6-113">Process of marshaling data to (encoding) and unmarshaling data from (decoding) buffers that you control.</span></span> <span data-ttu-id="375e6-114">這與傳統的 RPC 使用方式相反，因為存根和 RPC 執行時間會控制封送處理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="375e6-114">This is in contrast to traditional RPC usage, where the stubs and the RPC runtime control the marshaling buffers.</span></span> <span data-ttu-id="375e6-115">也稱為 pickling。</span><span class="sxs-lookup"><span data-stu-id="375e6-115">Also called pickling.</span></span> <span data-ttu-id="375e6-116">另請參閱程式 [*序列化*](p-glos.md)， [*類型序列化*](t-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="375e6-116">See also [*procedure serialization*](p-glos.md), [*type serialization*](t-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="375e6-117"><span id="_rpc_server_stub_glos"></span><span id="_RPC_SERVER_STUB_GLOS"></span>**伺服器 stub**</span><span class="sxs-lookup"><span data-stu-id="375e6-117"><span id="_rpc_server_stub_glos"></span><span id="_RPC_SERVER_STUB_GLOS"></span>**server stub**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-118">MIDL 產生的 C 語言原始程式碼，其中包含伺服器應用程式使用本機程序呼叫處理遠端要求所需的所有功能。</span><span class="sxs-lookup"><span data-stu-id="375e6-118">MIDL-generated C-language source code that contains all the functions necessary for the server application to handle remote requests using local procedure calls.</span></span> <span data-ttu-id="375e6-119">另請參閱 [*用戶端存根*](c-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="375e6-119">See also [*client stub*](c-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="375e6-120"><span id="_rpc_session_glos"></span><span id="_RPC_SESSION_GLOS"></span>**會話**</span><span class="sxs-lookup"><span data-stu-id="375e6-120"><span id="_rpc_session_glos"></span><span id="_RPC_SESSION_GLOS"></span>**session**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-121">建立用戶端應用程式與伺服器應用程式之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="375e6-121">Established relationship between a client application and a server application.</span></span> <span data-ttu-id="375e6-122">另請參閱 [*bind*](b-glos.md)、系結 [*控制碼*](b-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="375e6-122">See also [*bind*](b-glos.md), [*binding handle*](b-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="375e6-123"><span id="_rpc_static_callback_function_glos"></span><span id="_RPC_STATIC_CALLBACK_FUNCTION_GLOS"></span>**靜態回呼函數**</span><span class="sxs-lookup"><span data-stu-id="375e6-123"><span id="_rpc_static_callback_function_glos"></span><span id="_RPC_STATIC_CALLBACK_FUNCTION_GLOS"></span>**static callback function**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-124">屬於分散式應用程式用戶端一部分的遠端程式，伺服器可呼叫以取得用戶端的資訊。</span><span class="sxs-lookup"><span data-stu-id="375e6-124">Remote procedure that is part of the client side of a distributed application, that a server can call to obtain information from the client.</span></span> <span data-ttu-id="375e6-125">\[[回呼](/windows/desktop/Midl/callback) \] 屬性會指定靜態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="375e6-125">The \[ [callback](/windows/desktop/Midl/callback)\] attribute designates a static callback function.</span></span>

</dd> <dt>

<span data-ttu-id="375e6-126"><span id="_rpc_static_identity_tracking_glos"></span><span id="_RPC_STATIC_IDENTITY_TRACKING_GLOS"></span>**靜態身分識別追蹤**</span><span class="sxs-lookup"><span data-stu-id="375e6-126"><span id="_rpc_static_identity_tracking_glos"></span><span id="_RPC_STATIC_IDENTITY_TRACKING_GLOS"></span>**static identity tracking**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-127">靜態身分識別追蹤指定 RPC 執行時間在用戶端的系結控制碼中，針對所有 RPC 呼叫使用安全性認證。</span><span class="sxs-lookup"><span data-stu-id="375e6-127">Static identity tracking specifies that the RPC run-time uses the security credentials in the client's binding handle for all RPC calls.</span></span> <span data-ttu-id="375e6-128">另請參閱 [*動態身分識別追蹤*](d-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="375e6-128">See also [*dynamic identity tracking*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="375e6-129"><span id="_rpc_string_binding_glos"></span><span id="_RPC_STRING_BINDING_GLOS"></span>**字串系結**</span><span class="sxs-lookup"><span data-stu-id="375e6-129"><span id="_rpc_string_binding_glos"></span><span id="_RPC_STRING_BINDING_GLOS"></span>**string binding**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-130">包含物件 [*UUID*](u-glos.md)、 [*通訊協定順序*](p-glos.md)、 [*網路位址*](n-glos.md)、 [*端點*](e-glos.md)和端點選項的字元字串，這些選項全都可用來建立指定之伺服器的系結 [*控制碼*](b-glos.md) 。</span><span class="sxs-lookup"><span data-stu-id="375e6-130">Character string that consists of the object [*UUID*](u-glos.md), [*protocol sequence*](p-glos.md), [*network address*](n-glos.md), [*endpoint*](e-glos.md), and endpoint options, all of which can be used to create a [*binding handle*](b-glos.md) to the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="375e6-131"><span id="_rpc_strong_typing_glos"></span><span id="_RPC_STRONG_TYPING_GLOS"></span>**強型別**</span><span class="sxs-lookup"><span data-stu-id="375e6-131"><span id="_rpc_strong_typing_glos"></span><span id="_RPC_STRONG_TYPING_GLOS"></span>**strong typing**</span></span>
</dt> <dd>

<span data-ttu-id="375e6-132">嚴格控制資料類型的編譯器強制執行。</span><span class="sxs-lookup"><span data-stu-id="375e6-132">Compiler enforcement of strict control over data types.</span></span> <span data-ttu-id="375e6-133">在 MIDL 和 RPC 中，強型別是用來確保分散式環境中的不同電腦都能一致地解讀資料。</span><span class="sxs-lookup"><span data-stu-id="375e6-133">In MIDL and RPC, strong typing is used to ensure that data is interpreted consistently by different computers in a distributed environment.</span></span>

</dd> </dl>

 

 
