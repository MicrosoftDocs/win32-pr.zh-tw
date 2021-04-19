---
title: Win32_TSNetworkAdapterListSetting 類別
description: '\_根據指定的終端通訊協定和傳輸方法，列舉可針對 Win32 終端機設定的網路介面卡清單。'
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterListSetting 類別遠端桌面服務
- Win32_TSNetworkAdapterListSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106978596"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="d18ab-105">Win32 \_ TSNetworkAdapterListSetting 類別</span><span class="sxs-lookup"><span data-stu-id="d18ab-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="d18ab-106">**Win32 \_ TSNetworkAdapterListSetting** WMI 類別會根據指定的終端通訊協定和傳輸方法，列舉可針對 [**Win32 \_ 終端**](win32-terminal.md)機設定的網路介面卡清單。</span><span class="sxs-lookup"><span data-stu-id="d18ab-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="d18ab-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d18ab-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18ab-108">語法</span><span class="sxs-lookup"><span data-stu-id="d18ab-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="d18ab-109">成員</span><span class="sxs-lookup"><span data-stu-id="d18ab-109">Members</span></span>

<span data-ttu-id="d18ab-110">**Win32 \_ TSNetworkAdapterListSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d18ab-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d18ab-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d18ab-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d18ab-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d18ab-112">Properties</span></span>

<span data-ttu-id="d18ab-113">**Win32 \_ TSNetworkAdapterListSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d18ab-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d18ab-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="d18ab-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d18ab-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="d18ab-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d18ab-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d18ab-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="d18ab-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d18ab-123">Description of the object.</span></span>

<span data-ttu-id="d18ab-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d18ab-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d18ab-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d18ab-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="d18ab-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="d18ab-129">The date the object was installed.</span></span> <span data-ttu-id="d18ab-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d18ab-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d18ab-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d18ab-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d18ab-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-135">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="d18ab-135">The name of the object.</span></span>

<span data-ttu-id="d18ab-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d18ab-137">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="d18ab-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-140">網路介面卡的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d18ab-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d18ab-141">**NetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="d18ab-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-144">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d18ab-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-145">網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d18ab-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d18ab-146">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d18ab-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-149">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="d18ab-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-150">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d18ab-150">Current status of the object.</span></span> <span data-ttu-id="d18ab-151">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="d18ab-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d18ab-152">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="d18ab-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d18ab-153">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d18ab-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d18ab-154">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="d18ab-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d18ab-155">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d18ab-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d18ab-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d18ab-157"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-158"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-159"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-160"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-161"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-162"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-163"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d18ab-164"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="d18ab-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d18ab-165">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="d18ab-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18ab-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d18ab-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d18ab-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d18ab-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d18ab-168">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="d18ab-168">The name of the terminal.</span></span>

<span data-ttu-id="d18ab-169">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d18ab-170">備註</span><span class="sxs-lookup"><span data-stu-id="d18ab-170">Remarks</span></span>

<span data-ttu-id="d18ab-171">若要連接到「根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway」命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="d18ab-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d18ab-172">針對 C/c + + 呼叫，這會是 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="d18ab-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d18ab-173">針對 Visual Basic 和腳本呼叫，這會是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="d18ab-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d18ab-174">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="d18ab-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d18ab-175">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d18ab-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d18ab-176">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d18ab-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d18ab-177">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d18ab-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d18ab-178">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d18ab-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d18ab-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="d18ab-179">Requirements</span></span>



| <span data-ttu-id="d18ab-180">需求</span><span class="sxs-lookup"><span data-stu-id="d18ab-180">Requirement</span></span> | <span data-ttu-id="d18ab-181">值</span><span class="sxs-lookup"><span data-stu-id="d18ab-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d18ab-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d18ab-182">Minimum supported client</span></span><br/> | <span data-ttu-id="d18ab-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d18ab-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d18ab-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d18ab-184">Minimum supported server</span></span><br/> | <span data-ttu-id="d18ab-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d18ab-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d18ab-186">命名空間</span><span class="sxs-lookup"><span data-stu-id="d18ab-186">Namespace</span></span><br/>                | <span data-ttu-id="d18ab-187">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d18ab-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d18ab-188">MOF</span><span class="sxs-lookup"><span data-stu-id="d18ab-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d18ab-189"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d18ab-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d18ab-190">DLL</span><span class="sxs-lookup"><span data-stu-id="d18ab-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d18ab-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d18ab-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18ab-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d18ab-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18ab-193">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="d18ab-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="d18ab-194">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="d18ab-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

