---
title: Win32_TSRemoteDesktop 類別
description: 描述可透過遠端桌面 Web 存取 (RD Web 存取) 取得的遠端桌面連線。
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteDesktop 類別遠端桌面服務
- Win32_TSRemoteDesktop 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093955"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="ed2f5-105">Win32 \_ TSRemoteDesktop 類別</span><span class="sxs-lookup"><span data-stu-id="ed2f5-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="ed2f5-106">描述可透過遠端桌面 Web 存取 (RD Web 存取) 取得的遠端桌面連線。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2f5-107">語法</span><span class="sxs-lookup"><span data-stu-id="ed2f5-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="ed2f5-108">成員</span><span class="sxs-lookup"><span data-stu-id="ed2f5-108">Members</span></span>

<span data-ttu-id="ed2f5-109">**Win32 \_ TSRemoteDesktop** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ed2f5-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="ed2f5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ed2f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed2f5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ed2f5-111">Properties</span></span>

<span data-ttu-id="ed2f5-112">**Win32 \_ TSRemoteDesktop** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed2f5-113">**別名**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-116">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-117">遠端桌面連線的別名。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed2f5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-122">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ed2f5-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed2f5-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-127">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-127">Description of the object.</span></span>

<span data-ttu-id="ed2f5-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-129">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-130">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="ed2f5-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed2f5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-132">圖示的位元組內容，對應到遠端桌面連線。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-133">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-134">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-136">遠端桌面連線圖示的索引或識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-137">**>iconpath**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-140">遠端桌面連線圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-142">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed2f5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-144">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="ed2f5-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-145">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-145">The date the object was installed.</span></span> <span data-ttu-id="ed2f5-146">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ed2f5-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-148">**IsVmFarm**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-149">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-151">指出此遠端桌面連線是否為虛擬機器伺服器陣列的一部分。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-152">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed2f5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-155">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-155">The name of the object.</span></span>

<span data-ttu-id="ed2f5-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-157">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-160">對應到遠端桌面連線之 RDP 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-164">控制遠端桌面連線存取的安全描述項（SDDL 格式）。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="ed2f5-165">空字串表示允許所有存取。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-165">An empty string implies allow all access.</span></span> <span data-ttu-id="ed2f5-166">此安全描述項不支援拒絕 Ace 或參考非網域使用者或群組的 Ace。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-167">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-170">指出是否應該在 RD Web 存取中顯示遠端桌面連線。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="ed2f5-171">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed2f5-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-174">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-175">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-175">Current status of the object.</span></span> <span data-ttu-id="ed2f5-176">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ed2f5-177">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ed2f5-178">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ed2f5-179">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ed2f5-180">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ed2f5-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ed2f5-182"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-183"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-184"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-185"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-186"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-187"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-188"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed2f5-189"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="ed2f5-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed2f5-190">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2f5-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed2f5-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2f5-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed2f5-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed2f5-193">遠端桌面連線的虛擬機器伺服器陣列設定。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed2f5-194">備註</span><span class="sxs-lookup"><span data-stu-id="ed2f5-194">Remarks</span></span>

<span data-ttu-id="ed2f5-195">您必須是 Administrators 群組的成員，才能使用這個類別來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="ed2f5-196">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ed2f5-197">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="ed2f5-198">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ed2f5-199">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ed2f5-200">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed2f5-201">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ed2f5-202">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed2f5-203">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="ed2f5-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2f5-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed2f5-204">Requirements</span></span>



| <span data-ttu-id="ed2f5-205">需求</span><span class="sxs-lookup"><span data-stu-id="ed2f5-205">Requirement</span></span> | <span data-ttu-id="ed2f5-206">值</span><span class="sxs-lookup"><span data-stu-id="ed2f5-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2f5-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed2f5-207">Minimum supported client</span></span><br/> | <span data-ttu-id="ed2f5-208">都不支援</span><span class="sxs-lookup"><span data-stu-id="ed2f5-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ed2f5-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed2f5-209">Minimum supported server</span></span><br/> | <span data-ttu-id="ed2f5-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed2f5-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed2f5-211">命名空間</span><span class="sxs-lookup"><span data-stu-id="ed2f5-211">Namespace</span></span><br/>                | <span data-ttu-id="ed2f5-212">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ed2f5-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ed2f5-213">MOF</span><span class="sxs-lookup"><span data-stu-id="ed2f5-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed2f5-214"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed2f5-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="ed2f5-215">DLL</span><span class="sxs-lookup"><span data-stu-id="ed2f5-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed2f5-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed2f5-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

