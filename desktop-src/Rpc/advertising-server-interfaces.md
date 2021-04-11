---
title: 廣告伺服器介面
description: 使用自動控制碼的應用程式的伺服器端必須呼叫函式 RpcNsBindingExport，以將伺服器的相關系結資訊提供給用戶端使用。
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021495"
---
# <a name="advertising-server-interfaces"></a><span data-ttu-id="3a937-103">廣告伺服器介面</span><span class="sxs-lookup"><span data-stu-id="3a937-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="3a937-104">使用自動控制碼的應用程式的伺服器端必須呼叫函式 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) ，以將伺服器的相關系結資訊提供給用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="3a937-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="3a937-105">自動系結控制碼需要在可供用戶端存取的伺服器上執行名稱服務。</span><span class="sxs-lookup"><span data-stu-id="3a937-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="3a937-106">Microsoft 的名稱服務（Microsoft 定位器）的實作為管理自動控點。</span><span class="sxs-lookup"><span data-stu-id="3a937-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="3a937-107">使用隱含和明確系結控制碼的伺服器應用程式，也可以在名稱服務資料庫中通告其存在。</span><span class="sxs-lookup"><span data-stu-id="3a937-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="3a937-108">一般來說，伺服器會呼叫下列執行時間函數：</span><span class="sxs-lookup"><span data-stu-id="3a937-108">Typically, the server calls the following run-time functions:</span></span>

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

<span data-ttu-id="3a937-109">呼叫此程式碼片段中的前兩個函式，類似于 [Hello，World 範例](tutorial.md)。</span><span class="sxs-lookup"><span data-stu-id="3a937-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="3a937-110">這些函式會將可用系結的相關資訊提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="3a937-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="3a937-111">[**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)和 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)的呼叫會將資訊放入名稱服務資料庫中。</span><span class="sxs-lookup"><span data-stu-id="3a937-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="3a937-112">在將控制碼匯出至名稱服務之前，對 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 的呼叫會以有效的系結控制碼填滿系結向量。</span><span class="sxs-lookup"><span data-stu-id="3a937-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="3a937-113">在伺服器程式將控制碼匯出至資料庫之後，用戶端 (或用戶端存根) 可以呼叫 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) 和 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) 來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="3a937-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="3a937-114">如需詳細資訊，請參閱 [尋找伺服器主機系統](finding-server-host-systems.md)。</span><span class="sxs-lookup"><span data-stu-id="3a937-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="3a937-115">[**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)和 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)的呼叫和其相關聯的資料結構看起來會像下面這樣：</span><span class="sxs-lookup"><span data-stu-id="3a937-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

<span data-ttu-id="3a937-116">請注意， [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 參數 *PBindingVector* 是指向 RPC 系結 [**\_ \_ 向量**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="3a937-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="3a937-117">也請記住，每次呼叫 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) 時，都必須接著呼叫 [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)。</span><span class="sxs-lookup"><span data-stu-id="3a937-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="3a937-118">若要從名稱服務資料庫中移除匯出的介面，伺服器會呼叫 [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3a937-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="3a937-119">只有在永久移除服務時，才應該使用 [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) 函數。</span><span class="sxs-lookup"><span data-stu-id="3a937-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="3a937-120">暫時停用服務時，不應使用此服務，例如當伺服器關閉進行維護時。</span><span class="sxs-lookup"><span data-stu-id="3a937-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="3a937-121">伺服器程式可以向名稱服務資料庫登錄，但因為伺服器暫時離線，所以無法使用。</span><span class="sxs-lookup"><span data-stu-id="3a937-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="3a937-122">用戶端應用程式應包含這類條件的例外狀況處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="3a937-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="3a937-123">如需名稱服務資料庫的內容和格式的詳細資訊，請參閱 [RPC 名稱服務資料庫](the-rpc-name-service-database.md)。</span><span class="sxs-lookup"><span data-stu-id="3a937-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="3a937-124">如果用戶端和伺服器程式都是在 Windows 2000 下執行，應用程式就可以利用 Active Directory 服務。</span><span class="sxs-lookup"><span data-stu-id="3a937-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="3a937-125">執行用戶端和伺服器程式的電腦必須是 Windows 2000 網域的成員。</span><span class="sxs-lookup"><span data-stu-id="3a937-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="3a937-126">若要使用 Active Directory 服務通告其存在，伺服器程式應在網域系統管理員的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="3a937-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="3a937-127">如果它是在網域使用者的內容中執行，則網域系統管理員必須修改 RPC 服務容器 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="3a937-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="3a937-128">如需詳細資訊，請參閱 Active Directory 檔。</span><span class="sxs-lookup"><span data-stu-id="3a937-128">For more information, see the Active Directory documentation.</span></span>

 

 




