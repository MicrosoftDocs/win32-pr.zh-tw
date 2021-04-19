---
title: Win32_TSPermissionsSetting 類別
description: 包含將新帳戶新增至終端機的方法，以及將預設許可權還原到終端機的方法。
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Win32_TSPermissionsSetting 類別遠端桌面服務
- Win32_TSPermissionsSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969816"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="a6167-105">Win32 \_ TSPermissionsSetting 類別</span><span class="sxs-lookup"><span data-stu-id="a6167-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="a6167-106">**Win32 \_ TSPermissionsSetting** WMI 類別包含將新帳戶新增至終端機的方法，以及將預設許可權還原到終端機的方法。</span><span class="sxs-lookup"><span data-stu-id="a6167-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="a6167-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a6167-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="a6167-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="a6167-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6167-109">語法</span><span class="sxs-lookup"><span data-stu-id="a6167-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="a6167-110">成員</span><span class="sxs-lookup"><span data-stu-id="a6167-110">Members</span></span>

<span data-ttu-id="a6167-111">**Win32 \_ TSPermissionsSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a6167-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="a6167-112">方法</span><span class="sxs-lookup"><span data-stu-id="a6167-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6167-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a6167-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6167-114">方法</span><span class="sxs-lookup"><span data-stu-id="a6167-114">Methods</span></span>

<span data-ttu-id="a6167-115">**Win32 \_ TSPermissionsSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a6167-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="a6167-116">方法</span><span class="sxs-lookup"><span data-stu-id="a6167-116">Method</span></span>                                                                | <span data-ttu-id="a6167-117">描述</span><span class="sxs-lookup"><span data-stu-id="a6167-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6167-118">**AddAccount**</span><span class="sxs-lookup"><span data-stu-id="a6167-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="a6167-119">使用 *PermissionPreSet* 參數值中指定的許可權集合，將帳戶新增至終端機。</span><span class="sxs-lookup"><span data-stu-id="a6167-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="a6167-120">**RestoreDefaults**</span><span class="sxs-lookup"><span data-stu-id="a6167-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="a6167-121">還原終端機的預設許可權集合值。</span><span class="sxs-lookup"><span data-stu-id="a6167-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="a6167-122">屬性</span><span class="sxs-lookup"><span data-stu-id="a6167-122">Properties</span></span>

<span data-ttu-id="a6167-123">**Win32 \_ TSPermissionsSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a6167-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6167-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="a6167-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6167-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6167-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a6167-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6167-128">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="a6167-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a6167-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6167-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6167-130">**DenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="a6167-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a6167-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6167-133">指定本機系統管理員是否有許可權可自訂。</span><span class="sxs-lookup"><span data-stu-id="a6167-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="a6167-134">**說明**</span><span class="sxs-lookup"><span data-stu-id="a6167-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6167-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6167-137">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a6167-137">Description of the object.</span></span>

<span data-ttu-id="a6167-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6167-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6167-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a6167-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a6167-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6167-142">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="a6167-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a6167-143">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="a6167-143">The date the object was installed.</span></span> <span data-ttu-id="a6167-144">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="a6167-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a6167-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6167-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6167-146">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a6167-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6167-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6167-149">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6167-149">The name of the object.</span></span>

<span data-ttu-id="a6167-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6167-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6167-151">**PolicySourceDenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="a6167-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a6167-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6167-154">指出 **MinEncryptionLevel** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="a6167-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="a6167-155">0</span><span class="sxs-lookup"><span data-stu-id="a6167-155">0</span></span>
</dt> <dd>

<span data-ttu-id="a6167-156">伺服器</span><span class="sxs-lookup"><span data-stu-id="a6167-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="a6167-157">1</span><span class="sxs-lookup"><span data-stu-id="a6167-157">1</span></span>
</dt> <dd>

<span data-ttu-id="a6167-158">群組原則</span><span class="sxs-lookup"><span data-stu-id="a6167-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a6167-159">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a6167-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6167-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6167-162">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="a6167-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a6167-163">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a6167-163">Current status of the object.</span></span> <span data-ttu-id="a6167-164">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="a6167-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a6167-165">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="a6167-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a6167-166">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="a6167-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a6167-167">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="a6167-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a6167-168">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="a6167-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a6167-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6167-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a6167-170"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a6167-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-171"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a6167-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-172"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a6167-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-173"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a6167-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-174"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a6167-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-175"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a6167-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-176"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a6167-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a6167-177"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="a6167-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6167-178">**StringSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a6167-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6167-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6167-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6167-181">與二元位元組陣列格式的終端機相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="a6167-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="a6167-182">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="a6167-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6167-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6167-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6167-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6167-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6167-185">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6167-185">The name of the terminal.</span></span>

<span data-ttu-id="a6167-186">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="a6167-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6167-187">備註</span><span class="sxs-lookup"><span data-stu-id="a6167-187">Remarks</span></span>

<span data-ttu-id="a6167-188">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="a6167-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="a6167-189">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="a6167-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="a6167-190">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="a6167-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="a6167-191">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="a6167-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="a6167-192">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a6167-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a6167-193">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a6167-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a6167-194">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a6167-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a6167-195">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a6167-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6167-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6167-196">Requirements</span></span>



| <span data-ttu-id="a6167-197">需求</span><span class="sxs-lookup"><span data-stu-id="a6167-197">Requirement</span></span> | <span data-ttu-id="a6167-198">值</span><span class="sxs-lookup"><span data-stu-id="a6167-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6167-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6167-199">Minimum supported client</span></span><br/> | <span data-ttu-id="a6167-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6167-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6167-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6167-201">Minimum supported server</span></span><br/> | <span data-ttu-id="a6167-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6167-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6167-203">命名空間</span><span class="sxs-lookup"><span data-stu-id="a6167-203">Namespace</span></span><br/>                | <span data-ttu-id="a6167-204">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a6167-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a6167-205">MOF</span><span class="sxs-lookup"><span data-stu-id="a6167-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6167-206"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6167-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6167-207">DLL</span><span class="sxs-lookup"><span data-stu-id="a6167-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6167-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6167-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6167-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6167-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6167-210">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="a6167-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

