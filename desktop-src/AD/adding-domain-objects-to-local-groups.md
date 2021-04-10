---
title: 將網域物件新增至本機群組
description: 屬於網域的使用者和群組可以新增至本機電腦上的群組，以將許可權授與該特定電腦上的網域使用者或群組。
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，將網域物件新增至本機群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e956d1cf076f4c33c46700e52798463b7e1d2c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681698"
---
# <a name="adding-domain-objects-to-local-groups"></a><span data-ttu-id="a9ddd-104">將網域物件新增至本機群組</span><span class="sxs-lookup"><span data-stu-id="a9ddd-104">Adding Domain Objects to Local Groups</span></span>

<span data-ttu-id="a9ddd-105">當成員伺服器或在 Windows 2000 Professional 上執行的電腦是 Windows 2000 網域的成員時，屬於該網域的使用者和群組可以新增至本機電腦上的群組，以授與該特定電腦上網域使用者或群組的許可權。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-105">When a member server or a computer running on Windows 2000 Professional is a member of a Windows 2000 domain, the users and groups that belong to the domain can be added to groups on the local computer to grant rights to the domain user or group on that particular computer.</span></span>

<span data-ttu-id="a9ddd-106">使用 ADSI 管理 Windows 2000 網域上的網域本機群組時，通常會使用 LDAP 提供者。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-106">When managing domain local groups on a Windows 2000 domain using ADSI, the LDAP provider is normally used.</span></span> <span data-ttu-id="a9ddd-107">不過，在成員伺服器上管理本機群組和執行 Windows 2000 Professional 的電腦時，必須使用 WinNT 提供者。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-107">When managing local groups on member servers and a computer running Windows 2000 Professional, however, the WinNT provider must be used.</span></span>

<span data-ttu-id="a9ddd-108">只有本機群組可以在成員伺服器和 Windows 2000 Professional 上建立。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-108">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="a9ddd-109">不過，本機群組可包含：</span><span class="sxs-lookup"><span data-stu-id="a9ddd-109">However, the local groups can contain:</span></span>

-   <span data-ttu-id="a9ddd-110">樹系中的通用和全域群組，其中包含電腦所屬的網域。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-110">Universal and global groups from the forest that contains the domain that the computer is a member.</span></span>
-   <span data-ttu-id="a9ddd-111">來自該電腦網域的網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-111">Domain local groups from that computer domain.</span></span>
-   <span data-ttu-id="a9ddd-112">樹系中任何網域的使用者。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-112">Users from any domain in the forest.</span></span>

<span data-ttu-id="a9ddd-113">**將網域物件新增至本機群組**</span><span class="sxs-lookup"><span data-stu-id="a9ddd-113">**To add a domain object to a local group**</span></span>

1.  <span data-ttu-id="a9ddd-114">系結至電腦的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面，其中包含要新增成員的本機群組。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the computer that contains the local group to add a member to.</span></span> <span data-ttu-id="a9ddd-115">系結必須使用具有足夠許可權的帳戶來執行，才能存取該電腦。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-115">The binding must be performed using an account that has sufficient rights to access that computer.</span></span> <span data-ttu-id="a9ddd-116">系結字串的格式必須是 "WinNT:// <computer name> ，computer"，其中 " &lt; computer name &gt; " 是要新增成員的電腦群組名。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-116">The binding string must take the form "WinNT://<computer name>,computer" where "&lt;computer name&gt;" is the name of the computer group to add a member to.</span></span> <span data-ttu-id="a9ddd-117">"，Computer" 參數會指示 ADSI 系結至電腦。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-117">The ",computer" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="a9ddd-118">ADSI 會將此資料公開給 WinNT 提供者的剖析器，讓它可以略過一些明確的解析查詢，以判斷您要系結到的物件類型。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-118">ADSI exposes this data to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span> <span data-ttu-id="a9ddd-119">這可以讓使用者有5到20秒的時間來解決不明確的問題。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-119">This can save the user a 5 to 20 second wait for the ambiguity to be resolved.</span></span>
2.  <span data-ttu-id="a9ddd-120">使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) 做為類別的 "group"，並使用本機群組名稱作為要系結至群組的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-120">Use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method with "group" as the class and the local group name as the name of the object to bind to the group.</span></span>
3.  <span data-ttu-id="a9ddd-121">系結至將加入成員之本機群組的 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 介面。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-121">Bind to the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the local group to which a member will be added.</span></span>
4.  <span data-ttu-id="a9ddd-122">以 "WinNT://" 形式來建立要新增至本機群組之物件的 ADsPath <domain> / <name> ，其中 " &lt; domain &gt; " 是包含要加入之物件的功能變數名稱，而 " &lt; name &gt; " 是要加入之物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-122">Construct the ADsPath of the object to add to the local group in the form "WinNT://<domain>/<name>", where "&lt;domain&gt;" is the name of the domain that contains the object to add and "&lt;name&gt;" is the name of the object to add.</span></span>
5.  <span data-ttu-id="a9ddd-123">使用 [**IADsGroup**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) 將使用者或群組新增至本機群組，並傳遞在步驟4中所建立的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-123">Add the user or group to the local group with the [**IADsGroup.Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method, passing the ADsPath constructed in Step 4.</span></span>

<span data-ttu-id="a9ddd-124">如需詳細資訊和示範如何將網域使用者或群組物件新增到本機群組的程式碼範例，請參閱 [將網域使用者或群組新增至本機群組的範例程式碼](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md)。</span><span class="sxs-lookup"><span data-stu-id="a9ddd-124">For more information and a code example that shows how to add a domain user or group object to a local group, see [Example Code for Adding a Domain User or Group to a Local Group](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md).</span></span>

 

 