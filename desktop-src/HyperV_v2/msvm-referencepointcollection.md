---
description: 表示虛擬系統參考點的集合。
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Msvm_ReferencePointCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849494"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="a2c91-103">Msvm \_ ReferencePointCollection 類別</span><span class="sxs-lookup"><span data-stu-id="a2c91-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="a2c91-104">表示虛擬系統參考點的集合。</span><span class="sxs-lookup"><span data-stu-id="a2c91-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="a2c91-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c91-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c91-106">語法</span><span class="sxs-lookup"><span data-stu-id="a2c91-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="a2c91-107">成員</span><span class="sxs-lookup"><span data-stu-id="a2c91-107">Members</span></span>

<span data-ttu-id="a2c91-108">**Msvm \_ ReferencePointCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a2c91-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="a2c91-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a2c91-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2c91-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a2c91-110">Properties</span></span>

<span data-ttu-id="a2c91-111">**Msvm \_ ReferencePointCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c91-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2c91-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="a2c91-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c91-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2c91-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2c91-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CollectionID" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a2c91-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a2c91-116">集合物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2c91-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="a2c91-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="a2c91-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c91-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a2c91-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2c91-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a2c91-120">參考點的一致性層級。</span><span class="sxs-lookup"><span data-stu-id="a2c91-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2c91-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a2c91-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="a2c91-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>損 **毀一致** (1) </span><span class="sxs-lookup"><span data-stu-id="a2c91-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a2c91-123">參考點表示虛擬系統處於損毀一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="a2c91-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="a2c91-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**應用程式一致** (2) </span><span class="sxs-lookup"><span data-stu-id="a2c91-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a2c91-125">參考點表示虛擬系統處於應用程式一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="a2c91-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a2c91-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a2c91-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c91-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2c91-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2c91-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-129">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="a2c91-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="a2c91-130">集合的使用者定義名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c91-130">An user-defined name for the collection.</span></span> <span data-ttu-id="a2c91-131">請注意，這不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a2c91-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="a2c91-132">**HasAssociatedLog**</span><span class="sxs-lookup"><span data-stu-id="a2c91-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c91-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a2c91-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2c91-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a2c91-135">如果所有成員參考點都有相關聯的記錄，**則為 true** 。</span><span class="sxs-lookup"><span data-stu-id="a2c91-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="a2c91-136">這僅適用于以記錄為基礎的參考點。</span><span class="sxs-lookup"><span data-stu-id="a2c91-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="a2c91-137">若為 .RCT 型參考點， **HasAssociatedLog** 會設為 **false**。</span><span class="sxs-lookup"><span data-stu-id="a2c91-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="a2c91-138">針對以記錄為基礎的參考點，一旦捨棄記錄檔， **HasAssociatedLog** 就會變成 **false**。</span><span class="sxs-lookup"><span data-stu-id="a2c91-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c91-139">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="a2c91-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c91-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a2c91-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2c91-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-142">限定詞： [ **In**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2c91-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2c91-143">指出參考點的型別。</span><span class="sxs-lookup"><span data-stu-id="a2c91-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2c91-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a2c91-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="a2c91-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>以 **記錄為基礎** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="a2c91-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a2c91-146">Hyper-v 複本記錄追蹤。</span><span class="sxs-lookup"><span data-stu-id="a2c91-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="a2c91-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**依** (2) 的 .rct</span><span class="sxs-lookup"><span data-stu-id="a2c91-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a2c91-148">以虛擬磁片的復原變更追蹤為基礎。</span><span class="sxs-lookup"><span data-stu-id="a2c91-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a2c91-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a2c91-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="a2c91-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a2c91-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2c91-151">**VirtualSystemCollectionId**</span><span class="sxs-lookup"><span data-stu-id="a2c91-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c91-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2c91-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2c91-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c91-154">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)。**CollectionID**") </span><span class="sxs-lookup"><span data-stu-id="a2c91-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="a2c91-155">這個參考點所屬的 [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2c91-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2c91-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2c91-156">Requirements</span></span>



| <span data-ttu-id="a2c91-157">需求</span><span class="sxs-lookup"><span data-stu-id="a2c91-157">Requirement</span></span> | <span data-ttu-id="a2c91-158">值</span><span class="sxs-lookup"><span data-stu-id="a2c91-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c91-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2c91-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c91-160">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2c91-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a2c91-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2c91-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c91-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a2c91-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a2c91-163">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2c91-163">Namespace</span></span><br/>                | <span data-ttu-id="a2c91-164">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2c91-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2c91-165">MOF</span><span class="sxs-lookup"><span data-stu-id="a2c91-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2c91-166"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a2c91-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2c91-167">DLL</span><span class="sxs-lookup"><span data-stu-id="a2c91-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2c91-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2c91-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2c91-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2c91-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c91-170">**CIM \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="a2c91-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

