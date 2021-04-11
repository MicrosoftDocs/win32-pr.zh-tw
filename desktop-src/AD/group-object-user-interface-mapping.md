---
title: 群組物件消費者介面對應
description: 本主題說明 [Active Directory 消費者和電腦] 嵌入式管理單元中的 [群組物件] 屬性工作表。屬性工作表 SheetManaged 之屬性 SheetMembers 屬性的一般屬性 SheetMember
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- 消費者介面對應 AD 的群組物件
- 消費者介面對應，群組物件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2277c24f621f8e32f46b9e9571d0d0d4de9cfc
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023237"
---
# <a name="group-object-user-interface-mapping"></a><span data-ttu-id="0839c-105">群組物件消費者介面對應</span><span class="sxs-lookup"><span data-stu-id="0839c-105">Group Object User Interface Mapping</span></span>

<span data-ttu-id="0839c-106">本主題說明 [Active Directory 消費者和電腦] 嵌入式管理單元中的 [群組物件] 屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="0839c-106">This topic describes the Group object property sheets in the Active Directory Users and Computers snap-in.</span></span>

-   [<span data-ttu-id="0839c-107">一般屬性工作表</span><span class="sxs-lookup"><span data-stu-id="0839c-107">General Property Sheet</span></span>](#general-property-sheet)
-   [<span data-ttu-id="0839c-108">屬性工作表的成員</span><span class="sxs-lookup"><span data-stu-id="0839c-108">Member Of Property Sheet</span></span>](#member-of-property-sheet)
-   [<span data-ttu-id="0839c-109">成員屬性表</span><span class="sxs-lookup"><span data-stu-id="0839c-109">Members Property Sheet</span></span>](#members-property-sheet)
-   [<span data-ttu-id="0839c-110">由屬性工作表管理</span><span class="sxs-lookup"><span data-stu-id="0839c-110">Managed By Property Sheet</span></span>](#managed-by-property-sheet)

## <a name="general-property-sheet"></a><span data-ttu-id="0839c-111">一般屬性工作表</span><span class="sxs-lookup"><span data-stu-id="0839c-111">General Property Sheet</span></span>

<span data-ttu-id="0839c-112">下表顯示 [ **一般** ] 屬性工作表的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="0839c-112">The following table shows the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="0839c-113">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="0839c-113">UI label</span></span>                      | <span data-ttu-id="0839c-114">Active Directory Domain Services 中的屬性</span><span class="sxs-lookup"><span data-stu-id="0839c-114">Attribute in Active Directory Domain Services</span></span>     |
|-------------------------------|---------------------------------------------------|
| <span data-ttu-id="0839c-115">組名 (Windows 2000 之前的) </span><span class="sxs-lookup"><span data-stu-id="0839c-115">Group Name (pre-Windows 2000)</span></span> | [<span data-ttu-id="0839c-116">**SAM-帳戶-名稱**</span><span class="sxs-lookup"><span data-stu-id="0839c-116">**SAM-Account-Name**</span></span>](/windows/desktop/ADSchema/a-samaccountname) |
| <span data-ttu-id="0839c-117">Description</span><span class="sxs-lookup"><span data-stu-id="0839c-117">Description</span></span>                   | [<span data-ttu-id="0839c-118">**描述**</span><span class="sxs-lookup"><span data-stu-id="0839c-118">**Description**</span></span>](/windows/desktop/ADSchema/a-description)         |
| <span data-ttu-id="0839c-119">電子郵件</span><span class="sxs-lookup"><span data-stu-id="0839c-119">E-Mail</span></span>                        | [<span data-ttu-id="0839c-120">**電子郵件地址**</span><span class="sxs-lookup"><span data-stu-id="0839c-120">**E-mail-Addresses**</span></span>](/windows/desktop/ADSchema/a-mail)           |
| <span data-ttu-id="0839c-121">群組領域</span><span class="sxs-lookup"><span data-stu-id="0839c-121">Group Scope</span></span>                   | [<span data-ttu-id="0839c-122">**群組類型**</span><span class="sxs-lookup"><span data-stu-id="0839c-122">**Group-Type**</span></span>](/windows/desktop/ADSchema/a-grouptype)            |
| <span data-ttu-id="0839c-123">群組類型</span><span class="sxs-lookup"><span data-stu-id="0839c-123">Group Type</span></span>                    | [<span data-ttu-id="0839c-124">**群組類型**</span><span class="sxs-lookup"><span data-stu-id="0839c-124">**Group-Type**</span></span>](/windows/desktop/ADSchema/a-grouptype)            |
| <span data-ttu-id="0839c-125">備註</span><span class="sxs-lookup"><span data-stu-id="0839c-125">Notes</span></span>                         | [<span data-ttu-id="0839c-126">**註解**</span><span class="sxs-lookup"><span data-stu-id="0839c-126">**Comment**</span></span>](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="0839c-127">屬性工作表的成員</span><span class="sxs-lookup"><span data-stu-id="0839c-127">Member Of Property Sheet</span></span>

<span data-ttu-id="0839c-128">下表顯示內容表 **成員** 的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="0839c-128">The following table shows the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="0839c-129">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="0839c-129">UI label</span></span>  | <span data-ttu-id="0839c-130">Active Directory Domain Services 中的屬性</span><span class="sxs-lookup"><span data-stu-id="0839c-130">Attribute in Active Directory Domain Services</span></span> | <span data-ttu-id="0839c-131">Description</span><span class="sxs-lookup"><span data-stu-id="0839c-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0839c-132">成員隸屬</span><span class="sxs-lookup"><span data-stu-id="0839c-132">Member of</span></span> | [<span data-ttu-id="0839c-133">**是-DL 的成員**</span><span class="sxs-lookup"><span data-stu-id="0839c-133">**Is-Member-Of-DL**</span></span>](/windows/desktop/ADSchema/a-memberof)    | <span data-ttu-id="0839c-134">包含此群組所屬群組的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="0839c-134">Contains the distinguished names of the groups to which this group belongs.</span></span> <span data-ttu-id="0839c-135">這份清單中每個群組的成員屬性包含此群組物件的分辨名稱。使用者介面不會直接修改是- [**DL**](/windows/desktop/ADSchema/a-memberof) 屬性的成員。</span><span class="sxs-lookup"><span data-stu-id="0839c-135">The member attribute of each of the groups in this list contains the distinguished name of this group object.The user interface does not directly modify the [**Is-Member-Of-DL**](/windows/desktop/ADSchema/a-memberof) attribute.</span></span> <span data-ttu-id="0839c-136">它會修改此物件所屬之群組物件的 [**成員**](/windows/desktop/ADSchema/a-member) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-136">It modifies the [**Member**](/windows/desktop/ADSchema/a-member) attribute on the group object of which this object is made a member of.</span></span> <span data-ttu-id="0839c-137">Active Directory 伺服器 **會維護-DL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-137">The Active Directory server maintains the **Is-Member-Of-DL** attribute.</span></span><br/> |



 

## <a name="members-property-sheet"></a><span data-ttu-id="0839c-138">成員屬性表</span><span class="sxs-lookup"><span data-stu-id="0839c-138">Members Property Sheet</span></span>

<span data-ttu-id="0839c-139">下表顯示 [ **成員** ] 屬性工作表的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="0839c-139">The following table shows the UI labels of the **Members** property sheet.</span></span>



| <span data-ttu-id="0839c-140">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="0839c-140">UI label</span></span> | <span data-ttu-id="0839c-141">Active Directory Domain Services 中的屬性</span><span class="sxs-lookup"><span data-stu-id="0839c-141">Attribute in Active Directory Domain Services</span></span> | <span data-ttu-id="0839c-142">Description</span><span class="sxs-lookup"><span data-stu-id="0839c-142">Description</span></span>                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0839c-143">成員</span><span class="sxs-lookup"><span data-stu-id="0839c-143">Members</span></span>  | [<span data-ttu-id="0839c-144">**成員**</span><span class="sxs-lookup"><span data-stu-id="0839c-144">**Member**</span></span>](/windows/desktop/ADSchema/a-member)               | <span data-ttu-id="0839c-145">包含此群組物件成員的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="0839c-145">Contains the distinguished names of the members of this group object.</span></span> |



 

## <a name="managed-by-property-sheet"></a><span data-ttu-id="0839c-146">由屬性工作表管理</span><span class="sxs-lookup"><span data-stu-id="0839c-146">Managed By Property Sheet</span></span>

<span data-ttu-id="0839c-147">下表顯示 [ **受管理** 的] 屬性工作表的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="0839c-147">The following table shows the UI labels of the **Managed By** property sheet.</span></span>



| <span data-ttu-id="0839c-148">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="0839c-148">UI label</span></span>                           | <span data-ttu-id="0839c-149">Active Directory Domain Services 中的屬性</span><span class="sxs-lookup"><span data-stu-id="0839c-149">Attribute in Active Directory Domain Services</span></span>                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0839c-150">Name</span><span class="sxs-lookup"><span data-stu-id="0839c-150">Name</span></span>                               | [<span data-ttu-id="0839c-151">**管理者**</span><span class="sxs-lookup"><span data-stu-id="0839c-151">**Managed-By**</span></span>](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| <span data-ttu-id="0839c-152">管理員可以更新成員資格清單</span><span class="sxs-lookup"><span data-stu-id="0839c-152">Manager can update membership list</span></span> | <span data-ttu-id="0839c-153">無。</span><span class="sxs-lookup"><span data-stu-id="0839c-153">None.</span></span> <span data-ttu-id="0839c-154">具有「允許寫入成員」許可權的 ACE 會新增至依 **名稱** 識別的帳戶。</span><span class="sxs-lookup"><span data-stu-id="0839c-154">An ACE with the "Allow - Write Members" permission is added to the account identified by **Name**.</span></span>                        |
| <span data-ttu-id="0839c-155">Office</span><span class="sxs-lookup"><span data-stu-id="0839c-155">Office</span></span>                             | <span data-ttu-id="0839c-156">依 **名稱** 識別之帳戶的 [**實體傳遞-辦公室名稱**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-156">The [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) attribute of the account identified by **Name**.</span></span> |
| <span data-ttu-id="0839c-157">Street</span><span class="sxs-lookup"><span data-stu-id="0839c-157">Street</span></span>                             | <span data-ttu-id="0839c-158">依 **名稱** 識別的帳戶 [**街道位址**](/windows/desktop/ADSchema/a-street)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-158">The [**Street-Address**](/windows/desktop/ADSchema/a-street) attribute of the account identified by **Name**.</span></span>                                    |
| <span data-ttu-id="0839c-159">City</span><span class="sxs-lookup"><span data-stu-id="0839c-159">City</span></span>                               | <span data-ttu-id="0839c-160">依 **名稱** 識別之帳戶的 [**位置名稱**](/windows/desktop/ADSchema/a-l)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-160">The [**Locality-Name**](/windows/desktop/ADSchema/a-l) attribute of the account identified by **Name**.</span></span>                                          |
| <span data-ttu-id="0839c-161">州/省</span><span class="sxs-lookup"><span data-stu-id="0839c-161">State/province</span></span>                     | <span data-ttu-id="0839c-162">依 **名稱** 識別之帳戶的 [**州/省名稱**](/windows/desktop/ADSchema/a-st)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-162">The [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) attribute of the account identified by **Name**.</span></span>                                |
| <span data-ttu-id="0839c-163">國家/區域</span><span class="sxs-lookup"><span data-stu-id="0839c-163">Country/region</span></span>                     | <span data-ttu-id="0839c-164">依 **名稱** 識別之帳戶的 [**國家/地區名稱**](/windows/desktop/ADSchema/a-c)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-164">The [**Country-Name**](/windows/desktop/ADSchema/a-c) attribute of the account identified by **Name**.</span></span>                                           |
| <span data-ttu-id="0839c-165">電話號碼</span><span class="sxs-lookup"><span data-stu-id="0839c-165">Telephone number</span></span>                   | <span data-ttu-id="0839c-166">依 **名稱** 識別之帳戶的 [**電話號碼**](/windows/desktop/ADSchema/a-telephonenumber)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-166">The [**Telephone-Number**](/windows/desktop/ADSchema/a-telephonenumber) attribute of the account identified by **Name**.</span></span>                         |
| <span data-ttu-id="0839c-167">傳真號碼</span><span class="sxs-lookup"><span data-stu-id="0839c-167">Fax number</span></span>                         | <span data-ttu-id="0839c-168">依 **名稱** 識別之帳戶的 [**傳真呼叫號碼**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)屬性。</span><span class="sxs-lookup"><span data-stu-id="0839c-168">The [**Facsimile-Telephone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) attribute of the account identified by **Name**.</span></span>      |



 

 

