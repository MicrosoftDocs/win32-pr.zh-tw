---
title: 停用現有的類別和屬性
description: 新增架構是永久性的。
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671343"
---
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="f3f55-103">停用現有的類別和屬性</span><span class="sxs-lookup"><span data-stu-id="f3f55-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="f3f55-104">新增架構是永久性的。</span><span class="sxs-lookup"><span data-stu-id="f3f55-104">Schema additions are permanent.</span></span> <span data-ttu-id="f3f55-105">您無法刪除 **attributeSchema** 和 **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="f3f55-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="f3f55-106">在分散式系統中，很難保證指定類別或屬性沒有任何實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="f3f55-107">移除類別或屬性的定義會損害該類別或屬性的現有實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="f3f55-108">您可以藉由將現有的類別或屬性標示為「無用」來停用它。</span><span class="sxs-lookup"><span data-stu-id="f3f55-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="f3f55-109">這並不會影響類別或屬性的現有實例來標記，但會防止建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="f3f55-110">停用架構類別和屬性時，適用下列限制：</span><span class="sxs-lookup"><span data-stu-id="f3f55-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="f3f55-111">您無法停用類別目錄1類別或屬性。</span><span class="sxs-lookup"><span data-stu-id="f3f55-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="f3f55-112">您無法停用不是也停用之類別成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3f55-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="f3f55-113">這是因為 (未停用) 類別的屬性可能是必要的，而停用屬性則會防止建立類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="f3f55-114">若要停用屬性，請將其 **attributeSchema** 物件的 **isDefunct** 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f3f55-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="f3f55-115">當屬性停用時，就無法建立屬性的新實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="f3f55-116">若要重新啟用屬性，請將 **isDefunct** 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f3f55-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="f3f55-117">若要停用類別，請將其 **classSchema** 物件的 **isDefunct** 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f3f55-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="f3f55-118">當某個類別停用時，就無法建立類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="f3f55-119">若要重新啟用類別，請將 **isDefunct** 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f3f55-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="f3f55-120">將架構物件設定為無用，在實際執行環境中會很有用。</span><span class="sxs-lookup"><span data-stu-id="f3f55-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="f3f55-121">當不再需要架構延伸模組的測試版本時，請將它標示為無用。</span><span class="sxs-lookup"><span data-stu-id="f3f55-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="f3f55-122">您可以藉由移除 **isDefunct** 屬性或將屬性值設定為 **FALSE** 來還原。</span><span class="sxs-lookup"><span data-stu-id="f3f55-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="f3f55-123">這也可防止非預期的架構物件移除，因為它會將它設定為「無用」，因為可以輕鬆地反向操作。</span><span class="sxs-lookup"><span data-stu-id="f3f55-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="f3f55-124">請注意，當您讓架構物件無用時，Active Directory 伺服器不會清除屬性或類別的現有實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="f3f55-125">如果您移除 **isDefunct** 屬性，任何實例會再次變成有效的一般物件。</span><span class="sxs-lookup"><span data-stu-id="f3f55-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="f3f55-126">下列清單包含其他將 **attributeSchema** 或 **classSchema** 物件標示為無用的後果：</span><span class="sxs-lookup"><span data-stu-id="f3f55-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="f3f55-127">新增或修改實例失敗。</span><span class="sxs-lookup"><span data-stu-id="f3f55-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="f3f55-128">錯誤碼的行為就像是無用的類別永遠不存在一樣。</span><span class="sxs-lookup"><span data-stu-id="f3f55-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="f3f55-129">搜尋和刪除的行為就像尚未讓任何架構物件成為無用一樣。</span><span class="sxs-lookup"><span data-stu-id="f3f55-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="f3f55-130">只允許從物件刪除整個屬性。</span><span class="sxs-lookup"><span data-stu-id="f3f55-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="f3f55-131">下列清單包含生產環境中的其他選項，以減少無用架構延伸的影響：</span><span class="sxs-lookup"><span data-stu-id="f3f55-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="f3f55-132">從無用的類別中移除所有 **mayHave** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="f3f55-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="f3f55-133">從無用的類別中，減少所有 **mustHave** 屬性值的大小。</span><span class="sxs-lookup"><span data-stu-id="f3f55-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="f3f55-134">從通用類別目錄中移除無用的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3f55-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="f3f55-135">從任何索引中移除無用的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3f55-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="f3f55-136">在實際執行環境中移除不必要架構變更的其他選項，是讓開發人員使用私用網域控制站進行測試。</span><span class="sxs-lookup"><span data-stu-id="f3f55-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="f3f55-137">在此情況下，您可以：</span><span class="sxs-lookup"><span data-stu-id="f3f55-137">In this case, you can:</span></span>

-   <span data-ttu-id="f3f55-138">使用 Dcpromo.exe 將 DC 降級，以「重設」 Active Directory 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f3f55-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="f3f55-139">降級完成之後，請再次使用 Dcpromo.exe 將伺服器升級回 DC。</span><span class="sxs-lookup"><span data-stu-id="f3f55-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="f3f55-140">然後，開發人員可以使用 LDIF 腳本來重載任何必要的類別、屬性和物件實例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="f3f55-141">使用 Ntbackup.exe 對可用的磁碟分割執行系統狀態備份。</span><span class="sxs-lookup"><span data-stu-id="f3f55-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="f3f55-142">重新開機至安全/目錄服務還原模式以進行還原。</span><span class="sxs-lookup"><span data-stu-id="f3f55-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="f3f55-143">若為 Windows Server 2003 作業系統，當您將類別或屬性設定為 [無用] 時，當您建立新的類別或屬性來取代它時，可以立即重複使用無用架構專案的 **ldapDisplayName**、 **schemaIdGuid**、 **OID** 和 **mapiID** 值。</span><span class="sxs-lookup"><span data-stu-id="f3f55-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="f3f55-144">類別或屬性的無用版本會保留在架構容器中，但會在 MMC 嵌入式管理單元中隱藏。</span><span class="sxs-lookup"><span data-stu-id="f3f55-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="f3f55-145">若要重新啟用舊的 schema 元素，請將 **isDefunct** 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f3f55-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="f3f55-146">下列 LDIF 程式碼範例顯示如何修改 **isDefunct** 屬性並變更 RDN，使其不會與您建立用來取代它的新類別混淆。</span><span class="sxs-lookup"><span data-stu-id="f3f55-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

<span data-ttu-id="f3f55-147">使用下列命令，針對在 Windows Server 2003 作業系統上執行的電腦，對樹系執行 LDIF 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="f3f55-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="f3f55-148">**ldifde/i/f rdn .ldf。 .ldf/c "DC = X" "dc = mydomain，DC = com"**</span><span class="sxs-lookup"><span data-stu-id="f3f55-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="f3f55-149"> (，其中 "DC = X" 是常數) </span><span class="sxs-lookup"><span data-stu-id="f3f55-149">(Where "DC=X" is a constant)</span></span>

 

 




