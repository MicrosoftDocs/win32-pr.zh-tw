---
title: Win32_TSLegacyPlugin 類別
description: 代表內建的 RemoteApp 和桌面連線管理服務外掛程式將會查詢 RemoteApp 程式的遠端桌面伺服器。
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Win32_TSLegacyPlugin 類別遠端桌面服務
- Win32_TSLegacyPlugin 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968533"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="09055-105">Win32 \_ TSLegacyPlugin 類別</span><span class="sxs-lookup"><span data-stu-id="09055-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="09055-106">代表內建的 RemoteApp 和桌面連線管理服務外掛程式將會查詢 RemoteApp 程式的遠端桌面伺服器。</span><span class="sxs-lookup"><span data-stu-id="09055-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="09055-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="09055-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="09055-108">從 Windows Server 2012 開始，這個類別已被取代。</span><span class="sxs-lookup"><span data-stu-id="09055-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="09055-109">語法</span><span class="sxs-lookup"><span data-stu-id="09055-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="09055-110">成員</span><span class="sxs-lookup"><span data-stu-id="09055-110">Members</span></span>

<span data-ttu-id="09055-111">**Win32 \_ TSLegacyPlugin** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="09055-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="09055-112">屬性</span><span class="sxs-lookup"><span data-stu-id="09055-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09055-113">屬性</span><span class="sxs-lookup"><span data-stu-id="09055-113">Properties</span></span>

<span data-ttu-id="09055-114">**Win32 \_ TSLegacyPlugin** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="09055-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09055-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="09055-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09055-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09055-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09055-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09055-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09055-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="09055-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="09055-119">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="09055-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="09055-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="09055-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09055-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="09055-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09055-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09055-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09055-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09055-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09055-124">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="09055-124">Description of the object.</span></span>

<span data-ttu-id="09055-125">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="09055-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09055-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="09055-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09055-127">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="09055-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09055-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09055-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09055-129">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="09055-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="09055-130">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="09055-130">The date the object was installed.</span></span> <span data-ttu-id="09055-131">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="09055-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="09055-132">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="09055-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09055-133">**名稱**</span><span class="sxs-lookup"><span data-stu-id="09055-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09055-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09055-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09055-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09055-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09055-136">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="09055-136">The name of the object.</span></span>

<span data-ttu-id="09055-137">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="09055-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09055-138">**狀態**</span><span class="sxs-lookup"><span data-stu-id="09055-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09055-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09055-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09055-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09055-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09055-141">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="09055-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="09055-142">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="09055-142">Current status of the object.</span></span> <span data-ttu-id="09055-143">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="09055-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="09055-144">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="09055-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="09055-145">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="09055-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="09055-146">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="09055-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="09055-147">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="09055-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="09055-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="09055-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="09055-149"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="09055-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-150"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="09055-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-151"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="09055-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-152"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="09055-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-153"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="09055-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-154"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="09055-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-155"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="09055-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="09055-156"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="09055-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="09055-157">**型別**</span><span class="sxs-lookup"><span data-stu-id="09055-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09055-158">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="09055-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09055-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="09055-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="09055-160">遠端桌面服務伺服器的型別。</span><span class="sxs-lookup"><span data-stu-id="09055-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="09055-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**終端機伺服器 (0)** (0) </span><span class="sxs-lookup"><span data-stu-id="09055-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="09055-162">遠端桌面伺服器。</span><span class="sxs-lookup"><span data-stu-id="09055-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="09055-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**VM 伺服器陣列的虛擬終端機伺服器 (1)** (1) </span><span class="sxs-lookup"><span data-stu-id="09055-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="09055-164">VM 伺服器陣列的人工遠端桌面伺服器。</span><span class="sxs-lookup"><span data-stu-id="09055-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09055-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="09055-165">Requirements</span></span>



| <span data-ttu-id="09055-166">需求</span><span class="sxs-lookup"><span data-stu-id="09055-166">Requirement</span></span> | <span data-ttu-id="09055-167">值</span><span class="sxs-lookup"><span data-stu-id="09055-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09055-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09055-168">Minimum supported client</span></span><br/> | <span data-ttu-id="09055-169">都不支援</span><span class="sxs-lookup"><span data-stu-id="09055-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="09055-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09055-170">Minimum supported server</span></span><br/> | <span data-ttu-id="09055-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09055-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="09055-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="09055-172">Namespace</span></span><br/>                | <span data-ttu-id="09055-173">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="09055-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="09055-174">MOF</span><span class="sxs-lookup"><span data-stu-id="09055-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09055-175"><dt>TscPub mof</dt></span><span class="sxs-lookup"><span data-stu-id="09055-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="09055-176">DLL</span><span class="sxs-lookup"><span data-stu-id="09055-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09055-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09055-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

