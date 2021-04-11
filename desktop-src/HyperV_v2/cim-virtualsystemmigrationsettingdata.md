---
description: 定義由 CIM VirtualSystemMigrationService 類別的實例所管理之虛擬系統移轉的設定 \_ 。
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692823"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="1d01f-103">CIM \_ VirtualSystemMigrationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="1d01f-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="1d01f-104">定義由 [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) 類別的實例所管理之虛擬系統移轉的設定。</span><span class="sxs-lookup"><span data-stu-id="1d01f-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d01f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d01f-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="1d01f-106">成員</span><span class="sxs-lookup"><span data-stu-id="1d01f-106">Members</span></span>

<span data-ttu-id="1d01f-107">**CIM \_ VirtualSystemMigrationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1d01f-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1d01f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1d01f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d01f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1d01f-109">Properties</span></span>

<span data-ttu-id="1d01f-110">**CIM \_ VirtualSystemMigrationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1d01f-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d01f-111">**頻寬**</span><span class="sxs-lookup"><span data-stu-id="1d01f-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d01f-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1d01f-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d01f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-114">限定詞：量測 [**計、**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ VirtualSystemMigrationSettingData**。**BandwidthUnit**") </span><span class="sxs-lookup"><span data-stu-id="1d01f-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="1d01f-115">指派給或要求進行虛擬系統移轉操作的頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="1d01f-116">"0" 是遷移要求的預設頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="1d01f-117">**頻寬** 和 **優先順序** 屬性可以搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1d01f-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="1d01f-118">具有最高相等 **優先權** 值的遷移程式會根據其要求的頻寬共用可用的頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="1d01f-119">如果並非所有的頻寬都是由這組進程取用，則具有下一個較低 **優先順序** 值的遷移程式會共用剩餘的頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="1d01f-120">如果保留更多頻寬，則會考慮具有下一個較低 **優先順序** 值的遷移程式。</span><span class="sxs-lookup"><span data-stu-id="1d01f-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="1d01f-121">[ **頻寬** ] 屬性中所使用的單位是由 [ **BandwidthUnit** ] 屬性的值所指定。</span><span class="sxs-lookup"><span data-stu-id="1d01f-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="1d01f-122">如果 **BandwidthUnit** 屬性的值為 "percent"，則適用下列規則：</span><span class="sxs-lookup"><span data-stu-id="1d01f-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="1d01f-123">**頻寬** 屬性的值必須介於 "0" 和 "100" 之間，且值越高，表示較高的頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="1d01f-124">值為 "100" 表示執行虛擬系統移轉作業的所有可用頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="1d01f-125">"1" 和 "100" 之間的值會以線性方式與可用的頻寬範圍產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1d01f-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="1d01f-126">例如，值為50時，會要求一半的可用頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="1d01f-127">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="1d01f-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d01f-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d01f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d01f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-130">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VirtualSystemMigrationSettingData**.**頻寬**」 ) 、 **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="1d01f-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="1d01f-131">**頻寬** 屬性所使用的單位。</span><span class="sxs-lookup"><span data-stu-id="1d01f-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="1d01f-132">這個屬性的值應該是 DSP0004 2.4 或更新版本的附錄 C 中所定義之程式設計單位辨識符號的合法值。</span><span class="sxs-lookup"><span data-stu-id="1d01f-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="1d01f-133">諸如 DMTF DSP1081 等設定檔會定義用戶端如何探索執行所支援的單位集合，以及 **頻寬** 屬性值的範圍和增量。</span><span class="sxs-lookup"><span data-stu-id="1d01f-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="1d01f-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="1d01f-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d01f-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1d01f-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d01f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d01f-137">要執行的遷移作業類型。</span><span class="sxs-lookup"><span data-stu-id="1d01f-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d01f-138">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1d01f-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d01f-139">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1d01f-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="1d01f-140">**Live** (2) </span><span class="sxs-lookup"><span data-stu-id="1d01f-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="1d01f-141">**繼續** (3) </span><span class="sxs-lookup"><span data-stu-id="1d01f-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="1d01f-142">**重新開機** (4) </span><span class="sxs-lookup"><span data-stu-id="1d01f-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d01f-143">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="1d01f-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d01f-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d01f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d01f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-146">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**") </span><span class="sxs-lookup"><span data-stu-id="1d01f-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="1d01f-147">如果 **TransportType** 的值為 "1" (其他) ，則為要套用的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="1d01f-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="1d01f-148">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="1d01f-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d01f-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1d01f-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d01f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d01f-151">虛擬系統移轉程式可能用來在多個暫止的遷移要求之間訂購或指派喜好設定的相對遷移重要性。</span><span class="sxs-lookup"><span data-stu-id="1d01f-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="1d01f-152">值愈低，優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="1d01f-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="1d01f-153">"0" 是遷移要求的預設頻寬。</span><span class="sxs-lookup"><span data-stu-id="1d01f-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="1d01f-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="1d01f-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d01f-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1d01f-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d01f-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d01f-157">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**") </span><span class="sxs-lookup"><span data-stu-id="1d01f-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="1d01f-158">要套用至虛擬系統移轉作業的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="1d01f-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d01f-159">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1d01f-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d01f-160">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1d01f-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="1d01f-161">**SSH** (2) </span><span class="sxs-lookup"><span data-stu-id="1d01f-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="1d01f-162">**TLS** (3) </span><span class="sxs-lookup"><span data-stu-id="1d01f-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="1d01f-163">**TLS Strict** (4) </span><span class="sxs-lookup"><span data-stu-id="1d01f-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="1d01f-164">**TCP** (5) </span><span class="sxs-lookup"><span data-stu-id="1d01f-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="1d01f-165">**IPC** (6) </span><span class="sxs-lookup"><span data-stu-id="1d01f-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1d01f-166">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1d01f-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1d01f-167">**廠商保留** (32768 ) </span><span class="sxs-lookup"><span data-stu-id="1d01f-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="1d01f-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1d01f-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1d01f-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d01f-169">Requirements</span></span>



| <span data-ttu-id="1d01f-170">需求</span><span class="sxs-lookup"><span data-stu-id="1d01f-170">Requirement</span></span> | <span data-ttu-id="1d01f-171">值</span><span class="sxs-lookup"><span data-stu-id="1d01f-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d01f-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d01f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="1d01f-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1d01f-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1d01f-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d01f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="1d01f-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d01f-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1d01f-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d01f-176">Namespace</span></span><br/>                | <span data-ttu-id="1d01f-177">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1d01f-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1d01f-178">MOF</span><span class="sxs-lookup"><span data-stu-id="1d01f-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d01f-179"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1d01f-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d01f-180">DLL</span><span class="sxs-lookup"><span data-stu-id="1d01f-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d01f-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d01f-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d01f-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d01f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d01f-183">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="1d01f-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

