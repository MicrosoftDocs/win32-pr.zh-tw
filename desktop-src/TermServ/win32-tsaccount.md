---
title: Win32_TSAccount 類別
description: 允許刪除存在於 Win32 終端機上的帳戶 \_ ，以及修改現有的許可權。
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Win32_TSAccount 類別遠端桌面服務
- Win32_TSAccount 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969817"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="094b7-105">Win32 \_ TSAccount 類別</span><span class="sxs-lookup"><span data-stu-id="094b7-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="094b7-106">**Win32 \_ TSAccount** WMI 類別可讓您刪除存在於 [**Win32 \_ 終端**](win32-terminal.md)機上的帳戶，以及修改現有的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="094b7-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="094b7-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="094b7-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="094b7-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="094b7-109">語法</span><span class="sxs-lookup"><span data-stu-id="094b7-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="094b7-110">成員</span><span class="sxs-lookup"><span data-stu-id="094b7-110">Members</span></span>

<span data-ttu-id="094b7-111">**Win32 \_ TSAccount** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="094b7-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="094b7-112">方法</span><span class="sxs-lookup"><span data-stu-id="094b7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="094b7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="094b7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="094b7-114">方法</span><span class="sxs-lookup"><span data-stu-id="094b7-114">Methods</span></span>

<span data-ttu-id="094b7-115">**Win32 \_ TSAccount** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="094b7-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="094b7-116">方法</span><span class="sxs-lookup"><span data-stu-id="094b7-116">Method</span></span>                                                                   | <span data-ttu-id="094b7-117">描述</span><span class="sxs-lookup"><span data-stu-id="094b7-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="094b7-118">**刪除**</span><span class="sxs-lookup"><span data-stu-id="094b7-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="094b7-119">刪除指定的使用者、群組或電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="094b7-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="094b7-120">**ModifyAuditPermissions**</span><span class="sxs-lookup"><span data-stu-id="094b7-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="094b7-121">變更所指定帳戶的 audit 許可權集的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="094b7-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="094b7-122">**ModifyPermissions**</span><span class="sxs-lookup"><span data-stu-id="094b7-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="094b7-123">將更細微的許可權集合設定為指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="094b7-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="094b7-124">屬性</span><span class="sxs-lookup"><span data-stu-id="094b7-124">Properties</span></span>

<span data-ttu-id="094b7-125">**Win32 \_ TSAccount** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="094b7-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="094b7-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="094b7-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="094b7-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="094b7-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="094b7-130">帳戶的目前名稱。</span><span class="sxs-lookup"><span data-stu-id="094b7-130">The current name of the account.</span></span> <span data-ttu-id="094b7-131">包含功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="094b7-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="094b7-132">**AuditFail**</span><span class="sxs-lookup"><span data-stu-id="094b7-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="094b7-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-135">指定針對失敗狀況進行審核的 [遠端桌面工作階段主機服務許可權](terminal-services-permissions.md) 。</span><span class="sxs-lookup"><span data-stu-id="094b7-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="094b7-136">這個屬性的值是位元遮罩，可以設定為 **PermissionsAllowed** 屬性的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="094b7-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="094b7-137">**WINSTATION \_QUERY = 0x1** (0) </span><span class="sxs-lookup"><span data-stu-id="094b7-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="094b7-138">**WINSTATION \_SET = 0x2** (1) </span><span class="sxs-lookup"><span data-stu-id="094b7-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="094b7-139">**WINSTATION \_登出 = 0x4** (2) </span><span class="sxs-lookup"><span data-stu-id="094b7-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="094b7-140">**WINSTATION \_必要的虛擬 \| 標準 \_ 許可權 \_ = 0xF008** (3) </span><span class="sxs-lookup"><span data-stu-id="094b7-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="094b7-141">**WINSTATION \_SHADOW = 0x10** (4) </span><span class="sxs-lookup"><span data-stu-id="094b7-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="094b7-142">**WINSTATION \_LOGON = 0x20** (5) </span><span class="sxs-lookup"><span data-stu-id="094b7-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="094b7-143">**WINSTATION \_MSG = 0x80** (6) </span><span class="sxs-lookup"><span data-stu-id="094b7-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="094b7-144">**WINSTATION \_CONNECT = 0x100** (7) </span><span class="sxs-lookup"><span data-stu-id="094b7-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="094b7-145">**WINSTATION \_DISCONNECT = 0x200** (8) </span><span class="sxs-lookup"><span data-stu-id="094b7-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="094b7-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="094b7-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="094b7-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-149">指定針對成功條件進行審核的 RD 工作階段主機伺服器特定許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="094b7-150">這個屬性的值是位元遮罩，可以設定為 **PermissionsAllowed** 屬性的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="094b7-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="094b7-151">**WINSTATION \_QUERY = 0x1** (0) </span><span class="sxs-lookup"><span data-stu-id="094b7-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="094b7-152">**WINSTATION \_SET = 0x2** (1) </span><span class="sxs-lookup"><span data-stu-id="094b7-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="094b7-153">**WINSTATION \_登出 = 0x4WINSTATION \_ 虛擬 \| 標準 \_ 許可權 \_ 必填 = 0xF008** (2) </span><span class="sxs-lookup"><span data-stu-id="094b7-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="094b7-154">**WINSTATION \_SHADOW = 0x10** (3) </span><span class="sxs-lookup"><span data-stu-id="094b7-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="094b7-155">**WINSTATION \_LOGON = 0x20** (4) </span><span class="sxs-lookup"><span data-stu-id="094b7-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="094b7-156">**WINSTATION \_MSG = 0x80** (5) </span><span class="sxs-lookup"><span data-stu-id="094b7-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="094b7-157">**WINSTATION \_CONNECT = 0x100** (6) </span><span class="sxs-lookup"><span data-stu-id="094b7-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="094b7-158">**WINSTATION \_DISCONNECT = 0x200** (7) </span><span class="sxs-lookup"><span data-stu-id="094b7-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="094b7-159">**標題**</span><span class="sxs-lookup"><span data-stu-id="094b7-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="094b7-162">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="094b7-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="094b7-163">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="094b7-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="094b7-164">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="094b7-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="094b7-165">**說明**</span><span class="sxs-lookup"><span data-stu-id="094b7-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-168">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="094b7-168">Description of the object.</span></span>

