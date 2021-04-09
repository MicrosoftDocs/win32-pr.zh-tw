---
title: 消費者介面對應的電腦物件
description: 下表列出 Active Directory 消費者和電腦嵌入式管理單元中電腦物件屬性工作表的元素。
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681686"
---
# <a name="computer-object-user-interface-mapping"></a><span data-ttu-id="6edee-103">消費者介面對應的電腦物件</span><span class="sxs-lookup"><span data-stu-id="6edee-103">Computer Object User Interface Mapping</span></span>

<span data-ttu-id="6edee-104">下表列出 Active Directory 消費者和電腦嵌入式管理單元中電腦物件屬性工作表的元素。</span><span class="sxs-lookup"><span data-stu-id="6edee-104">The following tables list elements of the Computer object property sheets in the Active Directory Users and Computers snap-in.</span></span>

## <a name="general-property-sheet"></a><span data-ttu-id="6edee-105">一般屬性工作表</span><span class="sxs-lookup"><span data-stu-id="6edee-105">General Property Sheet</span></span>

<span data-ttu-id="6edee-106">下表列出 [ **一般** ] 屬性工作表的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="6edee-106">The following table lists the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="6edee-107">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="6edee-107">UI label</span></span>                         | <span data-ttu-id="6edee-108">Active Directory Domain Services 屬性</span><span class="sxs-lookup"><span data-stu-id="6edee-108">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="6edee-109">註解</span><span class="sxs-lookup"><span data-stu-id="6edee-109">Comments</span></span>                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="6edee-110">電腦名稱稱 (Windows 2000 之前的) </span><span class="sxs-lookup"><span data-stu-id="6edee-110">Computer Name (pre-Windows 2000)</span></span> | <span data-ttu-id="6edee-111">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="6edee-111">sAMAccountName</span></span>                             |                                                  |
| <span data-ttu-id="6edee-112">DNS 名稱</span><span class="sxs-lookup"><span data-stu-id="6edee-112">DNS Name</span></span>                         | <span data-ttu-id="6edee-113">dNSHostName</span><span class="sxs-lookup"><span data-stu-id="6edee-113">dNSHostName</span></span>                                |                                                  |
| <span data-ttu-id="6edee-114">角色</span><span class="sxs-lookup"><span data-stu-id="6edee-114">Role</span></span>                             | <span data-ttu-id="6edee-115">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="6edee-115">userAccountControl</span></span>                         | <span data-ttu-id="6edee-116">切換 userAccountControl 位元遮罩中的位。</span><span class="sxs-lookup"><span data-stu-id="6edee-116">Toggles a bit in the userAccountControl bitmask.</span></span> |
| <span data-ttu-id="6edee-117">描述</span><span class="sxs-lookup"><span data-stu-id="6edee-117">Description</span></span>                      | <span data-ttu-id="6edee-118">description</span><span class="sxs-lookup"><span data-stu-id="6edee-118">description</span></span>                                |                                                  |
| <span data-ttu-id="6edee-119">信任電腦以進行委派</span><span class="sxs-lookup"><span data-stu-id="6edee-119">Trust Computer for delegation</span></span>    | <span data-ttu-id="6edee-120">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="6edee-120">userAccountControl</span></span>                         | <span data-ttu-id="6edee-121">切換 userAccountControl 位元遮罩中的位。</span><span class="sxs-lookup"><span data-stu-id="6edee-121">Toggles a bit in the userAccountControl bitmask.</span></span> |



 

## <a name="location-property-sheet"></a><span data-ttu-id="6edee-122">位置屬性工作表</span><span class="sxs-lookup"><span data-stu-id="6edee-122">Location Property Sheet</span></span>

<span data-ttu-id="6edee-123">下表列出 **Location** 屬性工作表的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="6edee-123">The following table lists the UI labels of the **Location** property sheet.</span></span>



