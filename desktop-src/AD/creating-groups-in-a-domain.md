---
title: 在網域中建立群組
description: 在將包含新群組的網域容器 Active Directory Domain Services 中建立群組物件。
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- 群組 AD，在網域中建立群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023266"
---
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="a9eb8-104">在網域中建立群組</span><span class="sxs-lookup"><span data-stu-id="a9eb8-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="a9eb8-105">在將包含新群組的網域容器 Active Directory Domain Services 中建立群組物件。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="a9eb8-106">您可以在網域的根目錄、組織單位內或在容器內建立群組。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="a9eb8-107">若要建立群組物件，請使用 [**IADsContainer：： create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 或 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="a9eb8-108">需要下列屬性才能讓群組物件成為 Active Directory 伺服器和 Windows 安全性系統可辨識的合法群組：</span><span class="sxs-lookup"><span data-stu-id="a9eb8-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="a9eb8-109"><span id="cn"></span><span id="CN"></span>**快遞 之 家**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-110">指定目錄中群組物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="a9eb8-111">這會是在建立群組的容器內，物件的相對辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-113">包含指定群組類型和範圍的整數。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="a9eb8-114">[**ADS \_ 群組 \_ 類型 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)列舉會定義 **groupType** 屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="a9eb8-115">下列清單會定義此屬性的一般群組類型和值。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="a9eb8-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>網域本機散發</span><span class="sxs-lookup"><span data-stu-id="a9eb8-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-117">**ADS \_ 群組 \_ 類型 \_ 域 \_ 本地 \_ 組**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>網域區域安全性</span><span class="sxs-lookup"><span data-stu-id="a9eb8-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-119">**廣告 \_群組 \_ 類型的 \_ 網域 \_ 本地 \_ 組** \| **ADS \_ 群組 \_ 類型 \_ 安全性 \_ 已啟用**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>全域散發</span><span class="sxs-lookup"><span data-stu-id="a9eb8-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-121">**ADS \_ 群組 \_ 類型 \_ 全域 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>全域安全性</span><span class="sxs-lookup"><span data-stu-id="a9eb8-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-123">**廣告 \_群組 \_ 類型 \_ 全域 \_ 群組** \| **廣告 \_ 群組 \_ 類型 \_ 安全性 \_ 已啟用**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>通用散發</span><span class="sxs-lookup"><span data-stu-id="a9eb8-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-125">**ADS \_ 群組 \_ 類型 \_ 通用 \_ 組**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>通用安全性</span><span class="sxs-lookup"><span data-stu-id="a9eb8-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-127">**廣告 \_群組 \_ 類型 \_ 通用 \_ 群組** \| **ADS \_ 群組 \_ 類型 \_ 安全性 \_ 已啟用**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="a9eb8-128">如果群組是要在目錄物件上設定存取控制，則群組應該是全域安全性或通用安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="a9eb8-129">請注意，通用安全性群組只能建立在以原生模式執行的 Windows 2000 網域上。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="a9eb8-130">如需偵測混合和原生模式的詳細資訊，請參閱偵測 [網域的操作模式](detecting-the-operation-mode-of-a-domain.md)。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9eb8-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="a9eb8-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="a9eb8-132">包含字串，此字串是用來支援舊版用戶端和伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="a9eb8-133">**SAMAccountName** 應小於20個字元，以支援舊版 Windows 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="a9eb8-134">**SAMAccountName** 在網域內的所有安全性主體物件之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="a9eb8-135">應針對定義域執行查詢，以確認 **sAMAccountName** 在網域內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="a9eb8-136">您可以使用 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) 方法，在建立時加入群組的成員。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="a9eb8-137">您可以選擇性地使用 [**IADsGroup：： Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) 方法，在建立之後將成員新增至群組。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="a9eb8-138">如需有關將成員新增至群組的詳細資訊，請參閱 [將成員新增至網域中的群組](adding-members-to-groups-in-a-domain.md)。</span><span class="sxs-lookup"><span data-stu-id="a9eb8-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 