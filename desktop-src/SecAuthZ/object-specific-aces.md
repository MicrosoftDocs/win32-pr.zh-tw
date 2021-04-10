---
description: 目錄服務 (DS) 物件支援特定物件的 Ace。 特定物件的 ACE 包含一組 Guid，可擴充 ACE 可以保護物件的方式。
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: 物件特定的 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027095"
---
# <a name="object-specific-aces"></a><span data-ttu-id="73b41-104">物件特定的 Ace</span><span class="sxs-lookup"><span data-stu-id="73b41-104">Object-specific ACEs</span></span>

<span data-ttu-id="73b41-105">目錄服務 (DS) 物件支援特定物件的 [*ace*](/windows/desktop/SecGloss/a-gly) 。</span><span class="sxs-lookup"><span data-stu-id="73b41-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="73b41-106">特定物件的 ACE 包含一組 Guid，可擴充 ACE 可以保護物件的方式。</span><span class="sxs-lookup"><span data-stu-id="73b41-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73b41-107">GUID</span><span class="sxs-lookup"><span data-stu-id="73b41-107">GUID</span></span></th>
<th><span data-ttu-id="73b41-108">Description</span><span class="sxs-lookup"><span data-stu-id="73b41-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73b41-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="73b41-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="73b41-110">識別下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="73b41-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="73b41-111">子物件的類型。</span><span class="sxs-lookup"><span data-stu-id="73b41-111">A type of child object.</span></span> <span data-ttu-id="73b41-112">ACE 控制建立指定之子物件類型的許可權。</span><span class="sxs-lookup"><span data-stu-id="73b41-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="73b41-113">如需詳細資訊，請參閱 <a href="controlling-child-object-creation-in-c--.md">在 c + + 中控制建立子物件</a>。</span><span class="sxs-lookup"><span data-stu-id="73b41-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="73b41-114">屬性集或屬性。</span><span class="sxs-lookup"><span data-stu-id="73b41-114">A property set or property.</span></span> <span data-ttu-id="73b41-115">ACE 控制讀取或寫入屬性（property）或屬性集的許可權。</span><span class="sxs-lookup"><span data-stu-id="73b41-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="73b41-116">如需詳細資訊，請參閱 <a href="aces-to-control-access-to-an-object-s-properties.md">ace 來控制物件屬性的存取</a>。</span><span class="sxs-lookup"><span data-stu-id="73b41-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="73b41-117">延伸的許可權。</span><span class="sxs-lookup"><span data-stu-id="73b41-117">An extended right.</span></span> <span data-ttu-id="73b41-118">ACE 控制執行與擴充許可權相關聯之作業的許可權。</span><span class="sxs-lookup"><span data-stu-id="73b41-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="73b41-119">經過驗證的寫入。</span><span class="sxs-lookup"><span data-stu-id="73b41-119">A validated write.</span></span> <span data-ttu-id="73b41-120">ACE 控制執行特定寫入作業的許可權。</span><span class="sxs-lookup"><span data-stu-id="73b41-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="73b41-121">這些已驗證的寫入權限（在 ACL 編輯器中定義和公開）提供了驗證的屬性寫入權限，而不是將任何值的未檢查低層級寫入，授與具有 &quot; write property 許可權的屬性 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="73b41-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73b41-122"><strong>InheritedObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="73b41-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="73b41-123">表示可以繼承 ACE 的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="73b41-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="73b41-124">繼承也是由 <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>中的繼承旗標，以及針對子物件所放置之繼承的任何保護所控制。</span><span class="sxs-lookup"><span data-stu-id="73b41-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="73b41-125">如需詳細資訊，請參閱 <a href="ace-inheritance.md">ACE 繼承</a>。</span><span class="sxs-lookup"><span data-stu-id="73b41-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="73b41-126">支援三種類型的物件特定 Ace。</span><span class="sxs-lookup"><span data-stu-id="73b41-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="73b41-127">目前不支援系統警示物件 Ace。</span><span class="sxs-lookup"><span data-stu-id="73b41-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="73b41-128">類型</span><span class="sxs-lookup"><span data-stu-id="73b41-128">Type</span></span>                      | <span data-ttu-id="73b41-129">Description</span><span class="sxs-lookup"><span data-stu-id="73b41-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b41-130">拒絕存取的物件 ACE</span><span class="sxs-lookup"><span data-stu-id="73b41-130">Access-denied object ACE</span></span>  | <span data-ttu-id="73b41-131">用於 DACL 中，以拒絕受信任者存取物件上設定的屬性或屬性，或限制 ACE 繼承到指定的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="73b41-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="73b41-132">使用 [**拒絕存取 \_ \_ 物件 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) 結構。</span><span class="sxs-lookup"><span data-stu-id="73b41-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="73b41-133">存取-允許的物件 ACE</span><span class="sxs-lookup"><span data-stu-id="73b41-133">Access-allowed object ACE</span></span> | <span data-ttu-id="73b41-134">在 DACL 中用來允許信任者存取物件上設定的屬性或屬性，或限制 ACE 繼承至指定的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="73b41-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="73b41-135">使用 [**存取 \_ 允許的 \_ 物件 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) 結構。</span><span class="sxs-lookup"><span data-stu-id="73b41-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="73b41-136">系統審核物件 ACE</span><span class="sxs-lookup"><span data-stu-id="73b41-136">System-audit object ACE</span></span>   | <span data-ttu-id="73b41-137">在 SACL 中用來記錄受信任者嘗試存取物件上設定的屬性或屬性，或限制 ACE 繼承至指定的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="73b41-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="73b41-138">使用 [**系統 \_ AUDIT \_ OBJECT \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) 結構。</span><span class="sxs-lookup"><span data-stu-id="73b41-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="73b41-139">任何包含物件專屬 ACE 的 ACL，都必須使用修訂 ACL 的 \_ 修訂 \_ DS。</span><span class="sxs-lookup"><span data-stu-id="73b41-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 
