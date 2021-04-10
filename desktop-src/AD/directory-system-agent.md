---
title: 目錄服務代理程式
description: 目錄服務代理程式 (DSA) 是在每個網域控制站上執行的服務和進程集合，並提供資料存放區的存取權。
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- 目錄服務代理程式 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842095"
---
# <a name="directory-system-agent"></a><span data-ttu-id="fcd2d-104">目錄服務代理程式</span><span class="sxs-lookup"><span data-stu-id="fcd2d-104">Directory System Agent</span></span>

<span data-ttu-id="fcd2d-105">[*目錄服務代理程式*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) 是在每個網域控制站上執行的服務和進程集合，並提供資料存放區的存取權。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="fcd2d-106">資料存放區是位於硬碟的目錄資料的實體存放區。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="fcd2d-107">在 Active Directory Domain Services 中，DSA 是本機系統授權單位的一部分 (LSA) 子系統。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="fcd2d-108">用戶端會使用 DSA 所支援的下列其中一種機制來存取目錄：</span><span class="sxs-lookup"><span data-stu-id="fcd2d-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="fcd2d-109">LDAP 用戶端會使用輕量型目錄存取協定 (LDAP) 來連線至 DSA。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="fcd2d-110">Active Directory Domain Services 支援 rfc 3377 定義的 LDAP 3.0，以及由 RFC 1777 定義的 LDAP 2.0。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="fcd2d-111">Windows 用戶端會使用 LDAP 3.0 來連接到 DSA。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="fcd2d-112">MAPI 用戶端（例如 Microsoft Exchange Server）會使用 MAPI 遠端程序呼叫介面連接到 DSA。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="fcd2d-113">Active Directory Domain Services 的 Dsa 會彼此連接，以使用專屬的遠端程序呼叫介面來執行複寫。</span><span class="sxs-lookup"><span data-stu-id="fcd2d-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 