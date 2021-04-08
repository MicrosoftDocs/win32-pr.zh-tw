---
title: 依名稱尋找物件
description: Active Directory Domain Services 中的大部分物件都會使用 cn 屬性作為其命名屬性。
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- 依名稱 Active Directory、使用、搜尋
- 物件廣告，依名稱搜尋
- 依名稱尋找物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671279"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="622a1-106">依名稱尋找物件</span><span class="sxs-lookup"><span data-stu-id="622a1-106">Finding Objects by Name</span></span>

<span data-ttu-id="622a1-107">Active Directory Domain Services 中的大部分物件都會使用 **cn** 屬性作為其命名屬性。</span><span class="sxs-lookup"><span data-stu-id="622a1-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="622a1-108">不過，某些物件會使用 **cn** 以外的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="622a1-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="622a1-109">例如，網域控制站會使用命名屬性的 **domainDNS** 屬性，而組織單位會使用 **organizationalUnit** 屬性作為命名屬性。</span><span class="sxs-lookup"><span data-stu-id="622a1-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="622a1-110">為了避免必須針對不同的物件類型使用不同的命名屬性，必須使用 **name** 屬性（包含物件的相對辨別名稱）來依名稱搜尋物件。</span><span class="sxs-lookup"><span data-stu-id="622a1-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="622a1-111">範例</span><span class="sxs-lookup"><span data-stu-id="622a1-111">Examples</span></span>

<span data-ttu-id="622a1-112">下列程式碼範例會顯示不同的查詢字串，可用來依名稱尋找物件。</span><span class="sxs-lookup"><span data-stu-id="622a1-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="622a1-113">下列查詢字串會尋找名稱開頭為 "Jeff" 的所有物件。</span><span class="sxs-lookup"><span data-stu-id="622a1-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="622a1-114">下列查詢字串會尋找名稱開頭為 "租借" 或 "corp" 的所有電腦物件。</span><span class="sxs-lookup"><span data-stu-id="622a1-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="622a1-115">下列查詢字串會尋找所有使用者，以及名稱開頭為 "張穎" 或 "Jeff" 的使用者。</span><span class="sxs-lookup"><span data-stu-id="622a1-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




