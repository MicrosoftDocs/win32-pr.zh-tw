---
title: Win32_TSPublishedApplicationList 類別
description: 代表遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上 [RemoteApp 程式] 清單中的程式清單。
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplicationList 類別遠端桌面服務
- Win32_TSPublishedApplicationList 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024963"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="f8eef-105">Win32 \_ TSPublishedApplicationList 類別</span><span class="sxs-lookup"><span data-stu-id="f8eef-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="f8eef-106">代表遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上 [RemoteApp 程式] 清單中的程式清單。</span><span class="sxs-lookup"><span data-stu-id="f8eef-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8eef-107">語法</span><span class="sxs-lookup"><span data-stu-id="f8eef-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="f8eef-108">成員</span><span class="sxs-lookup"><span data-stu-id="f8eef-108">Members</span></span>

<span data-ttu-id="f8eef-109">**Win32 \_ TSPublishedApplicationList** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f8eef-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="f8eef-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f8eef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8eef-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f8eef-111">Properties</span></span>

<span data-ttu-id="f8eef-112">**Win32 \_ TSPublishedApplicationList** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f8eef-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8eef-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="f8eef-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f8eef-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f8eef-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f8eef-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-117">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="f8eef-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f8eef-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f8eef-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="f8eef-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f8eef-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f8eef-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-122">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f8eef-122">Description of the object.</span></span>

<span data-ttu-id="f8eef-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f8eef-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-124">**Disabled**</span><span class="sxs-lookup"><span data-stu-id="f8eef-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-125">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f8eef-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f8eef-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-127">指出 RD 工作階段主機伺服器是否會在初始連線至 [RemoteApp 程式] 清單中的程式時，限制使用者可以啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="f8eef-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8eef-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-129">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f8eef-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f8eef-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-131">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="f8eef-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-132">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="f8eef-132">The date the object was installed.</span></span> <span data-ttu-id="f8eef-133">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="f8eef-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f8eef-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f8eef-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-135">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f8eef-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f8eef-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f8eef-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-138">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8eef-138">The name of the object.</span></span>

<span data-ttu-id="f8eef-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f8eef-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-140">**PolicySourceDisabled**</span><span class="sxs-lookup"><span data-stu-id="f8eef-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f8eef-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f8eef-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-143">指出已 **停用** 屬性的設定位置。</span><span class="sxs-lookup"><span data-stu-id="f8eef-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="f8eef-144">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="f8eef-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="f8eef-145">0</span><span class="sxs-lookup"><span data-stu-id="f8eef-145">0</span></span>
</dt> <dd>

<span data-ttu-id="f8eef-146">您可以透過 RemoteApp 管理員或 RemoteApp WMI 提供者，在伺服器上設定此設定。</span><span class="sxs-lookup"><span data-stu-id="f8eef-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-147">1</span><span class="sxs-lookup"><span data-stu-id="f8eef-147">1</span></span>
</dt> <dd>

<span data-ttu-id="f8eef-148">設定是透過群組原則來設定。</span><span class="sxs-lookup"><span data-stu-id="f8eef-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="f8eef-149">2</span><span class="sxs-lookup"><span data-stu-id="f8eef-149">2</span></span>
</dt> <dd>

<span data-ttu-id="f8eef-150">未設定此設定。</span><span class="sxs-lookup"><span data-stu-id="f8eef-150">The setting is not configured.</span></span> <span data-ttu-id="f8eef-151">預設值 **FALSE** 會用於 **停用** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="f8eef-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f8eef-152">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f8eef-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8eef-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f8eef-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f8eef-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8eef-155">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="f8eef-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f8eef-156">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f8eef-156">Current status of the object.</span></span> <span data-ttu-id="f8eef-157">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="f8eef-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f8eef-158">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="f8eef-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f8eef-159">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f8eef-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f8eef-160">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="f8eef-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f8eef-161">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f8eef-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f8eef-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f8eef-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f8eef-163"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-164"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-165"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-166"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-167"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-168"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-169"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8eef-170"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="f8eef-170">("Service")</span></span>


<span data-ttu-id="f8eef-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f8eef-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f8eef-172">備註</span><span class="sxs-lookup"><span data-stu-id="f8eef-172">Remarks</span></span>

<span data-ttu-id="f8eef-173">您必須是 Administrators 群組的成員，才能使用這個類別來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="f8eef-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="f8eef-174">[ **已停用** ] 屬性不會防止使用者在使用 RemoteApp 程式連線到 RD 工作階段主機伺服器之後，從遠端啟動未列出的程式。</span><span class="sxs-lookup"><span data-stu-id="f8eef-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="f8eef-175">只有在下列登錄專案遺失時， **已停用** 的屬性才會設定為2的值：</span><span class="sxs-lookup"><span data-stu-id="f8eef-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="f8eef-176">**HKEY \_LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WindowsNT** \\ **CurrentVersion** \\ **TerminalServer** \\ **TSAppAllowList** \\ **fDisabledAllowList**</span><span class="sxs-lookup"><span data-stu-id="f8eef-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="f8eef-177">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="f8eef-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f8eef-178">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="f8eef-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="f8eef-179">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="f8eef-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f8eef-180">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="f8eef-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f8eef-181">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f8eef-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8eef-182">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f8eef-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f8eef-183">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f8eef-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8eef-184">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f8eef-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8eef-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8eef-185">Requirements</span></span>



| <span data-ttu-id="f8eef-186">需求</span><span class="sxs-lookup"><span data-stu-id="f8eef-186">Requirement</span></span> | <span data-ttu-id="f8eef-187">值</span><span class="sxs-lookup"><span data-stu-id="f8eef-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8eef-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8eef-188">Minimum supported client</span></span><br/> | <span data-ttu-id="f8eef-189">都不支援</span><span class="sxs-lookup"><span data-stu-id="f8eef-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f8eef-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8eef-190">Minimum supported server</span></span><br/> | <span data-ttu-id="f8eef-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8eef-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8eef-192">命名空間</span><span class="sxs-lookup"><span data-stu-id="f8eef-192">Namespace</span></span><br/>                | <span data-ttu-id="f8eef-193">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="f8eef-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f8eef-194">MOF</span><span class="sxs-lookup"><span data-stu-id="f8eef-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8eef-195"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8eef-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f8eef-196">DLL</span><span class="sxs-lookup"><span data-stu-id="f8eef-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8eef-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8eef-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

