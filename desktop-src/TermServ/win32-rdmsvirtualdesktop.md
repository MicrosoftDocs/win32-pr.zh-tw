---
title: Win32_RDMSVirtualDesktop 類別
description: 代表虛擬桌面。
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop 類別遠端桌面服務
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965895"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="8e251-105">Win32 \_ RDMSVirtualDesktop 類別</span><span class="sxs-lookup"><span data-stu-id="8e251-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="8e251-106">代表虛擬桌面。</span><span class="sxs-lookup"><span data-stu-id="8e251-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="8e251-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e251-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e251-108">語法</span><span class="sxs-lookup"><span data-stu-id="8e251-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="8e251-109">成員</span><span class="sxs-lookup"><span data-stu-id="8e251-109">Members</span></span>

<span data-ttu-id="8e251-110">**Win32 \_ RDMSVirtualDesktop** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e251-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="8e251-111">方法</span><span class="sxs-lookup"><span data-stu-id="8e251-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8e251-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8e251-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8e251-113">方法</span><span class="sxs-lookup"><span data-stu-id="8e251-113">Methods</span></span>

<span data-ttu-id="8e251-114">**Win32 \_ RDMSVirtualDesktop** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8e251-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="8e251-115">方法</span><span class="sxs-lookup"><span data-stu-id="8e251-115">Method</span></span>                                                                                              | <span data-ttu-id="8e251-116">描述</span><span class="sxs-lookup"><span data-stu-id="8e251-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e251-117">**GetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="8e251-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="8e251-118">抓取指派給虛擬桌面使用者的使用者名稱和功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="8e251-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="8e251-119">**GetVirtualDesktopAssignedToUser**</span><span class="sxs-lookup"><span data-stu-id="8e251-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="8e251-120">抓取指派給指定使用者的虛擬桌面。</span><span class="sxs-lookup"><span data-stu-id="8e251-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="8e251-121">**GetVirtualDesktopDetails**</span><span class="sxs-lookup"><span data-stu-id="8e251-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="8e251-122">抓取虛擬桌面的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e251-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="8e251-123">**GetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="8e251-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="8e251-124">捕獲虛擬桌面的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e251-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="8e251-125">**RemoveUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="8e251-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="8e251-126">從虛擬桌面移除使用者指派。</span><span class="sxs-lookup"><span data-stu-id="8e251-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="8e251-127">**SetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="8e251-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="8e251-128">將虛擬桌面指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="8e251-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="8e251-129">**SetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="8e251-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="8e251-130">更新虛擬桌面的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e251-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="8e251-131">屬性</span><span class="sxs-lookup"><span data-stu-id="8e251-131">Properties</span></span>

<span data-ttu-id="8e251-132">**Win32 \_ RDMSVirtualDesktop** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e251-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e251-133">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="8e251-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e251-136">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8e251-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8e251-137">取得管理虛擬機器之虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="8e251-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="8e251-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e251-141">取得裝載虛擬機器的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8e251-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8e251-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e251-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e251-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8e251-146">取得虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e251-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-147">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="8e251-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e251-150">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8e251-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8e251-151">取得虛擬桌面會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e251-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-152">**SessionUserName**</span><span class="sxs-lookup"><span data-stu-id="8e251-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e251-155">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8e251-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8e251-156">取得登入虛擬桌面會話之使用者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8e251-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-157">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8e251-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-158">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e251-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e251-160">取得虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e251-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-161">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="8e251-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e251-164">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8e251-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8e251-165">取得指派給虛擬桌面之使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="8e251-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-166">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="8e251-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e251-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e251-169">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8e251-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8e251-170">取得指派給虛擬桌面使用者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8e251-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="8e251-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="8e251-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e251-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e251-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e251-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e251-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e251-174">取得虛擬桌面的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e251-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e251-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e251-175">Requirements</span></span>



| <span data-ttu-id="8e251-176">需求</span><span class="sxs-lookup"><span data-stu-id="8e251-176">Requirement</span></span> | <span data-ttu-id="8e251-177">值</span><span class="sxs-lookup"><span data-stu-id="8e251-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e251-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e251-178">Minimum supported client</span></span><br/> | <span data-ttu-id="8e251-179">都不支援</span><span class="sxs-lookup"><span data-stu-id="8e251-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8e251-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e251-180">Minimum supported server</span></span><br/> | <span data-ttu-id="8e251-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e251-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8e251-182">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e251-182">Namespace</span></span><br/>                | <span data-ttu-id="8e251-183">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="8e251-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8e251-184">MOF</span><span class="sxs-lookup"><span data-stu-id="8e251-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e251-185"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e251-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e251-186">DLL</span><span class="sxs-lookup"><span data-stu-id="8e251-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e251-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e251-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8e251-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e251-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e251-189">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="8e251-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

