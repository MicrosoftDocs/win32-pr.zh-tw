---
title: Win32_RDMSDesktopAssignment 類別
description: 描述 RD 集合使用者桌面指派。
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment 類別遠端桌面服務
- Win32_RDMSDesktopAssignment 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317239"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="954e4-105">Win32 \_ RDMSDesktopAssignment 類別</span><span class="sxs-lookup"><span data-stu-id="954e4-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="954e4-106">描述 RD 集合使用者桌面指派。</span><span class="sxs-lookup"><span data-stu-id="954e4-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="954e4-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="954e4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="954e4-108">語法</span><span class="sxs-lookup"><span data-stu-id="954e4-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="954e4-109">成員</span><span class="sxs-lookup"><span data-stu-id="954e4-109">Members</span></span>

<span data-ttu-id="954e4-110">**Win32 \_ RDMSDesktopAssignment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="954e4-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="954e4-111">方法</span><span class="sxs-lookup"><span data-stu-id="954e4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="954e4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="954e4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="954e4-113">方法</span><span class="sxs-lookup"><span data-stu-id="954e4-113">Methods</span></span>

<span data-ttu-id="954e4-114">**Win32 \_ RDMSDesktopAssignment** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="954e4-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="954e4-115">方法</span><span class="sxs-lookup"><span data-stu-id="954e4-115">Method</span></span>                                                                                 | <span data-ttu-id="954e4-116">描述</span><span class="sxs-lookup"><span data-stu-id="954e4-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="954e4-117">**AddDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="954e4-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="954e4-118">新增桌面指派。</span><span class="sxs-lookup"><span data-stu-id="954e4-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="954e4-119">**RemoveDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="954e4-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="954e4-120">移除桌面指派。</span><span class="sxs-lookup"><span data-stu-id="954e4-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="954e4-121">屬性</span><span class="sxs-lookup"><span data-stu-id="954e4-121">Properties</span></span>

<span data-ttu-id="954e4-122">**Win32 \_ RDMSDesktopAssignment** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="954e4-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="954e4-123">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="954e4-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="954e4-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="954e4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954e4-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="954e4-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="954e4-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="954e4-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="954e4-127">集合的別名。</span><span class="sxs-lookup"><span data-stu-id="954e4-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="954e4-128">**DesktopName**</span><span class="sxs-lookup"><span data-stu-id="954e4-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="954e4-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="954e4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954e4-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="954e4-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="954e4-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="954e4-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="954e4-132">桌面的名稱。</span><span class="sxs-lookup"><span data-stu-id="954e4-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="954e4-133">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="954e4-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="954e4-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="954e4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954e4-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="954e4-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="954e4-136">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="954e4-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="954e4-137">使用者帳戶功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="954e4-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="954e4-138">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="954e4-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="954e4-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="954e4-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954e4-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="954e4-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="954e4-141">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="954e4-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="954e4-142">使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="954e4-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="954e4-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="954e4-143">Requirements</span></span>



| <span data-ttu-id="954e4-144">需求</span><span class="sxs-lookup"><span data-stu-id="954e4-144">Requirement</span></span> | <span data-ttu-id="954e4-145">值</span><span class="sxs-lookup"><span data-stu-id="954e4-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="954e4-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="954e4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="954e4-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="954e4-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="954e4-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="954e4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="954e4-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="954e4-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="954e4-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="954e4-150">Namespace</span></span><br/>                | <span data-ttu-id="954e4-151">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="954e4-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="954e4-152">MOF</span><span class="sxs-lookup"><span data-stu-id="954e4-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="954e4-153"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="954e4-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="954e4-154">DLL</span><span class="sxs-lookup"><span data-stu-id="954e4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="954e4-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="954e4-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

