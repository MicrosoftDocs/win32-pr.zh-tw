---
description: 描述虛擬系統透過一組虛擬化特定屬性的虛擬層面。 CIM \_ VirtualSystemSettingData 也可作為虛擬系統組態的最上層類別。
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984628"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="caeb2-104">CIM \_ VirtualSystemSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="caeb2-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="caeb2-105">描述虛擬系統透過一組虛擬化特定屬性的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="caeb2-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="caeb2-106">**CIM \_VirtualSystemSettingData** 也可作為虛擬系統組態的最上層類別。</span><span class="sxs-lookup"><span data-stu-id="caeb2-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="caeb2-107">語法</span><span class="sxs-lookup"><span data-stu-id="caeb2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="caeb2-108">成員</span><span class="sxs-lookup"><span data-stu-id="caeb2-108">Members</span></span>

<span data-ttu-id="caeb2-109">**CIM \_ VirtualSystemSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="caeb2-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="caeb2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="caeb2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="caeb2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="caeb2-111">Properties</span></span>

<span data-ttu-id="caeb2-112">**CIM \_ VirtualSystemSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="caeb2-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="caeb2-113">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="caeb2-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="caeb2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-116">當虛擬系統執行的軟體失敗時，對虛擬系統採取的動作。</span><span class="sxs-lookup"><span data-stu-id="caeb2-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="caeb2-117">這個屬性所解決的失敗只包含主機平臺可偵測的失敗，例如無法中斷的等候狀態條件。</span><span class="sxs-lookup"><span data-stu-id="caeb2-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="caeb2-118">**無** (2) </span><span class="sxs-lookup"><span data-stu-id="caeb2-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="caeb2-119"> (3) **重新開機**</span><span class="sxs-lookup"><span data-stu-id="caeb2-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="caeb2-120">**還原為 snapshot** (4) </span><span class="sxs-lookup"><span data-stu-id="caeb2-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="caeb2-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="caeb2-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="caeb2-122">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="caeb2-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="caeb2-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-125">當主機關閉時，要對虛擬系統採取的動作。</span><span class="sxs-lookup"><span data-stu-id="caeb2-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="caeb2-126">**關閉** (2) </span><span class="sxs-lookup"><span data-stu-id="caeb2-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="caeb2-127">**儲存狀態** (3) </span><span class="sxs-lookup"><span data-stu-id="caeb2-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="caeb2-128">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="caeb2-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="caeb2-129">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="caeb2-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="caeb2-130">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="caeb2-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="caeb2-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-133">當主機啟動時，要在虛擬系統上採取的動作。</span><span class="sxs-lookup"><span data-stu-id="caeb2-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="caeb2-134">**無** (2) </span><span class="sxs-lookup"><span data-stu-id="caeb2-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="caeb2-135">**如果先前** 作用中的 (3) 重新開機</span><span class="sxs-lookup"><span data-stu-id="caeb2-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="caeb2-136">**一律啟動** (4) </span><span class="sxs-lookup"><span data-stu-id="caeb2-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="caeb2-137">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="caeb2-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="caeb2-138">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="caeb2-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-139">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="caeb2-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-141">啟動動作的延遲。</span><span class="sxs-lookup"><span data-stu-id="caeb2-141">The delay for the startup action.</span></span> <span data-ttu-id="caeb2-142">這個值是 **datetime** 資料類型的間隔變異。</span><span class="sxs-lookup"><span data-stu-id="caeb2-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-143">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="caeb2-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="caeb2-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-146">啟動主機系統時，虛擬系統啟用的序號。</span><span class="sxs-lookup"><span data-stu-id="caeb2-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="caeb2-147">較低的數位表示先前的啟用。</span><span class="sxs-lookup"><span data-stu-id="caeb2-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="caeb2-148">如果有一或多個設定顯示相同的值，則序列會相依。</span><span class="sxs-lookup"><span data-stu-id="caeb2-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="caeb2-149">值為 "0" 表示序列與實值相依。</span><span class="sxs-lookup"><span data-stu-id="caeb2-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-150">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="caeb2-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-153">儲存虛擬系統組態相關資訊之目錄的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="caeb2-154">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-155">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="caeb2-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-158">儲存虛擬系統組態相關資訊之檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="caeb2-159">相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="caeb2-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="caeb2-160">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="caeb2-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-164">虛擬系統組態的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="caeb2-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="caeb2-165">**ConfigurationID** 與 **InstanceID** 不同，它是由實作為虛擬系統或虛擬系統組態的實作為指派。</span><span class="sxs-lookup"><span data-stu-id="caeb2-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="caeb2-166">**ConfigurationID** 不是索引鍵，而且一個以上的實例可能會發生相同的值。</span><span class="sxs-lookup"><span data-stu-id="caeb2-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="caeb2-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="caeb2-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-168">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="caeb2-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-170">建立虛擬系統組態的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="caeb2-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-171">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="caeb2-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-174">儲存虛擬系統記錄檔資訊之目錄的相對檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="caeb2-175">相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="caeb2-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="caeb2-176">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-177">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="caeb2-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-178">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="caeb2-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-180">陣列，其中包含與虛擬系統相關的使用者提供的附注。</span><span class="sxs-lookup"><span data-stu-id="caeb2-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-181">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="caeb2-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-184">儲存虛擬系統復原相關資訊之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="caeb2-185">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-186">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="caeb2-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-189">儲存虛擬系統快照相關資訊之目錄的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="caeb2-190">相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="caeb2-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="caeb2-191">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-192">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="caeb2-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-195">儲存虛擬系統暫停相關資訊之目錄的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="caeb2-196">相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="caeb2-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="caeb2-197">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-198">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="caeb2-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-201">儲存虛擬系統之交換檔的目錄相對檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="caeb2-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="caeb2-202">相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="caeb2-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="caeb2-203">這個屬性的格式是以 RFC 2079 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="caeb2-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-204">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="caeb2-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-207">虛擬化平臺內系統的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="caeb2-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="caeb2-208">**VirtualSystemIdentifier** 不是指派給虛擬系統內執行之作業系統實例的主機名稱，而是指派給其任何網路埠的 IP 位址或 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="caeb2-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="caeb2-209">**VirtualSystemIdentifier** 可能包含執行特定的規則，例如簡單模式或在設定 **VirtualSystemIdentifier** 時可由執行所解讀的正則運算式。</span><span class="sxs-lookup"><span data-stu-id="caeb2-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="caeb2-210">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="caeb2-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caeb2-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="caeb2-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caeb2-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="caeb2-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="caeb2-213">虛擬系統的類型。</span><span class="sxs-lookup"><span data-stu-id="caeb2-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="caeb2-214">如果虛擬系統類型不明，此值必須設為 "DMTF： unknown"。</span><span class="sxs-lookup"><span data-stu-id="caeb2-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="caeb2-215">這個屬性會使用下列增強型巴克斯格斯格式來格式化 (ABNF) 格式：</span><span class="sxs-lookup"><span data-stu-id="caeb2-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="caeb2-216">vs-type = dmtf-值/其他-組織-值/舊版-值;dmtf-value = "DMTF：" 定義-org "：" org-vs type;其他-org-value = 定義-org "：" org-vs type;</span><span class="sxs-lookup"><span data-stu-id="caeb2-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="caeb2-217">上述 ABNF 格式的值為：</span><span class="sxs-lookup"><span data-stu-id="caeb2-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="caeb2-218">*dmtf-值*   ：由 dmtf 定義的屬性值，定義于這個屬性的描述中。</span><span class="sxs-lookup"><span data-stu-id="caeb2-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="caeb2-219">*其他-組織-值*   是由 DMTF 以外的商務實體所定義的屬性值，不會在這個屬性的描述中定義。</span><span class="sxs-lookup"><span data-stu-id="caeb2-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="caeb2-220">*舊版-值*   是由 DMTF 以外的商務實體所定義的屬性值，而且不會定義在這個屬性的描述中。</span><span class="sxs-lookup"><span data-stu-id="caeb2-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="caeb2-221">允許這些值，但建議在一段時間後淘汰。</span><span class="sxs-lookup"><span data-stu-id="caeb2-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="caeb2-222">*定義-org*   ：定義虛擬系統類型之商務實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="caeb2-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="caeb2-223">它應該包含受著作權、商標或商務實體所擁有的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="caeb2-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="caeb2-224">它不應該是 "DMTF"，且不能包含冒號。</span><span class="sxs-lookup"><span data-stu-id="caeb2-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="caeb2-225">*組織-vs-*   在定義商務實體內輸入虛擬系統類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="caeb2-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="caeb2-226">它在定義-組織內應該是唯一的。組織型別可以使用 CIM 字串允許的任何字元，但下列除外： U0000-U001F (Unicode C0 控制項) 、U0020 (空間) 、U007F (Unicode C0 控制項) 或 U0080-U009F (Unicode C1 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="caeb2-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="caeb2-227">如果需要將值結構組成區段，則應該以單一冒號分隔區段。</span><span class="sxs-lookup"><span data-stu-id="caeb2-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="caeb2-228">這個屬性的值應該處理案例區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="caeb2-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="caeb2-229">它們的目的是要以程式設計的方式處理，而不是顯示名稱，而且應該簡短。</span><span class="sxs-lookup"><span data-stu-id="caeb2-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="caeb2-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="caeb2-230">Requirements</span></span>



| <span data-ttu-id="caeb2-231">需求</span><span class="sxs-lookup"><span data-stu-id="caeb2-231">Requirement</span></span> | <span data-ttu-id="caeb2-232">值</span><span class="sxs-lookup"><span data-stu-id="caeb2-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caeb2-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caeb2-233">Minimum supported client</span></span><br/> | <span data-ttu-id="caeb2-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="caeb2-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="caeb2-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caeb2-235">Minimum supported server</span></span><br/> | <span data-ttu-id="caeb2-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="caeb2-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="caeb2-237">命名空間</span><span class="sxs-lookup"><span data-stu-id="caeb2-237">Namespace</span></span><br/>                | <span data-ttu-id="caeb2-238">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="caeb2-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="caeb2-239">MOF</span><span class="sxs-lookup"><span data-stu-id="caeb2-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caeb2-240"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="caeb2-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="caeb2-241">DLL</span><span class="sxs-lookup"><span data-stu-id="caeb2-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caeb2-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="caeb2-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="caeb2-243">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caeb2-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caeb2-244">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="caeb2-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




