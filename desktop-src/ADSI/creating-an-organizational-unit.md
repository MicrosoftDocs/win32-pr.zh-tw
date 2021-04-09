---
title: 建立組織單位
description: 現在您已有網域物件，可以開始建立組織單位。
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- 建立組織單位 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931849"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="1d99b-104">建立組織單位</span><span class="sxs-lookup"><span data-stu-id="1d99b-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="1d99b-105">現在您已有網域物件，可以開始建立組織單位。</span><span class="sxs-lookup"><span data-stu-id="1d99b-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="1d99b-106">Fabrikam 有兩個部門：銷售和生產。</span><span class="sxs-lookup"><span data-stu-id="1d99b-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="1d99b-107">公司計畫雇用兩部 Windows 2000 系統管理員來管理每個部門。</span><span class="sxs-lookup"><span data-stu-id="1d99b-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="1d99b-108">Joe Worden 是企業系統管理員，將在 Fabrikam 網域下建立兩個新的組織單位。</span><span class="sxs-lookup"><span data-stu-id="1d99b-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="1d99b-109">藉由建立組織單位，Joe 可以將多個物件群組在一起，讓其他人管理這些物件。</span><span class="sxs-lookup"><span data-stu-id="1d99b-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="1d99b-110">下列程式碼範例會建立 (OU) 的銷售組織單位。</span><span class="sxs-lookup"><span data-stu-id="1d99b-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="1d99b-111">[**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)方法會接受類別名稱和新物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d99b-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="1d99b-112">此時不會將物件認可至 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="1d99b-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="1d99b-113">不過，您在用戶端上將會有 ADSI/COM 物件參考。</span><span class="sxs-lookup"><span data-stu-id="1d99b-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="1d99b-114">使用這個 ADSI 物件，您可以使用 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-put) 方法來設定或修改屬性。</span><span class="sxs-lookup"><span data-stu-id="1d99b-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="1d99b-115">**IADs** 方法會接受屬性名稱和屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1d99b-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="1d99b-116">但是，不會對目錄認可任何內容;所有專案都會在用戶端快取。</span><span class="sxs-lookup"><span data-stu-id="1d99b-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="1d99b-117">當您呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法時，就會將變更（在此案例中為物件建立和屬性修改）認可至目錄。</span><span class="sxs-lookup"><span data-stu-id="1d99b-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="1d99b-118">這些變更都是交易的，也就是說，您會看到新的物件具有您設定的所有屬性，或完全沒有物件。</span><span class="sxs-lookup"><span data-stu-id="1d99b-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="1d99b-119">您也可以嵌套組織單位。</span><span class="sxs-lookup"><span data-stu-id="1d99b-119">You can also nest organizational units.</span></span> <span data-ttu-id="1d99b-120">下列程式碼範例假設銷售部門會進一步細分為東部和西部區域。</span><span class="sxs-lookup"><span data-stu-id="1d99b-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="1d99b-121">這也適用于西部區域。</span><span class="sxs-lookup"><span data-stu-id="1d99b-121">This also applies for the West region.</span></span>

<span data-ttu-id="1d99b-122">若要直接系結至銷售組織中的東部區域，請指定辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="1d99b-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="1d99b-123">如果您已經系結至父物件 (Sales) ，您可以使用子物件的相對名稱，系結至父物件 (東部) 的子物件。</span><span class="sxs-lookup"><span data-stu-id="1d99b-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="1d99b-124">若要確定已建立物件，請使用 Active Directory 消費者和電腦 MMC 嵌入式管理單元來查看新的組織單位。</span><span class="sxs-lookup"><span data-stu-id="1d99b-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d99b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d99b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d99b-126">將現有的使用者移至組織單位</span><span class="sxs-lookup"><span data-stu-id="1d99b-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