<span data-ttu-id="094b7-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="094b7-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="094b7-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="094b7-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-171">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="094b7-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="094b7-173">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="094b7-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="094b7-174">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="094b7-174">The date the object was installed.</span></span> <span data-ttu-id="094b7-175">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="094b7-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="094b7-176">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="094b7-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="094b7-177">**名稱**</span><span class="sxs-lookup"><span data-stu-id="094b7-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-180">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="094b7-180">The name of the object.</span></span>

<span data-ttu-id="094b7-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="094b7-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="094b7-182">**PermissionsAllowed**</span><span class="sxs-lookup"><span data-stu-id="094b7-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="094b7-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-185">指定帳戶允許的 [遠端桌面服務許可權](terminal-services-permissions.md) 。</span><span class="sxs-lookup"><span data-stu-id="094b7-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="094b7-186">這個屬性的值是位元遮罩，可設定為下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="094b7-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="094b7-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION \_QUERY = 0x1** (1) </span><span class="sxs-lookup"><span data-stu-id="094b7-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-188">查詢會話相關資訊的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="094b7-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_設定** (2) </span><span class="sxs-lookup"><span data-stu-id="094b7-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-190">修改連接參數的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="094b7-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_重設** (64) </span><span class="sxs-lookup"><span data-stu-id="094b7-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-192">重設或結束會話或連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="094b7-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_\| \_ \_ 需要** (983048) 的虛擬標準許可權</span><span class="sxs-lookup"><span data-stu-id="094b7-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-194">使用虛擬通道的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-194">Permission to use virtual channels.</span></span> <span data-ttu-id="094b7-195">虛擬通道可讓您從伺服器程式存取用戶端裝置。</span><span class="sxs-lookup"><span data-stu-id="094b7-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="094b7-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_陰影** (16) </span><span class="sxs-lookup"><span data-stu-id="094b7-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-197">陰影或遠端控制另一個使用者會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="094b7-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_登** 入 (32) </span><span class="sxs-lookup"><span data-stu-id="094b7-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-199">登入伺服器上會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="094b7-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_登出** (4) </span><span class="sxs-lookup"><span data-stu-id="094b7-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-201">從會話登出使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="094b7-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_MSG** (128) </span><span class="sxs-lookup"><span data-stu-id="094b7-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-203">將訊息傳送至另一個使用者會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="094b7-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_連接** (256) </span><span class="sxs-lookup"><span data-stu-id="094b7-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-205">連接到另一個會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="094b7-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_中斷** (512) </span><span class="sxs-lookup"><span data-stu-id="094b7-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="094b7-207">中斷會話連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="094b7-208">**PermissionsDenied**</span><span class="sxs-lookup"><span data-stu-id="094b7-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-209">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="094b7-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-211">指定帳戶不允許的 RD 工作階段主機伺服器特定許可權。</span><span class="sxs-lookup"><span data-stu-id="094b7-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="094b7-212">這個屬性的值是位元遮罩，可以設定為 **PermissionsAllowed** 屬性的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="094b7-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="094b7-213">**WINSTATION \_QUERY = 0x1** (0) </span><span class="sxs-lookup"><span data-stu-id="094b7-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="094b7-214">**WINSTATION \_SET = 0x2** (1) </span><span class="sxs-lookup"><span data-stu-id="094b7-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="094b7-215">**WINSTATION \_登出 = 0x4** (2) </span><span class="sxs-lookup"><span data-stu-id="094b7-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="094b7-216">**WINSTATION \_必要的虛擬 \| 標準 \_ 許可權 \_ = 0xF008** (3) </span><span class="sxs-lookup"><span data-stu-id="094b7-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="094b7-217">**WINSTATION \_SHADOW = 0x10** (4) </span><span class="sxs-lookup"><span data-stu-id="094b7-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="094b7-218">**WINSTATION \_LOGON = 0x20** (5) </span><span class="sxs-lookup"><span data-stu-id="094b7-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="094b7-219">**WINSTATION \_MSG = 0x80** (6) </span><span class="sxs-lookup"><span data-stu-id="094b7-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="094b7-220">**WINSTATION \_CONNECT = 0x100** (7) </span><span class="sxs-lookup"><span data-stu-id="094b7-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="094b7-221">**WINSTATION \_DISCONNECT = 0x200** (8) </span><span class="sxs-lookup"><span data-stu-id="094b7-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="094b7-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="094b7-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-225">指定帳戶的 [安全識別碼](/windows/desktop/SecAuthZ/security-identifiers) 。</span><span class="sxs-lookup"><span data-stu-id="094b7-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="094b7-226">**狀態**</span><span class="sxs-lookup"><span data-stu-id="094b7-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="094b7-229">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="094b7-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="094b7-230">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="094b7-230">Current status of the object.</span></span> <span data-ttu-id="094b7-231">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="094b7-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="094b7-232">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="094b7-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="094b7-233">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="094b7-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="094b7-234">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="094b7-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="094b7-235">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="094b7-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="094b7-236">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="094b7-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="094b7-237"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="094b7-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-238"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="094b7-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-239"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="094b7-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-240"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="094b7-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-241"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="094b7-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-242"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="094b7-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-243"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="094b7-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="094b7-244"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="094b7-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="094b7-245">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="094b7-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="094b7-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="094b7-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="094b7-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="094b7-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="094b7-248">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="094b7-248">The name of the terminal.</span></span>

