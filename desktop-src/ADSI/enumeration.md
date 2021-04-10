---
title: 列舉型別
description: 使用 ADSI 存取和運算元據提供數個列舉範例。 您也可以列舉容器物件的子系。 這些子系是物件本身，而不只是物件的屬性。
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，範例程式碼 Visual Basic，使用 IADsContainer 來列舉物件
- 容器 ADSI，使用 IADsContainer 來列舉容器的子系
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931846"
---
# <a name="enumeration"></a><span data-ttu-id="76347-107">列舉型別</span><span class="sxs-lookup"><span data-stu-id="76347-107">Enumeration</span></span>

<span data-ttu-id="76347-108">[使用 ADSI 存取和運算元據](accessing-and-manipulating-data-with-adsi.md) 提供數個列舉範例。</span><span class="sxs-lookup"><span data-stu-id="76347-108">[Accessing and Manipulating Data with ADSI](accessing-and-manipulating-data-with-adsi.md) provides several examples of enumeration.</span></span> <span data-ttu-id="76347-109">您也可以列舉容器物件的子系。</span><span class="sxs-lookup"><span data-stu-id="76347-109">You can also enumerate the children of container objects.</span></span> <span data-ttu-id="76347-110">這些子系是物件本身，而不只是物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="76347-110">These children are objects themselves, rather than just properties on objects.</span></span>

<span data-ttu-id="76347-111">下列範例會使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面來列舉容器的子系。</span><span class="sxs-lookup"><span data-stu-id="76347-111">The following example uses the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface to enumerate the children of the container.</span></span>


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




