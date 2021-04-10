---
title: Win32_TSStartMenuApplication 類別
description: 描述 [開始] 功能表遠端桌面工作階段主機 (RD 工作階段主機) server 上的應用程式。
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Win32_TSStartMenuApplication 類別遠端桌面服務
- Win32_TSStartMenuApplication 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686475"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="07a44-105">Win32 \_ TSStartMenuApplication 類別</span><span class="sxs-lookup"><span data-stu-id="07a44-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="07a44-106">描述 [開始] 功能表遠端桌面工作階段主機 (RD 工作階段主機) server 上的應用程式。</span><span class="sxs-lookup"><span data-stu-id="07a44-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a44-107">語法</span><span class="sxs-lookup"><span data-stu-id="07a44-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="07a44-108">成員</span><span class="sxs-lookup"><span data-stu-id="07a44-108">Members</span></span>

<span data-ttu-id="07a44-109">**Win32 \_ TSStartMenuApplication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="07a44-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="07a44-110">屬性</span><span class="sxs-lookup"><span data-stu-id="07a44-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07a44-111">屬性</span><span class="sxs-lookup"><span data-stu-id="07a44-111">Properties</span></span>

<span data-ttu-id="07a44-112">**Win32 \_ TSStartMenuApplication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="07a44-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07a44-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="07a44-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07a44-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="07a44-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="07a44-117">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="07a44-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="07a44-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07a44-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07a44-119">**CommandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="07a44-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07a44-122">要使用的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="07a44-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="07a44-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="07a44-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07a44-126">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="07a44-126">Description of the object.</span></span>

<span data-ttu-id="07a44-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07a44-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07a44-128">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="07a44-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="07a44-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07a44-131">圖示的索引或識別碼。</span><span class="sxs-lookup"><span data-stu-id="07a44-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="07a44-132">**>iconpath**</span><span class="sxs-lookup"><span data-stu-id="07a44-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07a44-135">應用程式圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="07a44-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="07a44-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07a44-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-137">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="07a44-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07a44-139">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="07a44-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="07a44-140">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="07a44-140">The date the object was installed.</span></span> <span data-ttu-id="07a44-141">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="07a44-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="07a44-142">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07a44-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07a44-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="07a44-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07a44-146">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="07a44-146">The name of the object.</span></span>

<span data-ttu-id="07a44-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07a44-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07a44-148">**路徑**</span><span class="sxs-lookup"><span data-stu-id="07a44-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07a44-151">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="07a44-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="07a44-152">應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="07a44-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="07a44-153">**狀態**</span><span class="sxs-lookup"><span data-stu-id="07a44-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07a44-156">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="07a44-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="07a44-157">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="07a44-157">Current status of the object.</span></span> <span data-ttu-id="07a44-158">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="07a44-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="07a44-159">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="07a44-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="07a44-160">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="07a44-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="07a44-161">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="07a44-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="07a44-162">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="07a44-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="07a44-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07a44-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="07a44-164"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="07a44-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-165"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="07a44-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-166"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="07a44-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-167"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="07a44-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-168"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="07a44-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-169"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="07a44-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-170"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="07a44-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="07a44-171"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="07a44-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07a44-172">**VPath**</span><span class="sxs-lookup"><span data-stu-id="07a44-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07a44-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07a44-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07a44-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07a44-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07a44-175">應用程式的虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="07a44-175">The virtual path of the application.</span></span> <span data-ttu-id="07a44-176">這包括系統內容變數，例如% windir%。</span><span class="sxs-lookup"><span data-stu-id="07a44-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07a44-177">備註</span><span class="sxs-lookup"><span data-stu-id="07a44-177">Remarks</span></span>

<span data-ttu-id="07a44-178">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="07a44-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="07a44-179">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="07a44-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="07a44-180">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="07a44-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="07a44-181">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="07a44-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="07a44-182">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="07a44-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="07a44-183">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="07a44-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="07a44-184">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="07a44-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="07a44-185">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="07a44-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="07a44-186">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="07a44-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="07a44-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="07a44-187">Requirements</span></span>



| <span data-ttu-id="07a44-188">需求</span><span class="sxs-lookup"><span data-stu-id="07a44-188">Requirement</span></span> | <span data-ttu-id="07a44-189">值</span><span class="sxs-lookup"><span data-stu-id="07a44-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a44-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07a44-190">Minimum supported client</span></span><br/> | <span data-ttu-id="07a44-191">都不支援</span><span class="sxs-lookup"><span data-stu-id="07a44-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="07a44-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07a44-192">Minimum supported server</span></span><br/> | <span data-ttu-id="07a44-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a44-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07a44-194">命名空間</span><span class="sxs-lookup"><span data-stu-id="07a44-194">Namespace</span></span><br/>                | <span data-ttu-id="07a44-195">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="07a44-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="07a44-196">MOF</span><span class="sxs-lookup"><span data-stu-id="07a44-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07a44-197"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="07a44-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="07a44-198">DLL</span><span class="sxs-lookup"><span data-stu-id="07a44-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a44-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a44-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

