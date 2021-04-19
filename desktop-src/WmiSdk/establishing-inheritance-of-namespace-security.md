---
description: 您可以控制子命名空間是否繼承父命名空間的安全描述項。
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: 建立命名空間安全性的繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990426"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="af124-103">建立命名空間安全性的繼承</span><span class="sxs-lookup"><span data-stu-id="af124-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="af124-104">您可以控制子命名空間是否繼承父命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="af124-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="af124-105">WMI 命名空間具有安全描述項，可控制誰可以存取命名空間和命名空間的資料。</span><span class="sxs-lookup"><span data-stu-id="af124-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="af124-106">每個安全描述項都有 (DACL) 的任意存取控制清單，以及 (SACL) 的安全性存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="af124-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="af124-107">這些清單包含 (ACE) 的存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="af124-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="af124-108">根據設定的 [**命名空間 ACE 旗標常數**](namespace-ace-flag-constants.md) ，該命名空間的所有子命名空間可能會繼承套用至命名空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="af124-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="af124-109">如果 **容器 \_ 繼承 \_ ACE** 旗標是在父命名空間安全描述項中，則在建立子命名空間時，子命名空間會繼承其父命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="af124-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="af124-110">如果 **CONTAINER \_ INHERIT \_ ace \| 未設定 \_ 無限傳播 \_ INHERIT \_ ace** ，則只有子命名空間會繼承安全描述項，而非孫命名空間。</span><span class="sxs-lookup"><span data-stu-id="af124-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="af124-111">子命名空間可以藉由呼叫 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別的方法來寫入新的安全描述項，藉以覆寫其父系的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="af124-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="af124-112">無法變更預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="af124-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="af124-113">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。如需 Dacl 的詳細資訊，請參閱 (ACL) 和 [**命名空間 ACE 類型常數**](namespace-ace-type-constants.md)的 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="af124-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="af124-114">請注意，預設許可權無法變更。</span><span class="sxs-lookup"><span data-stu-id="af124-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="af124-115">此外，設定安全描述項 (SD) 時，設定「 **SE \_ DACL \_ 保護** 」旗標並不會用來將特製化 SD 新增至子命名空間。</span><span class="sxs-lookup"><span data-stu-id="af124-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="af124-116">若要覆寫繼承的 SD，請只設定一個新的 SD。</span><span class="sxs-lookup"><span data-stu-id="af124-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="af124-117">若要將該 SD 繼承至子命名空間，請在命名空間安全描述項中傳遞 **容器 \_ inherit \_ ACE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="af124-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="af124-118">若要只繼承子系，而不是子代，請傳遞 `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="af124-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="af124-119">.</span><span class="sxs-lookup"><span data-stu-id="af124-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af124-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="af124-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af124-121">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="af124-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="af124-122">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="af124-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 
