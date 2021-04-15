---
description: 代表虛擬光纖通道交換器的設定。
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Msvm_VirtualFcSwitchSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511001"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="72f27-103">Msvm \_ VirtualFcSwitchSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="72f27-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="72f27-104">代表虛擬光纖通道交換器的設定。</span><span class="sxs-lookup"><span data-stu-id="72f27-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="72f27-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="72f27-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f27-106">語法</span><span class="sxs-lookup"><span data-stu-id="72f27-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
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

## <a name="members"></a><span data-ttu-id="72f27-107">成員</span><span class="sxs-lookup"><span data-stu-id="72f27-107">Members</span></span>

<span data-ttu-id="72f27-108">**Msvm \_ VirtualFcSwitchSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="72f27-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="72f27-109">屬性</span><span class="sxs-lookup"><span data-stu-id="72f27-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72f27-110">屬性</span><span class="sxs-lookup"><span data-stu-id="72f27-110">Properties</span></span>

<span data-ttu-id="72f27-111">**Msvm \_ VirtualFcSwitchSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="72f27-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72f27-112">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="72f27-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="72f27-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-115">當虛擬機器執行的軟體失敗時，針對虛擬機器所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="72f27-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="72f27-116">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-117">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="72f27-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="72f27-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-120">當主機關閉時，為虛擬機器採取的動作。</span><span class="sxs-lookup"><span data-stu-id="72f27-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="72f27-121">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-122">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="72f27-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="72f27-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-125">當主機啟動時，對虛擬機器採取的動作。</span><span class="sxs-lookup"><span data-stu-id="72f27-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="72f27-126">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-127">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="72f27-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="72f27-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-130">虛擬機器自動啟動之前的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="72f27-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="72f27-131">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-132">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="72f27-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="72f27-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-135">數位，指出主機系統啟動時的虛擬機器啟用的相對順序。</span><span class="sxs-lookup"><span data-stu-id="72f27-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="72f27-136">較低的數位表示先前的啟用。</span><span class="sxs-lookup"><span data-stu-id="72f27-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="72f27-137">如果有一或多個設定顯示相同的值，則序列會相依。</span><span class="sxs-lookup"><span data-stu-id="72f27-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="72f27-138">值為0時，表示序列與實值相依。</span><span class="sxs-lookup"><span data-stu-id="72f27-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="72f27-139">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-140">**標題**</span><span class="sxs-lookup"><span data-stu-id="72f27-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-143">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="72f27-143">A short description of the object.</span></span> <span data-ttu-id="72f27-144">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="72f27-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-145">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="72f27-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-148">儲存虛擬機器設定相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="72f27-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="72f27-149">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-150">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="72f27-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-153">儲存虛擬機器設定相關資訊之檔案的相對路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="72f27-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="72f27-154">此路徑相對於 **ConfigurationDataRoot** 屬性。</span><span class="sxs-lookup"><span data-stu-id="72f27-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="72f27-155">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="72f27-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-159">設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="72f27-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="72f27-160">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="72f27-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-162">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="72f27-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-164">建立設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="72f27-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="72f27-165">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="72f27-166">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-167">**說明**</span><span class="sxs-lookup"><span data-stu-id="72f27-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-170">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="72f27-170">A description of the object.</span></span> <span data-ttu-id="72f27-171">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="72f27-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="72f27-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-175">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="72f27-175">A display name for the object.</span></span> <span data-ttu-id="72f27-176">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="72f27-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72f27-180">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="72f27-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="72f27-181">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="72f27-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="72f27-182">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-183">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="72f27-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-186">儲存虛擬機器記錄資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="72f27-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="72f27-187">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-188">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="72f27-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-189">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="72f27-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72f27-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-191">與虛擬機器相關的使用者提供的附注。</span><span class="sxs-lookup"><span data-stu-id="72f27-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="72f27-192">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-193">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="72f27-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-196">儲存虛擬機器修復相關資訊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="72f27-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="72f27-197">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-198">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="72f27-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-201">儲存虛擬機器快照集相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="72f27-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="72f27-202">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-203">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="72f27-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-206">儲存虛擬機器暫停相關資訊之相關資訊的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="72f27-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="72f27-207">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-208">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="72f27-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-211">儲存虛擬機器之交換檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="72f27-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="72f27-212">這個屬性會繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="72f27-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72f27-213">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="72f27-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-216">這項設定資料所屬之 CIM 非程式物件的名稱。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem)</span><span class="sxs-lookup"><span data-stu-id="72f27-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="72f27-217">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72f27-218">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="72f27-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72f27-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72f27-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72f27-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72f27-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72f27-221">指定設定資料所代表的虛擬機器類型。</span><span class="sxs-lookup"><span data-stu-id="72f27-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="72f27-222">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="72f27-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72f27-223">規格需求</span><span class="sxs-lookup"><span data-stu-id="72f27-223">Requirements</span></span>



| <span data-ttu-id="72f27-224">需求</span><span class="sxs-lookup"><span data-stu-id="72f27-224">Requirement</span></span> | <span data-ttu-id="72f27-225">值</span><span class="sxs-lookup"><span data-stu-id="72f27-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f27-226">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72f27-226">Minimum supported client</span></span><br/> | <span data-ttu-id="72f27-227">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72f27-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72f27-228">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72f27-228">Minimum supported server</span></span><br/> | <span data-ttu-id="72f27-229">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72f27-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72f27-230">命名空間</span><span class="sxs-lookup"><span data-stu-id="72f27-230">Namespace</span></span><br/>                | <span data-ttu-id="72f27-231">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="72f27-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72f27-232">MOF</span><span class="sxs-lookup"><span data-stu-id="72f27-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72f27-233"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="72f27-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72f27-234">DLL</span><span class="sxs-lookup"><span data-stu-id="72f27-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f27-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72f27-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

