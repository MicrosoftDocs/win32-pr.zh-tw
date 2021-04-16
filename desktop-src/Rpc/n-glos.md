---
title: 'N (RPC) '
description: 在遠端程序呼叫中，以 N 開頭的單字會 (RPC) 詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b004002f-ae52-4ae8-a570-19241bfcee51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547012dcbd9b1044c09d3f039b0a72946cb65bef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383606"
---
# <a name="n-rpc"></a><span data-ttu-id="d47f6-103">N (RPC) </span><span class="sxs-lookup"><span data-stu-id="d47f6-103">N (RPC)</span></span>

<span data-ttu-id="d47f6-104">[](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G [](u-glos.md) [](v-glos.md) H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) N [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d47f6-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) N [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d47f6-105"><span id="_rpc_name_service_glos"></span><span id="_RPC_NAME_SERVICE_GLOS"></span>**名稱服務**</span><span class="sxs-lookup"><span data-stu-id="d47f6-105"><span id="_rpc_name_service_glos"></span><span id="_RPC_NAME_SERVICE_GLOS"></span>**name service**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-106">此服務會將名稱對應至物件，並將名稱/物件組儲存在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="d47f6-106">Service that maps names to objects and stores the name/object pairs in a database.</span></span> <span data-ttu-id="d47f6-107">例如，RPC 名稱服務會將邏輯名稱對應至系結 [*控制碼*](b-glos.md) ，因此用戶端應用程式可以參考該邏輯名稱，而不是通訊協定順序和網路位址。</span><span class="sxs-lookup"><span data-stu-id="d47f6-107">For example, the RPC name service maps a logical name to a [*binding handle*](b-glos.md) so client applications can refer to that logical name, rather than a protocol sequence and network address.</span></span> <span data-ttu-id="d47f6-108">另請參閱名稱服務-介面 daemon ([nsid)](/windows)、用戶端目錄服務 ([*cd)*](c-glos.md)、 [*定位器*](l-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="d47f6-108">See also name service–interface daemon ([nsid)](/windows), Client Directory Service ([*CDS)*](c-glos.md), [*Locator*](l-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-109"><span id="_rpc_nca_glos"></span><span id="_RPC_NCA_GLOS"></span>**(NCA) 的網路運算架構**</span><span class="sxs-lookup"><span data-stu-id="d47f6-109"><span id="_rpc_nca_glos"></span><span id="_RPC_NCA_GLOS"></span>**Network Computing Architecture (NCA)**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-110">分散式運算的指導方針。</span><span class="sxs-lookup"><span data-stu-id="d47f6-110">Collection of guidelines for distributed computing.</span></span> <span data-ttu-id="d47f6-111">RPC 通訊協定會遵循這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="d47f6-111">The RPC communication protocols follow these guidelines.</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-112"><span id="_rpc_nsi_glos"></span><span id="_RPC_NSI_GLOS"></span>**名稱服務獨立 (NSI)**</span><span class="sxs-lookup"><span data-stu-id="d47f6-112"><span id="_rpc_nsi_glos"></span><span id="_RPC_NSI_GLOS"></span>**Name Service Independent (NSI)**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-113">API 函式的標準，可讓分散式應用程式透過各種名稱服務提供者（例如憑證-DCE Cell Directory 服務或 Microsoft 定位器）來存取 RPC 名稱服務資料庫元素。</span><span class="sxs-lookup"><span data-stu-id="d47f6-113">Standard for API functions that allows a distributed application to access RPC name-service database elements through various name-service providers, such as OSF-DCE Cell Directory Service or Microsoft Locator.</span></span> <span data-ttu-id="d47f6-114">另請參閱 [-介面 daemon](/windows) (nsid) 。</span><span class="sxs-lookup"><span data-stu-id="d47f6-114">See also [–interface daemon](/windows) (nsid).</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-115"><span id="_rpc_nsid_glos"></span><span id="_RPC_NSID_GLOS"></span>**名稱服務-介面 daemon (nsid)**</span><span class="sxs-lookup"><span data-stu-id="d47f6-115"><span id="_rpc_nsid_glos"></span><span id="_RPC_NSID_GLOS"></span>**name service–interface daemon (nsid)**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-116">提供 Microsoft [*定位器*](l-glos.md) 與憑證-DCE Cell Directory 服務名稱服務資料庫之間的介面的服務，以進行 RPC 名稱服務功能。</span><span class="sxs-lookup"><span data-stu-id="d47f6-116">Service that provides an interface between Microsoft [*Locator*](l-glos.md) and the OSF-DCE Cell Directory Service name service databases for RPC name-service functions.</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-117"><span id="_rpc_named_pipe_glos"></span><span id="_RPC_NAMED_PIPE_GLOS"></span>**具名管道**</span><span class="sxs-lookup"><span data-stu-id="d47f6-117"><span id="_rpc_named_pipe_glos"></span><span id="_RPC_NAMED_PIPE_GLOS"></span>**named pipe**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-118">以連接導向的通訊協定（以伺服器訊息區為基礎） (Smb) 和 [NetBIOS](/windows)，用於伺服器進程與一或多個用戶端進程之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="d47f6-118">Connection-oriented protocol, based on Server Message Blocks (SMBs) and [NetBIOS](/windows), used for communication between a server process and one or more client processes.</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-119"><span id="_rpc_netbeui_glos"></span><span id="_RPC_NETBEUI_GLOS"></span>**NetBIOS 延伸消費者介面 (NetBEUI)**</span><span class="sxs-lookup"><span data-stu-id="d47f6-119"><span id="_rpc_netbeui_glos"></span><span id="_RPC_NETBEUI_GLOS"></span>**NetBIOS Extended User Interface (NetBEUI)**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-120">LAN Manager 原生傳輸通訊協定和網路設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d47f6-120">LAN Manager native transport protocol and network device driver.</span></span> <span data-ttu-id="d47f6-121">另請參閱 [NetBIOS](/windows)。</span><span class="sxs-lookup"><span data-stu-id="d47f6-121">See also [NetBIOS](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-122"><span id="_rpc_netbios_glos"></span><span id="_RPC_NETBIOS_GLOS"></span>**網路基本輸入/輸出系統 (NetBIOS)**</span><span class="sxs-lookup"><span data-stu-id="d47f6-122"><span id="_rpc_netbios_glos"></span><span id="_RPC_NETBIOS_GLOS"></span>**Network Basic Input/Output System (NetBIOS)**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-123">Microsoft MS-DOS 作業系統、i/o 匯流排和局域網路之間的軟體介面。</span><span class="sxs-lookup"><span data-stu-id="d47f6-123">Software interface between the Microsoft MS-DOS operating system, the I/O bus, and a local area network.</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-124"><span id="_rpc_ndr_glos"></span><span id="_RPC_NDR_GLOS"></span>**(NDR) 的網路資料表示**</span><span class="sxs-lookup"><span data-stu-id="d47f6-124"><span id="_rpc_ndr_glos"></span><span id="_RPC_NDR_GLOS"></span>**Network Data Representation (NDR)**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-125">在網路傳輸期間使用的標準格式，與任何特定電腦架構上的資料類型格式無關。</span><span class="sxs-lookup"><span data-stu-id="d47f6-125">Standard format used during network transmission that is independent of the data-type format on any particular computer architecture.</span></span> <span data-ttu-id="d47f6-126">傳送的資料包含指定其 NDR 格式的資訊。</span><span class="sxs-lookup"><span data-stu-id="d47f6-126">Transmitted data includes information that specifies its NDR format.</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-127"><span id="_rpc_network_address_glos"></span><span id="_RPC_NETWORK_ADDRESS_GLOS"></span>**網路位址**</span><span class="sxs-lookup"><span data-stu-id="d47f6-127"><span id="_rpc_network_address_glos"></span><span id="_RPC_NETWORK_ADDRESS_GLOS"></span>**network address**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-128">識別網路上伺服器的位址。</span><span class="sxs-lookup"><span data-stu-id="d47f6-128">Address that identifies a server on a network.</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-129"><span id="_rpc_nonencapsulated_union_glos"></span><span id="_RPC_NONENCAPSULATED_UNION_GLOS"></span>**nonencapsulated 聯集**</span><span class="sxs-lookup"><span data-stu-id="d47f6-129"><span id="_rpc_nonencapsulated_union_glos"></span><span id="_RPC_NONENCAPSULATED_UNION_GLOS"></span>**nonencapsulated union**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-130">在判別和等位未緊密系結的情況之下，與封裝聯集較不嚴格的差異聯 [*集*](d-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="d47f6-130">[*Discriminated union*](d-glos.md) that is less restrictive than an encapsulated union in that the discriminant and the union are not tightly bound.</span></span> <span data-ttu-id="d47f6-131">如果 union 是參數，則判別是另一個參數;如果聯集是結構欄位，判別就是另一個結構欄位。</span><span class="sxs-lookup"><span data-stu-id="d47f6-131">If the union is a parameter, the discriminant is another parameter; if the union is a structure field, the discriminant is another structure field.</span></span> <span data-ttu-id="d47f6-132">IDL 關鍵字 \[ [**參數 \_ 是**](/windows/desktop/Midl/switch-is) \] ， \[ [**參數 \_ 類型**](/windows/desktop/Midl/switch-type)會 \] 識別判別及其類型。</span><span class="sxs-lookup"><span data-stu-id="d47f6-132">The IDL keywords \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] and \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] identify the discriminant and its type.</span></span> <span data-ttu-id="d47f6-133">另請參閱 [*封裝聯集*](e-glos.md)。</span><span class="sxs-lookup"><span data-stu-id="d47f6-133">See also [*encapsulated union*](e-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="d47f6-134"><span id="_rpc_nonidempotent_glos"></span><span id="_RPC_NONIDEMPOTENT_GLOS"></span>**nonidempotent**</span><span class="sxs-lookup"><span data-stu-id="d47f6-134"><span id="_rpc_nonidempotent_glos"></span><span id="_RPC_NONIDEMPOTENT_GLOS"></span>**nonidempotent**</span></span>
</dt> <dd>

<span data-ttu-id="d47f6-135">指出遠端程序呼叫無法執行一次以上的指標，因為它會傳回不同的值或變更狀態。</span><span class="sxs-lookup"><span data-stu-id="d47f6-135">Indicator that a remote procedure call cannot be executed more than once because it will return a different value or change a state.</span></span>

</dd> </dl>

 

 
