---
title: 建立新群組
description: Joe Worden，企業系統管理員必須建立新的群組。
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933619"
---
# <a name="creating-a-new-group"></a><span data-ttu-id="2dcaa-103">建立新群組</span><span class="sxs-lookup"><span data-stu-id="2dcaa-103">Creating a New Group</span></span>

<span data-ttu-id="2dcaa-104">Joe Worden，企業系統管理員必須建立新的群組。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="2dcaa-105">他想要根據此群組的成員資格來保護某些資源，例如檔案、Active Directory 物件或其他物件。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="2dcaa-106">下列程式碼範例顯示如何建立新的群組。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="2dcaa-107">此群組管理將會在銷售組織單位中建立。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="2dcaa-108">首先，Joe 必須建立 Sales 組織單位的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="2dcaa-109">其次，他必須在這個物件上設定 [**samAccountName**](/windows/desktop/AD/group-objects) 屬性，因為它是回溯相容性的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="2dcaa-110">在此範例中，當已設定 **samAccountName** 時，Windows NT 4.0 工具（例如使用者管理員）會將 **屬性視為管理** 而非 **管理**。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="2dcaa-111">第三，Joe 必須指定群組的類型。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="2dcaa-112">在 Windows 2000 網域中，有三種類型的群組：全域、網域本機和通用。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="2dcaa-113">此外，群組也會攜帶其安全性特性。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="2dcaa-114">群組可以是啟用安全性或不安全的群組。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="2dcaa-115">基本上，啟用安全性的群組就是可授與或拒絕資源存取權的群組，類似于使用者。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="2dcaa-116">例如，將檔案共用的存取權授與群組，即表示該群組的所有成員都可以存取檔案共用。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="2dcaa-117">通訊群組清單無法以類似的方式使用，例如，您無法授與通訊群組清單存取檔案共用的許可權。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="2dcaa-118">升級期間，會將 Windows NT 4.0 群組遷移為啟用安全性的群組。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="2dcaa-119">Active Directory 中的不安全群組與 Exchange 中的通訊群組清單類似。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="2dcaa-120">因此，建立群組或通訊群組清單與 Windows 2000 中的作業類似。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="2dcaa-121">在 Windows 2000 原生模式 (原生模式中，表示網域中的所有網域控制站都是執行 Windows 2000 Server) 的電腦，這些群組可以嵌套到任何層級。</span><span class="sxs-lookup"><span data-stu-id="2dcaa-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dcaa-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="2dcaa-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dcaa-123">列舉物件</span><span class="sxs-lookup"><span data-stu-id="2dcaa-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 