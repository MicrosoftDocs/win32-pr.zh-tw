---
title: Win32_Workspace 類別
description: 指定遠端桌面服務工作區設定資訊。
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Win32_Workspace 類別遠端桌面服務
- Win32_Workspace 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965474"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="069f7-105">Win32 \_ Workspace 類別</span><span class="sxs-lookup"><span data-stu-id="069f7-105">Win32\_Workspace class</span></span>

<span data-ttu-id="069f7-106">指定遠端桌面服務工作區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="069f7-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="069f7-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="069f7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="069f7-108">語法</span><span class="sxs-lookup"><span data-stu-id="069f7-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="069f7-109">成員</span><span class="sxs-lookup"><span data-stu-id="069f7-109">Members</span></span>

<span data-ttu-id="069f7-110">**Win32 \_ Workspace** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="069f7-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="069f7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="069f7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="069f7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="069f7-112">Properties</span></span>

<span data-ttu-id="069f7-113">**Win32 \_ Workspace** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="069f7-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="069f7-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="069f7-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069f7-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069f7-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="069f7-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="069f7-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="069f7-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="069f7-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="069f7-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069f7-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="069f7-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069f7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069f7-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="069f7-123">Description of the object.</span></span>

<span data-ttu-id="069f7-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="069f7-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069f7-125">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="069f7-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="069f7-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="069f7-128">工作區的識別碼。</span><span class="sxs-lookup"><span data-stu-id="069f7-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="069f7-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="069f7-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-130">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="069f7-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069f7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069f7-132">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="069f7-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="069f7-133">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="069f7-133">The date the object was installed.</span></span> <span data-ttu-id="069f7-134">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="069f7-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="069f7-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="069f7-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069f7-136">**IsDefaultName**</span><span class="sxs-lookup"><span data-stu-id="069f7-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="069f7-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069f7-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069f7-139">指定工作區名稱是否為預設名稱。</span><span class="sxs-lookup"><span data-stu-id="069f7-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="069f7-140">如果名稱為預設名稱，則包含非零，否則為零。</span><span class="sxs-lookup"><span data-stu-id="069f7-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="069f7-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="069f7-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069f7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069f7-144">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="069f7-144">The name of the object.</span></span>

<span data-ttu-id="069f7-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="069f7-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069f7-146">**轉向器**</span><span class="sxs-lookup"><span data-stu-id="069f7-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="069f7-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="069f7-149">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="069f7-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="069f7-150">工作區之重新導向程式的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="069f7-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="069f7-151">**RedirectorAlternateAddress**</span><span class="sxs-lookup"><span data-stu-id="069f7-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="069f7-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="069f7-154">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="069f7-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="069f7-155">重新導向程式的替代位址。</span><span class="sxs-lookup"><span data-stu-id="069f7-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="069f7-156">**狀態**</span><span class="sxs-lookup"><span data-stu-id="069f7-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069f7-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069f7-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069f7-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069f7-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069f7-159">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="069f7-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="069f7-160">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="069f7-160">Current status of the object.</span></span> <span data-ttu-id="069f7-161">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="069f7-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="069f7-162">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="069f7-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="069f7-163">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="069f7-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="069f7-164">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="069f7-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="069f7-165">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="069f7-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="069f7-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="069f7-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="069f7-167"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="069f7-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-168"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="069f7-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-169"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="069f7-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-170"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="069f7-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-171"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="069f7-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-172"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="069f7-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-173"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="069f7-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="069f7-174"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="069f7-174">("Service")</span></span>


<span data-ttu-id="069f7-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="069f7-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="069f7-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="069f7-176">Requirements</span></span>



| <span data-ttu-id="069f7-177">需求</span><span class="sxs-lookup"><span data-stu-id="069f7-177">Requirement</span></span> | <span data-ttu-id="069f7-178">值</span><span class="sxs-lookup"><span data-stu-id="069f7-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="069f7-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="069f7-179">Minimum supported client</span></span><br/> | <span data-ttu-id="069f7-180">都不支援</span><span class="sxs-lookup"><span data-stu-id="069f7-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="069f7-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="069f7-181">Minimum supported server</span></span><br/> | <span data-ttu-id="069f7-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="069f7-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="069f7-183">命名空間</span><span class="sxs-lookup"><span data-stu-id="069f7-183">Namespace</span></span><br/>                | <span data-ttu-id="069f7-184">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="069f7-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="069f7-185">MOF</span><span class="sxs-lookup"><span data-stu-id="069f7-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="069f7-186"><dt>TscPub mof</dt></span><span class="sxs-lookup"><span data-stu-id="069f7-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="069f7-187">DLL</span><span class="sxs-lookup"><span data-stu-id="069f7-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="069f7-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="069f7-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