<span data-ttu-id="094b7-249">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="094b7-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="094b7-250">備註</span><span class="sxs-lookup"><span data-stu-id="094b7-250">Remarks</span></span>

<span data-ttu-id="094b7-251">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="094b7-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="094b7-252">針對 C/c + + 呼叫，這會是 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="094b7-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="094b7-253">針對 Visual Basic 和腳本呼叫，這會是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="094b7-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="094b7-254">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="094b7-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="094b7-255">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="094b7-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="094b7-256">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="094b7-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="094b7-257">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="094b7-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="094b7-258">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="094b7-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="094b7-259">規格需求</span><span class="sxs-lookup"><span data-stu-id="094b7-259">Requirements</span></span>



| <span data-ttu-id="094b7-260">需求</span><span class="sxs-lookup"><span data-stu-id="094b7-260">Requirement</span></span> | <span data-ttu-id="094b7-261">值</span><span class="sxs-lookup"><span data-stu-id="094b7-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="094b7-262">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="094b7-262">Minimum supported client</span></span><br/> | <span data-ttu-id="094b7-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="094b7-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="094b7-264">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="094b7-264">Minimum supported server</span></span><br/> | <span data-ttu-id="094b7-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="094b7-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="094b7-266">命名空間</span><span class="sxs-lookup"><span data-stu-id="094b7-266">Namespace</span></span><br/>                | <span data-ttu-id="094b7-267">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="094b7-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="094b7-268">MOF</span><span class="sxs-lookup"><span data-stu-id="094b7-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="094b7-269"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="094b7-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="094b7-270">DLL</span><span class="sxs-lookup"><span data-stu-id="094b7-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="094b7-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="094b7-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094b7-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="094b7-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094b7-273">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="094b7-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

