---
title: 混合式環境的系結問題
description: 混合式環境的系結問題
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，使用，混合式環境的系結問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966269"
---
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="e6eb5-104">混合式環境的系結問題</span><span class="sxs-lookup"><span data-stu-id="e6eb5-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="e6eb5-105">針對包含 Active Directory 網域與 Windows NT 4.0 網域具有信任關係的環境，使用無伺服器系結來系結至 Active Directory 物件時可能會發生問題。</span><span class="sxs-lookup"><span data-stu-id="e6eb5-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="e6eb5-106">在某些網路環境中，為了允許網域之間的驗證，在包含 Active Directory 和 Windows NT 4.0 伺服器的網域控制站之間已設定信任關係。</span><span class="sxs-lookup"><span data-stu-id="e6eb5-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="e6eb5-107">在這些混合的環境中，如果使用者是 Windows NT 4.0 的成員，網域會嘗試使用無伺服器系結來系結至受信任網域上的 Active Directory 物件，然後系結將會失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e6eb5-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="e6eb5-108">這是因為無伺服器系結會使用 [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) 函數系結至 Active Directory 中的物件，而此物件相依于適當的 DNS。</span><span class="sxs-lookup"><span data-stu-id="e6eb5-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="e6eb5-109">在此案例中，Windows NT 使用者必須提供要系結之特定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6eb5-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="e6eb5-110">以下是一個範例。</span><span class="sxs-lookup"><span data-stu-id="e6eb5-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 