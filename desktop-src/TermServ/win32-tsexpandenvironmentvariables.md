---
title: Win32_TSExpandEnvironmentVariables 類別
description: 展開系統定義的環境變數。 |Win32_TSExpandEnvironmentVariables 類別
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Win32_TSExpandEnvironmentVariables 類別遠端桌面服務
- Win32_TSExpandEnvironmentVariables 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853791"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="816c6-106">Win32 \_ TSExpandEnvironmentVariables 類別</span><span class="sxs-lookup"><span data-stu-id="816c6-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="816c6-107">展開系統定義的環境變數。</span><span class="sxs-lookup"><span data-stu-id="816c6-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="816c6-108">語法</span><span class="sxs-lookup"><span data-stu-id="816c6-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="816c6-109">成員</span><span class="sxs-lookup"><span data-stu-id="816c6-109">Members</span></span>

<span data-ttu-id="816c6-110">**Win32 \_ TSExpandEnvironmentVariables** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="816c6-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="816c6-111">方法</span><span class="sxs-lookup"><span data-stu-id="816c6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="816c6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="816c6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="816c6-113">方法</span><span class="sxs-lookup"><span data-stu-id="816c6-113">Methods</span></span>

<span data-ttu-id="816c6-114">**Win32 \_ TSExpandEnvironmentVariables** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="816c6-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="816c6-115">方法</span><span class="sxs-lookup"><span data-stu-id="816c6-115">Method</span></span>                                                                                  | <span data-ttu-id="816c6-116">描述</span><span class="sxs-lookup"><span data-stu-id="816c6-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="816c6-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="816c6-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="816c6-118">展開系統定義的環境變數。</span><span class="sxs-lookup"><span data-stu-id="816c6-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="816c6-119">屬性</span><span class="sxs-lookup"><span data-stu-id="816c6-119">Properties</span></span>

<span data-ttu-id="816c6-120">**Win32 \_ TSExpandEnvironmentVariables** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="816c6-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="816c6-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="816c6-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c6-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c6-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816c6-124">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="816c6-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="816c6-125">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="816c6-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="816c6-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c6-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c6-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="816c6-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c6-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c6-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="816c6-130">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="816c6-130">Description of the object.</span></span>

<span data-ttu-id="816c6-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c6-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c6-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="816c6-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c6-133">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="816c6-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="816c6-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816c6-135">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="816c6-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="816c6-136">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="816c6-136">The date the object was installed.</span></span> <span data-ttu-id="816c6-137">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="816c6-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="816c6-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c6-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c6-139">**名稱**</span><span class="sxs-lookup"><span data-stu-id="816c6-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c6-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c6-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c6-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="816c6-142">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="816c6-142">The name of the object.</span></span>

<span data-ttu-id="816c6-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c6-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c6-144">**狀態**</span><span class="sxs-lookup"><span data-stu-id="816c6-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c6-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c6-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c6-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c6-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816c6-147">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="816c6-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="816c6-148">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="816c6-148">Current status of the object.</span></span> <span data-ttu-id="816c6-149">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="816c6-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="816c6-150">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="816c6-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="816c6-151">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="816c6-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="816c6-152">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="816c6-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="816c6-153">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="816c6-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="816c6-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c6-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="816c6-155"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="816c6-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-156"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="816c6-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-157"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="816c6-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-158"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="816c6-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-159"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="816c6-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-160"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="816c6-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-161"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="816c6-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c6-162"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="816c6-162">("Service")</span></span>


<span data-ttu-id="816c6-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="816c6-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="816c6-164">備註</span><span class="sxs-lookup"><span data-stu-id="816c6-164">Remarks</span></span>

<span data-ttu-id="816c6-165">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="816c6-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="816c6-166">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="816c6-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="816c6-167">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="816c6-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="816c6-168">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="816c6-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="816c6-169">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="816c6-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="816c6-170">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="816c6-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="816c6-171">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="816c6-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="816c6-172">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="816c6-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="816c6-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="816c6-173">Requirements</span></span>



| <span data-ttu-id="816c6-174">需求</span><span class="sxs-lookup"><span data-stu-id="816c6-174">Requirement</span></span> | <span data-ttu-id="816c6-175">值</span><span class="sxs-lookup"><span data-stu-id="816c6-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="816c6-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="816c6-176">Minimum supported client</span></span><br/> | <span data-ttu-id="816c6-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="816c6-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="816c6-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="816c6-178">Minimum supported server</span></span><br/> | <span data-ttu-id="816c6-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="816c6-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="816c6-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="816c6-180">Namespace</span></span><br/>                | <span data-ttu-id="816c6-181">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="816c6-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="816c6-182">MOF</span><span class="sxs-lookup"><span data-stu-id="816c6-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="816c6-183"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="816c6-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="816c6-184">DLL</span><span class="sxs-lookup"><span data-stu-id="816c6-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="816c6-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="816c6-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

