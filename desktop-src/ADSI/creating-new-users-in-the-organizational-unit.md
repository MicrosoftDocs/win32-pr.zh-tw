---
title: 在組織單位中建立新的使用者
description: Terry Adams 是雇用 Fabrikam 銷售組織。 他的直接報告是一 Hines 的派翠克。
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- 在組織單位中建立新的使用者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461989"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="6b6d2-105">在組織單位中建立新的使用者</span><span class="sxs-lookup"><span data-stu-id="6b6d2-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="6b6d2-106">Terry Adams 是雇用 Fabrikam 銷售組織。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="6b6d2-107">他的直接報告是一 Hines 的派翠克。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="6b6d2-108">如下列程式碼範例所示，Joe Andreshak 企業系統管理員會為他建立新的帳戶。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="6b6d2-109">建立新的使用者時，您必須指定 **sAMAccountName**。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="6b6d2-110">這是使用者類別的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="6b6d2-111">在可以建立物件的實例之前，必須先設定所有必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="6b6d2-112">如果未指定新使用者的 SAMAccountName，則會自動產生 **sAMAccountName** 。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="6b6d2-113">建立新的使用者時，必須先在本機快取中設定所有必要的屬性，然後再呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="6b6d2-114">Joe 是系統管理員，可以使用 [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) 方法指派 Terry 的密碼。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="6b6d2-115">在呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)方法之前， **IADsUser. SetPassword** 方法將無法運作。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="6b6d2-116">然後，Joe 將 [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) 屬性設定為 **FALSE**，以啟用使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="6b6d2-117">下列程式碼範例示範如何將 Terry 設定為派翠克的經理。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="6b6d2-118">您可能會想要知道 Terry 變更他的姓名、移至不同的組織或離開公司時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="6b6d2-119">誰負責維護此管理員-直接報告連結？</span><span class="sxs-lookup"><span data-stu-id="6b6d2-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="6b6d2-120">如需詳細資訊，以及此問題的解決方法，請參閱 [重組](reorganization.md)。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="6b6d2-121">因為 Active Directory 架構是可擴充的，所以您可以建立物件的模型，以包含類似的管理員直接報表樣式關聯性。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="6b6d2-122">在繼續進行下一項工作之前，請先查看程式碼範例，其中顯示 Joe 如何審視 Terry 的直屬員工。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="6b6d2-123">在此程式碼範例中，即使從未修改過 **directReports** 屬性，還是會顯示 Terry 的直接報表。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="6b6d2-124">Active Directory 會自動執行此功能。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="6b6d2-125">在目錄世界中，屬性可以有單一或多個值。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="6b6d2-126">因為 **directReports** 有多個值，所以您可以藉由查看架構來取得這項資訊，因此使用 [**IADs GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) 方法會比較容易，因為它會傳回值的陣列，而不論是否傳回單一或多個值。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="6b6d2-127">Active Directory 消費者和電腦嵌入式管理單元可讓您在使用者的 [屬性] 頁面上，查看直接報表和管理員關聯性。</span><span class="sxs-lookup"><span data-stu-id="6b6d2-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b6d2-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b6d2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b6d2-129">將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="6b6d2-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 




