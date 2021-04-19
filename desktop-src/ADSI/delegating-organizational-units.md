---
title: 委派組織單位
description: Fabrikam 公司雇用兩位系統管理員（Mike 和 Paul），分別管理東部和西部組織單位。
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "107001061"
---
# <a name="delegating-organizational-units"></a><span data-ttu-id="551f8-103">委派組織單位</span><span class="sxs-lookup"><span data-stu-id="551f8-103">Delegating Organizational Units</span></span>

<span data-ttu-id="551f8-104">Fabrikam 公司雇用兩位系統管理員（Mike 和 Paul），分別管理東部和西部組織單位。</span><span class="sxs-lookup"><span data-stu-id="551f8-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="551f8-105">Joe 將他的管理責任委派給他們，讓他們可以在各自的組織單位中建立和刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="551f8-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="551f8-106">在瞭解如何在 Mike 和 Paul 下設定這些組織單位之前，您必須瞭解如何在 Active Directory 中設定物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="551f8-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="551f8-107">Active Directory 中的每個物件都有安全描述項。</span><span class="sxs-lookup"><span data-stu-id="551f8-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="551f8-108">有了安全描述項，您就可以修改物件的許可權、傳播許可權、啟用審核等等。</span><span class="sxs-lookup"><span data-stu-id="551f8-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="551f8-109">安全描述項本身有兩個存取控制清單 (Acl) ：任意 ACL (DACL) 和系統 ACL (SACL) 。</span><span class="sxs-lookup"><span data-stu-id="551f8-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="551f8-110">每個 ACL 可以包含 (Ace) 的存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="551f8-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="551f8-111">您可以使用 ACE 來設定物件的允許或拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="551f8-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="551f8-112">此外，您可以指定要允許或拒絕的特定動作。</span><span class="sxs-lookup"><span data-stu-id="551f8-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="551f8-113">動作範例包括「建立子系」、「刪除子系」、「讀取屬性」和「寫入」屬性。</span><span class="sxs-lookup"><span data-stu-id="551f8-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="551f8-114">這些許可權是使用 [**AccessMask**](iadsaccesscontrolentry-property-methods.md)指定的。</span><span class="sxs-lookup"><span data-stu-id="551f8-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="551f8-115">接著，您可以指定與此 ACE 相關聯的類別或屬性。</span><span class="sxs-lookup"><span data-stu-id="551f8-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="551f8-116">在接下來的 Fabrikam 範例中，Joe 挑選使用者類別，讓每位系統管理員可以將使用者新增至系統。</span><span class="sxs-lookup"><span data-stu-id="551f8-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="551f8-117">接下來，您必須回答下列問題：「誰將是此 ACE 的受益人？」</span><span class="sxs-lookup"><span data-stu-id="551f8-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="551f8-118">Joe 將指定 Mike。</span><span class="sxs-lookup"><span data-stu-id="551f8-118">Joe will specify Mike.</span></span>

<span data-ttu-id="551f8-119">最後，您可以設定 ACE 繼承行為，例如，您可以指定 Ace 來向下傳播階層。</span><span class="sxs-lookup"><span data-stu-id="551f8-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="551f8-120">總而言之，上述範例將會導致 Mike 能夠在東部銷售組織單位下建立和刪除使用者物件。</span><span class="sxs-lookup"><span data-stu-id="551f8-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="551f8-121">Joe 使用下列程式碼範例，在東部組織單位上設定 Ace 和 Acl。</span><span class="sxs-lookup"><span data-stu-id="551f8-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



<span data-ttu-id="551f8-122">下圖顯示在程式碼執行之後 Active Directory **建立新的視圖** 功能表。</span><span class="sxs-lookup"><span data-stu-id="551f8-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="551f8-123">當 Joe （系統管理員）登入時，他看到了數個可以建立的類別。</span><span class="sxs-lookup"><span data-stu-id="551f8-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="551f8-124">不過，當 Mike 登入時，他只能夠建立使用者物件。</span><span class="sxs-lookup"><span data-stu-id="551f8-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![建立新的視圖選項功能表](images/adadsi5.png)

<span data-ttu-id="551f8-126">如需詳細資訊，請參閱 [ADSI 安全性模型](adsi-security-model.md)。</span><span class="sxs-lookup"><span data-stu-id="551f8-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 




