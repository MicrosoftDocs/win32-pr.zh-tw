---
title: 保護物件不受繼承許可權的影響
description: 如在繼承和委派管理主題中所討論，Ace 可以設定在容器物件上（例如 organizationalUnit、domainDNS、容器等），並根據這些 Ace 上設定的 ACE 旗標傳播到子物件。
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- 保護物件不受繼承的許可權 AD 影響
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023229"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="c5723-104">保護物件不受繼承許可權的影響</span><span class="sxs-lookup"><span data-stu-id="c5723-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="c5723-105">如在 [繼承和委派管理](inheritance-and-delegation-of-administration.md)主題中所討論，ace 可以設定在容器物件上（例如 **organizationalUnit**、 **domainDNS**、 **容器** 等），並根據這些 ace 上設定的 ace 旗標傳播到子物件。</span><span class="sxs-lookup"><span data-stu-id="c5723-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="c5723-106">如果您有一個安全物件或您想要明確控制其 Ace 的物件（例如私用 OU 或特殊使用者），則可以防止 Ace 依其父容器或其父容器的前置項傳播至物件。</span><span class="sxs-lookup"><span data-stu-id="c5723-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="c5723-107">您可以使用 [**IADsSecurityDescriptor**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 屬性來控制是否要由物件的父容器繼承 Dacl 和 sacl。</span><span class="sxs-lookup"><span data-stu-id="c5723-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="c5723-108">[**IADsSecurityDescriptor 控制項**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods)屬性可以用來保護物件免于繼承的 ace 的影響。</span><span class="sxs-lookup"><span data-stu-id="c5723-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="c5723-109">下列旗標會強制在物件上明確設定存取控制，並防止使用者藉由在物件的父容器上設定可繼承的 Ace 或其父容器的前身來修改物件的存取控制。</span><span class="sxs-lookup"><span data-stu-id="c5723-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="c5723-110">旗標</span><span class="sxs-lookup"><span data-stu-id="c5723-110">Flag</span></span>                               | <span data-ttu-id="c5723-111">描述</span><span class="sxs-lookup"><span data-stu-id="c5723-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5723-112">**已 \_ 保護 SE DACL \_**</span><span class="sxs-lookup"><span data-stu-id="c5723-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="c5723-113">防止在父容器的 DACL 上設定 Ace，以及目錄階層中父容器上方的任何物件套用至物件 DACL。</span><span class="sxs-lookup"><span data-stu-id="c5723-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="c5723-114">**SE \_ SACL \_ 受保護**</span><span class="sxs-lookup"><span data-stu-id="c5723-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="c5723-115">防止將 Ace 設定在父容器的 SACL，以及目錄階層中父容器上方的任何物件，而不會套用到物件 SACL。</span><span class="sxs-lookup"><span data-stu-id="c5723-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="c5723-116">請注意，必須要有「 **se \_ dacl \_** 」旗標，才能設定「 **se \_ dacl \_ 受保護** 」，而「必須」有「se **\_ sacl \_** 」來設定「 **se \_ sacl \_ 受保護**」。</span><span class="sxs-lookup"><span data-stu-id="c5723-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 