| <span data-ttu-id="6edee-124">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="6edee-124">UI label</span></span> | <span data-ttu-id="6edee-125">Active Directory Domain Services 屬性</span><span class="sxs-lookup"><span data-stu-id="6edee-125">Active Directory Domain Services attribute</span></span> |
|----------|--------------------------------------------|
| <span data-ttu-id="6edee-126">Location</span><span class="sxs-lookup"><span data-stu-id="6edee-126">Location</span></span> | <span data-ttu-id="6edee-127">location</span><span class="sxs-lookup"><span data-stu-id="6edee-127">location</span></span>                                   |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="6edee-128">屬性工作表的成員</span><span class="sxs-lookup"><span data-stu-id="6edee-128">Member Of Property Sheet</span></span>

<span data-ttu-id="6edee-129">下表列出屬性工作表 **成員** 的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="6edee-129">The following table lists the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="6edee-130">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="6edee-130">UI label</span></span>          | <span data-ttu-id="6edee-131">Active Directory Domain Services 屬性</span><span class="sxs-lookup"><span data-stu-id="6edee-131">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="6edee-132">註解</span><span class="sxs-lookup"><span data-stu-id="6edee-132">Comments</span></span>                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edee-133">成員隸屬</span><span class="sxs-lookup"><span data-stu-id="6edee-133">Member of</span></span>         | <span data-ttu-id="6edee-134">memberOf</span><span class="sxs-lookup"><span data-stu-id="6edee-134">memberOf</span></span>                                   | <span data-ttu-id="6edee-135">包含 UI 清單中的所有群組（主要群組除外），而主要群組是透過 [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) 屬性在廣告中表示。</span><span class="sxs-lookup"><span data-stu-id="6edee-135">Includes all of the groups in the UI list, except the primary group, which is represented in the AD through the [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) attribute.</span></span> |
| <span data-ttu-id="6edee-136">設定主要群組</span><span class="sxs-lookup"><span data-stu-id="6edee-136">Set Primary Group</span></span> | <span data-ttu-id="6edee-137">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="6edee-137">primaryGroupID</span></span>                             | <span data-ttu-id="6edee-138">LDAP：系結至主要群組的 [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) 。</span><span class="sxs-lookup"><span data-stu-id="6edee-138">LDAP: Tied to [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) of the primary group.</span></span>                                                                                  |



 

## <a name="operating-system-property-sheet"></a><span data-ttu-id="6edee-139">作業系統屬性工作表</span><span class="sxs-lookup"><span data-stu-id="6edee-139">Operating System Property Sheet</span></span>

<span data-ttu-id="6edee-140">下表列出 **作業系統** 屬性工作表的 UI 標籤。</span><span class="sxs-lookup"><span data-stu-id="6edee-140">The following table lists the UI labels of the **Operating System** property sheet.</span></span>



| <span data-ttu-id="6edee-141">UI 標籤</span><span class="sxs-lookup"><span data-stu-id="6edee-141">UI label</span></span>     | <span data-ttu-id="6edee-142">Active Directory Domain Services 屬性</span><span class="sxs-lookup"><span data-stu-id="6edee-142">Active Directory Domain Services attribute</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="6edee-143">Name</span><span class="sxs-lookup"><span data-stu-id="6edee-143">Name</span></span>         | <span data-ttu-id="6edee-144">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="6edee-144">operatingSystem</span></span>                            |
| <span data-ttu-id="6edee-145">版本</span><span class="sxs-lookup"><span data-stu-id="6edee-145">Version</span></span>      | <span data-ttu-id="6edee-146">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="6edee-146">operatingSystemVersion</span></span>                     |
| <span data-ttu-id="6edee-147">Service Pack</span><span class="sxs-lookup"><span data-stu-id="6edee-147">Service Pack</span></span> | <span data-ttu-id="6edee-148">operatingSystemServicePack</span><span class="sxs-lookup"><span data-stu-id="6edee-148">operatingSystemServicePack</span></span>                 |



 

 

 