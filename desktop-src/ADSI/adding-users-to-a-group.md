---
title: 將使用者新增至群組
description: Joe Worden 是企業系統管理員，現在會將 Julie Bankert 新增至管理群組。 若要將物件加入至群組，請使用 IADsGroup。加入方法。
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- 將使用者加入至群組 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300108"
---
# <a name="adding-users-to-a-group"></a><span data-ttu-id="1f8c2-105">將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="1f8c2-105">Adding Users to a Group</span></span>

<span data-ttu-id="1f8c2-106">Joe Worden 是企業系統管理員，現在會將 Julie Bankert 新增至管理群組。</span><span class="sxs-lookup"><span data-stu-id="1f8c2-106">Joe Worden, the enterprise administrator, will now add Julie Bankert to the Management group.</span></span> <span data-ttu-id="1f8c2-107">若要將物件加入至群組，請使用 [**IADsGroup。加入**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) 方法。</span><span class="sxs-lookup"><span data-stu-id="1f8c2-107">To add an object to a group, use the [**IADsGroup.Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) method.</span></span>


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a><span data-ttu-id="1f8c2-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f8c2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8c2-109">建立新群組</span><span class="sxs-lookup"><span data-stu-id="1f8c2-109">Creating a New Group</span></span>](creating-a-new-group.md)
</dt> </dl>

 

 




