---
title: 將現有的使用者移至組織單位
description: 當企業系統管理員（Joe Worden）將 Windows NT 4.0 網域升級為 Active Directory 時，所有使用者和群組都會遷移至 Fabrikam 網域中的 [使用者] 容器。
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- 將現有的使用者移至組織單位的 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182986"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="f8e29-104">將現有的使用者移至組織單位</span><span class="sxs-lookup"><span data-stu-id="f8e29-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="f8e29-105">當企業系統管理員（Joe Worden）將 Windows NT 4.0 網域升級為 Active Directory 時，所有使用者和群組都會遷移至 Fabrikam 網域中的 [使用者] 容器。</span><span class="sxs-lookup"><span data-stu-id="f8e29-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="f8e29-106">Joe 現在可以將這些使用者和群組移至適當的組織單位。</span><span class="sxs-lookup"><span data-stu-id="f8e29-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="f8e29-107">您也可以使用 ADSI 在相關的 Windows 2000 網域之間移動物件。</span><span class="sxs-lookup"><span data-stu-id="f8e29-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="f8e29-108">在下列程式碼範例中，Joe 會將 "jeffsmith" 移至銷售組織。</span><span class="sxs-lookup"><span data-stu-id="f8e29-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="f8e29-109">[**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)方法會取得要移動之物件的 ADsPath，而新的物件名稱 (RDN) 。</span><span class="sxs-lookup"><span data-stu-id="f8e29-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="f8e29-110">若要保留相同的名稱，您可以為 *bstrNewName* 參數指定 **Null** (**vbNullString**) 。</span><span class="sxs-lookup"><span data-stu-id="f8e29-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="f8e29-111">若要在移動時重新命名物件，請為 *bstrNewName* 參數指定新的相對分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f8e29-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="f8e29-112">例如，若要將 jeffsmith 移至銷售組織，並在相同的作業中將 "jeffsmith" 物件重新命名為 "jeff \_ smith"，Joe 會執行下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="f8e29-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="f8e29-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8e29-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e29-114">在組織單位中建立新的使用者</span><span class="sxs-lookup"><span data-stu-id="f8e29-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




