---
description: 本主題討論使用對等基礎結構時的特定安全性考慮。
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: 安全性考量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850887"
---
# <a name="security-considerations"></a><span data-ttu-id="46b1d-103">安全性考量</span><span class="sxs-lookup"><span data-stu-id="46b1d-103">Security Considerations</span></span>

<span data-ttu-id="46b1d-104">本主題討論使用對等基礎結構時的特定安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="46b1d-104">This topic discusses specific security considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="46b1d-105">當您使用對等基礎結構開發對等應用程式時，基於安全性考慮，您必須考慮目錄許可權、對等網路服務的來賓存取、資訊洩漏和安全性服務提供者的實施。</span><span class="sxs-lookup"><span data-stu-id="46b1d-105">When you develop a peer application using the Peer Infrastructure, for security reasons you must consider directory permissions, guest access to peer networking services, information disclosure, and Security Service Provider Implementation.</span></span>

## <a name="directory-permissions"></a><span data-ttu-id="46b1d-106">目錄許可權</span><span class="sxs-lookup"><span data-stu-id="46b1d-106">Directory Permissions</span></span>

<span data-ttu-id="46b1d-107">對等網路服務會將資料儲存在使用者的使用者設定檔目錄樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="46b1d-107">Peer-to-peer networking services store data in the user profile directory tree of a user.</span></span> <span data-ttu-id="46b1d-108">使用者必須在設定檔的 **應用程式資料** 子樹中具有寫入權限。</span><span class="sxs-lookup"><span data-stu-id="46b1d-108">A user must have write permissions in the **application data** subtree of the profile.</span></span> <span data-ttu-id="46b1d-109">根據預設，此存取控制清單 (ACL) 設定正確，但使用者可以手動變更。</span><span class="sxs-lookup"><span data-stu-id="46b1d-109">By default, this access control list (ACL) is set correctly, but a user can change it manually.</span></span>

## <a name="guest-access-to-peer-networking-services"></a><span data-ttu-id="46b1d-110">對等網路服務的來賓存取</span><span class="sxs-lookup"><span data-stu-id="46b1d-110">Guest Access to Peer Networking Services</span></span>

<span data-ttu-id="46b1d-111">來賓帳戶和 **來賓** Windows 安全性群組的成員無法存取大部分的對等服務。</span><span class="sxs-lookup"><span data-stu-id="46b1d-111">A Guest account and members of the **Guests** Windows Security Group do not have access to most peer services.</span></span> <span data-ttu-id="46b1d-112">應用程式應該具有本機使用者存取權或更高的許可權。</span><span class="sxs-lookup"><span data-stu-id="46b1d-112">Applications should have local user access or higher.</span></span>

## <a name="information-disclosure"></a><span data-ttu-id="46b1d-113">資訊洩露</span><span class="sxs-lookup"><span data-stu-id="46b1d-113">Information Disclosure</span></span>

<span data-ttu-id="46b1d-114">資訊洩漏牽涉到位址、資料庫，以及身分識別和群組認證。</span><span class="sxs-lookup"><span data-stu-id="46b1d-114">Information disclosure involves address, database, and identity and group credentials.</span></span> <span data-ttu-id="46b1d-115">下列各節會識別並定義資訊洩漏。</span><span class="sxs-lookup"><span data-stu-id="46b1d-115">The following sections identify and define the information disclosure.</span></span>

<span data-ttu-id="46b1d-116">**位址洩漏** 對等名稱解析通訊協定 (PNRP) 是一種識別碼解析服務，可將對等名稱識別碼解析為 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="46b1d-116">**Address Disclosure** Peer Name Resolution Protocol (PNRP) is an identifier resolution service that allows a peer name identifier to be resolved into an IP address.</span></span> <span data-ttu-id="46b1d-117">與 DNS 類似，PNRP 會發佈 IP 位址，讓知道對應識別碼的使用者可以將它解析成該位址。</span><span class="sxs-lookup"><span data-stu-id="46b1d-117">Similar to DNS, PNRP publishes an IP address so that users who know the corresponding identifier can resolve it to that address.</span></span>

-   <span data-ttu-id="46b1d-118">在 PNRP 中發佈識別碼，表示任何使用者都可以將識別碼解析為已發佈的 IP 位址，並判斷發行身分識別之 PNRP 服務的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="46b1d-118">Publishing an identifier in PNRP means any user can resolve the identifier to the published IP address, and determine the IP address of the PNRP service that published the identity.</span></span>
-   <span data-ttu-id="46b1d-119">對等群組基礎結構會自動發佈 PNRP 中本機群組實例的對等組名。</span><span class="sxs-lookup"><span data-stu-id="46b1d-119">The Peer Grouping Infrastructure automatically publishes the peer group name of the local group instance in PNRP.</span></span> <span data-ttu-id="46b1d-120">連線至對等群組時，任何知道群組對等名稱的人都可以解析使用中成員的位址，並知道每位使用者的目前位址。</span><span class="sxs-lookup"><span data-stu-id="46b1d-120">While connected to a peer group, anyone who knows the peer name for the group can resolve the addresses of active members, and knows the current address of each user.</span></span>

