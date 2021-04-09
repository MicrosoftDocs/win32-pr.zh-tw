---
title: 'SNMP 管理資訊基礎 (MIB) '
description: 管理資訊基底 (MIB) 描述一組受管理的物件。 SNMP 管理主控台應用程式可以操控特定電腦上的物件（如果 SNMP 服務具有支援 MIB 的擴充代理程式 DLL）。
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672084"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="263df-104">SNMP 管理資訊基礎 (MIB) </span><span class="sxs-lookup"><span data-stu-id="263df-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="263df-105">管理資訊基底 (MIB) 描述一組受管理的物件。</span><span class="sxs-lookup"><span data-stu-id="263df-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="263df-106">SNMP 管理主控台應用程式可以操控特定電腦上的物件（如果 SNMP 服務具有支援 MIB 的擴充代理程式 DLL）。</span><span class="sxs-lookup"><span data-stu-id="263df-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="263df-107">MIB 中的每個受管理物件都有唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="263df-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="263df-108">識別碼包含物件的類型 (例如計數器、string、量測計或位址) 、物件的存取層級 (例如讀取或讀取/寫入) 、大小限制和範圍資訊。</span><span class="sxs-lookup"><span data-stu-id="263df-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="263df-109">下表包含系統隨附的 Mib 部分清單。</span><span class="sxs-lookup"><span data-stu-id="263df-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="263df-110">它們會與 SNMP 服務一起安裝在% systemroot% \\ system32 目錄中。</span><span class="sxs-lookup"><span data-stu-id="263df-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="263df-111">如需 Mib 的完整清單，請參閱 Windows 資源套件。</span><span class="sxs-lookup"><span data-stu-id="263df-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="263df-112">MIB</span><span class="sxs-lookup"><span data-stu-id="263df-112">MIB</span></span>         | <span data-ttu-id="263df-113">Description</span><span class="sxs-lookup"><span data-stu-id="263df-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="263df-114">Dhcp。Mib</span><span class="sxs-lookup"><span data-stu-id="263df-114">DHCP.MIB</span></span>    | <span data-ttu-id="263df-115">包含物件類型的 Microsoft 定義 MIB，可監視遠端主機與 DHCP 伺服器之間的網路流量</span><span class="sxs-lookup"><span data-stu-id="263df-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="263df-116">HOSTMIB.Mib</span><span class="sxs-lookup"><span data-stu-id="263df-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="263df-117">包含用於監視和管理主機資源的物件類型</span><span class="sxs-lookup"><span data-stu-id="263df-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="263df-118">LMMIB2.Mib</span><span class="sxs-lookup"><span data-stu-id="263df-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="263df-119">涵蓋工作站和伺服器服務</span><span class="sxs-lookup"><span data-stu-id="263df-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="263df-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="263df-120">MIB\_II.MIB</span></span> | <span data-ttu-id="263df-121">包含 Management Information Base (MIB-II) ，其提供簡單、可運作的架構和系統來管理以 TCP/IP 為基礎的網際網路</span><span class="sxs-lookup"><span data-stu-id="263df-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="263df-122">贏。Mib</span><span class="sxs-lookup"><span data-stu-id="263df-122">WINS.MIB</span></span>    | <span data-ttu-id="263df-123">Windows 網際網路名稱服務的 Microsoft 定義 MIB (WINS) </span><span class="sxs-lookup"><span data-stu-id="263df-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="263df-124">**Windows NT：** 一般而言，您可以從支援特定 MIB 的 SNMP 延伸模組代理程式複製 MIB。</span><span class="sxs-lookup"><span data-stu-id="263df-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="263df-125">Windows NT 4.0 資源套件提供一些額外的 Mib。</span><span class="sxs-lookup"><span data-stu-id="263df-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="263df-126">適用于 MIB 的擴充代理程式 Dll、LAN Manager MIB-II 和主機資源 MIB 會與 SNMP 服務一起安裝。</span><span class="sxs-lookup"><span data-stu-id="263df-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="263df-127">當安裝其他 Mib 的擴充代理程式 Dll 時，會安裝其個別的服務。</span><span class="sxs-lookup"><span data-stu-id="263df-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="263df-128">在服務啟動時，SNMP 服務會載入登錄中列出的所有擴充代理程式 Dll。</span><span class="sxs-lookup"><span data-stu-id="263df-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="263df-129">使用者可以新增其他擴充代理程式 Dll 來執行額外的 Mib。</span><span class="sxs-lookup"><span data-stu-id="263df-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="263df-130">若要這樣做，他們必須為 SNMP 服務下的新 DLL 新增登錄專案。</span><span class="sxs-lookup"><span data-stu-id="263df-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="263df-131">他們也必須向 SNMP 管理主控台應用程式註冊新的 MIB。</span><span class="sxs-lookup"><span data-stu-id="263df-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="263df-132">如需詳細資訊，請參閱管理主控台應用程式隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="263df-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="263df-133">如需詳細資訊，請參閱 [MIB 名稱樹狀目錄](mib-name-tree.md)。</span><span class="sxs-lookup"><span data-stu-id="263df-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 




