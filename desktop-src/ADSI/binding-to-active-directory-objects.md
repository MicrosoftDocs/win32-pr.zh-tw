---
title: 系結至 Active Directory 物件
description: 繼續進行此案例之前，您必須先瞭解 ADSI 物件在 Active Directory 中的命名方式，以及如何加以系結。 系結 ADSI 物件會將物件與目錄服務連接，並可讓您存取物件的方法。
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020807"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="75c6a-104">系結至 Active Directory 物件</span><span class="sxs-lookup"><span data-stu-id="75c6a-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="75c6a-105">繼續進行此案例之前，您必須先瞭解 ADSI 物件在 Active Directory 中的命名方式，以及如何加以系結。</span><span class="sxs-lookup"><span data-stu-id="75c6a-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="75c6a-106">系結 ADSI 物件會將物件與目錄服務連接，並可讓您存取物件的方法。</span><span class="sxs-lookup"><span data-stu-id="75c6a-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="75c6a-107">ADsPath</span><span class="sxs-lookup"><span data-stu-id="75c6a-107">ADsPath</span></span>

<span data-ttu-id="75c6a-108">ADSI 物件是由其系結字串（也稱為 ADsPath）唯一識別。</span><span class="sxs-lookup"><span data-stu-id="75c6a-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="75c6a-109">ADsPath 是 ADSI 提供者的程式設計識別碼 (progID) 的組合，以及物件的分辨名稱 (DN) 。</span><span class="sxs-lookup"><span data-stu-id="75c6a-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="75c6a-110">以下是 ADsPath 的格式：</span><span class="sxs-lookup"><span data-stu-id="75c6a-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="75c6a-111">"progID://DN"</span><span class="sxs-lookup"><span data-stu-id="75c6a-111">"progID://DN"</span></span>

-   <span data-ttu-id="75c6a-112">pogID： ADSI 提供者的程式設計識別碼，例如 LDAP 或 WinNT。</span><span class="sxs-lookup"><span data-stu-id="75c6a-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="75c6a-113">：//-分隔 progID 與 DN。</span><span class="sxs-lookup"><span data-stu-id="75c6a-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="75c6a-114">DN-ADSI 物件的辨別名稱，也就是物件的完整路徑，其中路徑是由 (RDNs) 的相對辨別名稱所組成。</span><span class="sxs-lookup"><span data-stu-id="75c6a-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="75c6a-115">RDN 是沒有路徑的物件名稱，而且在其同級物件中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="75c6a-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="75c6a-116">RDN 包含屬性識別碼和值（例如 "DC = Fabrikam"），其中 DC 是屬性，而 Fabrikam 是值。</span><span class="sxs-lookup"><span data-stu-id="75c6a-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="75c6a-117">DC 是代表網域元件的 RDN 屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="75c6a-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="75c6a-118">以下是 ADsPath 的範例：</span><span class="sxs-lookup"><span data-stu-id="75c6a-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="75c6a-119">"LDAP：//DC = Fabrikam，DC = Com"</span><span class="sxs-lookup"><span data-stu-id="75c6a-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="75c6a-120">系結物件</span><span class="sxs-lookup"><span data-stu-id="75c6a-120">Binding the object</span></span>

<span data-ttu-id="75c6a-121">以下是您可以在此案例中系結網域物件的方式：</span><span class="sxs-lookup"><span data-stu-id="75c6a-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="75c6a-122">當您執行此程式碼範例時，ADSI 會使用 DN 來判斷要系結的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="75c6a-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="75c6a-123">ADSI 系結這些物件之後，您就可以存取它們的方法。</span><span class="sxs-lookup"><span data-stu-id="75c6a-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="75c6a-124">先前的程式碼範例會將網域物件系結至 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 和 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)。</span><span class="sxs-lookup"><span data-stu-id="75c6a-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="75c6a-125">您現在可以在這些介面上使用方法，例如 [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get)、 [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put)、 [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)、 [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)和 [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)。</span><span class="sxs-lookup"><span data-stu-id="75c6a-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="75c6a-126">系結網域物件之後，您可以列印其部分屬性：</span><span class="sxs-lookup"><span data-stu-id="75c6a-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="75c6a-127">如需 ADsPath 的詳細資訊，請參閱系結 [字串](binding-string.md)。</span><span class="sxs-lookup"><span data-stu-id="75c6a-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="75c6a-128">如需系結的詳細資訊，請參閱系結 [至 ADSI 物件](binding-to-an-adsi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="75c6a-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75c6a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="75c6a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c6a-130">建立組織單位</span><span class="sxs-lookup"><span data-stu-id="75c6a-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 