<span data-ttu-id="46b1d-121">使用者在登入時連接至其他對等群組成員或對等圖形節點的能力，是對等網路的主要功能。</span><span class="sxs-lookup"><span data-stu-id="46b1d-121">The ability of a user to connect to other peer group members or peer graph nodes while logged on is a primary feature of peer networking.</span></span> <span data-ttu-id="46b1d-122">連線至對等群組或圖形時，使用者的目前 IP 位址可在對等群組或圖形內的目前狀態記錄中發行。</span><span class="sxs-lookup"><span data-stu-id="46b1d-122">While connected to a peer group or graph, the current IP address of a user can be published in a presence record within the peer group or graph.</span></span> <span data-ttu-id="46b1d-123">依預設，參與該對等群組或圖形的任何人都可以列舉群組或圖形的成員，並判斷成員的目前位址。</span><span class="sxs-lookup"><span data-stu-id="46b1d-123">By default, anyone participating in that peer group or graph can enumerate members of the group or graph, and determine the current addresses of the members.</span></span> <span data-ttu-id="46b1d-124">這項功能是可設定的對等群組和對等圖形屬性。</span><span class="sxs-lookup"><span data-stu-id="46b1d-124">This ability is a configurable Peer Grouping and Peer Graphing property.</span></span>

<span data-ttu-id="46b1d-125">**資料庫洩漏** 對等群組和圖形基礎結構記錄資料庫會儲存在本機檔案系統上。</span><span class="sxs-lookup"><span data-stu-id="46b1d-125">**Database Disclosure** The Peer Grouping and Graphing Infrastructures record databases are stored on the local file system.</span></span> <span data-ttu-id="46b1d-126">任何具有本機檔案系統系統管理存取權的 Windows 使用者 (例如本機系統管理員) ，理論上可以存取本機對等圖形或群組資料庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="46b1d-126">Any Windows user with administrative access to the local file system (such as a local administrator) can theoretically access the data in the local peer graph or group database.</span></span> <span data-ttu-id="46b1d-127">這與本機系統管理員在本機電腦上存取任何資料的能力一致。</span><span class="sxs-lookup"><span data-stu-id="46b1d-127">This is consistent with the ability of local administrators to access any data on the local computer.</span></span>

<span data-ttu-id="46b1d-128">**身分識別和群組認證洩漏** 點對點群組需要成員彼此建立連接，以使用修改的 x.509 憑證鏈進行驗證。</span><span class="sxs-lookup"><span data-stu-id="46b1d-128">**Identity and Group Credentials Disclosure** Peer-to-peer grouping requires that members establish connections with each other to authenticate using modified X.509 certificate chains.</span></span> <span data-ttu-id="46b1d-129">在驗證過程中，會交換每個成員對應的身分識別和群組成員資格憑證 (GMC) 鏈。</span><span class="sxs-lookup"><span data-stu-id="46b1d-129">As part of authentication, each member's corresponding identity and Group Membership Certificate (GMC) chains are exchanged.</span></span>

<span data-ttu-id="46b1d-130">當連接到對等群組時，對等群組基礎結構會使用 PNRP 發佈群組對等名稱。</span><span class="sxs-lookup"><span data-stu-id="46b1d-130">While connected to a peer group, the Peer Grouping Infrastructure publishes the group peer name with PNRP.</span></span> <span data-ttu-id="46b1d-131">作為一般 PNRP 作業的一部分，可以將該群組的 GMC 鏈提供給其他 PNRP 實例，以證明發行群組對等名稱的授權。</span><span class="sxs-lookup"><span data-stu-id="46b1d-131">As part of the normal PNRP operation, the GMC chain for that group can be provided to other PNRP instances to prove authorization to publish the group peer name.</span></span>

## <a name="security-service-provider-implementation"></a><span data-ttu-id="46b1d-132">安全性服務提供者的執行</span><span class="sxs-lookup"><span data-stu-id="46b1d-132">Security Service Provider Implementation</span></span>

<span data-ttu-id="46b1d-133">對等圖形基礎結構的安全性與應用程式開發人員所實行的安全性服務提供者 (SSP) 一樣安全。</span><span class="sxs-lookup"><span data-stu-id="46b1d-133">The Peer Graphing Infrastructure is as secure as the Security Service Provider (SSP) that the application developer implements.</span></span> <span data-ttu-id="46b1d-134">SSP 愈強，對等圖形應用程式的安全性就愈強。</span><span class="sxs-lookup"><span data-stu-id="46b1d-134">The stronger the SSP, the stronger the security of the Peer Graphing application.</span></span>

 

 



