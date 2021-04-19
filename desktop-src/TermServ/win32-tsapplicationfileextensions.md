---
title: Win32_TSApplicationFileExtensions 類別
description: 遠端桌面工作階段主機 (RD 工作階段主機) server 上的應用程式所處理的副檔名。
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Win32_TSApplicationFileExtensions 類別遠端桌面服務
- Win32_TSApplicationFileExtensions 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966147"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="6914a-105">Win32 \_ TSApplicationFileExtensions 類別</span><span class="sxs-lookup"><span data-stu-id="6914a-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="6914a-106">描述遠端桌面工作階段主機 (RD 工作階段主機) server 上的應用程式所處理的副檔名。</span><span class="sxs-lookup"><span data-stu-id="6914a-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6914a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6914a-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="6914a-108">成員</span><span class="sxs-lookup"><span data-stu-id="6914a-108">Members</span></span>

<span data-ttu-id="6914a-109">**Win32 \_ TSApplicationFileExtensions** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6914a-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="6914a-110">方法</span><span class="sxs-lookup"><span data-stu-id="6914a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6914a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6914a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6914a-112">方法</span><span class="sxs-lookup"><span data-stu-id="6914a-112">Methods</span></span>

<span data-ttu-id="6914a-113">**Win32 \_ TSApplicationFileExtensions** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6914a-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="6914a-114">方法</span><span class="sxs-lookup"><span data-stu-id="6914a-114">Method</span></span>                                                                         | <span data-ttu-id="6914a-115">描述</span><span class="sxs-lookup"><span data-stu-id="6914a-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6914a-116">**FileAssociations**</span><span class="sxs-lookup"><span data-stu-id="6914a-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="6914a-117">掃描登錄以取得應用程式目前的檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="6914a-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="6914a-118">**FileExtensions**</span><span class="sxs-lookup"><span data-stu-id="6914a-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="6914a-119">提供應用程式所處理的副檔名清單。</span><span class="sxs-lookup"><span data-stu-id="6914a-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6914a-120">屬性</span><span class="sxs-lookup"><span data-stu-id="6914a-120">Properties</span></span>

<span data-ttu-id="6914a-121">**Win32 \_ TSApplicationFileExtensions** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6914a-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6914a-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="6914a-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6914a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6914a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6914a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6914a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6914a-125">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="6914a-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6914a-126">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="6914a-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6914a-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6914a-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6914a-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="6914a-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6914a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6914a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6914a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6914a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6914a-131">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="6914a-131">Description of the object.</span></span>

<span data-ttu-id="6914a-132">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6914a-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6914a-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6914a-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6914a-134">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6914a-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6914a-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6914a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6914a-136">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="6914a-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6914a-137">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="6914a-137">The date the object was installed.</span></span> <span data-ttu-id="6914a-138">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="6914a-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6914a-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6914a-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6914a-140">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6914a-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6914a-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6914a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6914a-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6914a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6914a-143">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="6914a-143">The name of the object.</span></span>

<span data-ttu-id="6914a-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6914a-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6914a-145">**狀態**</span><span class="sxs-lookup"><span data-stu-id="6914a-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6914a-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6914a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6914a-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6914a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6914a-148">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="6914a-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6914a-149">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6914a-149">Current status of the object.</span></span> <span data-ttu-id="6914a-150">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="6914a-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6914a-151">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="6914a-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6914a-152">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="6914a-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6914a-153">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="6914a-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6914a-154">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="6914a-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6914a-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6914a-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6914a-156"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="6914a-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-157"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="6914a-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-158"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="6914a-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-159"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="6914a-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-160"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="6914a-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-161"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="6914a-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-162"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="6914a-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6914a-163"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="6914a-163">("Service")</span></span>


<span data-ttu-id="6914a-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6914a-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6914a-165">備註</span><span class="sxs-lookup"><span data-stu-id="6914a-165">Remarks</span></span>

<span data-ttu-id="6914a-166">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="6914a-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="6914a-167">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="6914a-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="6914a-168">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="6914a-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="6914a-169">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="6914a-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="6914a-170">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6914a-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6914a-171">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6914a-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6914a-172">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6914a-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6914a-173">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="6914a-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6914a-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="6914a-174">Requirements</span></span>



| <span data-ttu-id="6914a-175">需求</span><span class="sxs-lookup"><span data-stu-id="6914a-175">Requirement</span></span> | <span data-ttu-id="6914a-176">值</span><span class="sxs-lookup"><span data-stu-id="6914a-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6914a-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6914a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="6914a-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6914a-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6914a-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6914a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="6914a-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6914a-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6914a-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="6914a-181">Namespace</span></span><br/>                | <span data-ttu-id="6914a-182">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="6914a-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6914a-183">MOF</span><span class="sxs-lookup"><span data-stu-id="6914a-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6914a-184"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="6914a-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6914a-185">DLL</span><span class="sxs-lookup"><span data-stu-id="6914a-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6914a-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6914a-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

