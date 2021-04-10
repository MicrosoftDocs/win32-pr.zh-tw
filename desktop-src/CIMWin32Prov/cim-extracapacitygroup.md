---
description: CIM \_ ExtraCapacityGroup 類別衍生自冗余群組，指出匯總專案的容量或功能比所需的還多。
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: CIM_ExtraCapacityGroup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187761"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="90c5c-103">CIM \_ ExtraCapacityGroup 類別</span><span class="sxs-lookup"><span data-stu-id="90c5c-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="90c5c-104">**CIM \_ ExtraCapacityGroup** 類別衍生自冗余群組，指出匯總專案的容量或功能比所需的還多。</span><span class="sxs-lookup"><span data-stu-id="90c5c-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="90c5c-105">這類冗余的範例是在系統中安裝 N + 1 電源供應器或風扇。</span><span class="sxs-lookup"><span data-stu-id="90c5c-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90c5c-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="90c5c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="90c5c-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="90c5c-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="90c5c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="90c5c-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="90c5c-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c5c-110">語法</span><span class="sxs-lookup"><span data-stu-id="90c5c-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="90c5c-111">成員</span><span class="sxs-lookup"><span data-stu-id="90c5c-111">Members</span></span>

<span data-ttu-id="90c5c-112">**CIM \_ ExtraCapacityGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="90c5c-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="90c5c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="90c5c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90c5c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="90c5c-114">Properties</span></span>

<span data-ttu-id="90c5c-115">**CIM \_ ExtraCapacityGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="90c5c-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90c5c-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="90c5c-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="90c5c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-120">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="90c5c-120">A short textual description of the object.</span></span>

<span data-ttu-id="90c5c-121">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90c5c-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="90c5c-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="90c5c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="90c5c-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-126">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="90c5c-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="90c5c-127">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="90c5c-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="90c5c-128">這個屬性繼承自 [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="90c5c-129">**說明**</span><span class="sxs-lookup"><span data-stu-id="90c5c-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="90c5c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-132">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-133">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="90c5c-133">A textual description of the object.</span></span>

<span data-ttu-id="90c5c-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90c5c-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="90c5c-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-136">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="90c5c-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="90c5c-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-139">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="90c5c-139">Indicates when the object was installed.</span></span> <span data-ttu-id="90c5c-140">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="90c5c-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="90c5c-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90c5c-142">**MinNumberNeeded**</span><span class="sxs-lookup"><span data-stu-id="90c5c-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="90c5c-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-145">必須可運作以具有重複專案的最小元素數目。</span><span class="sxs-lookup"><span data-stu-id="90c5c-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="90c5c-146">例如，在 N + 1 個冗余關聯性中，這個屬性應該設定為等於 N。</span><span class="sxs-lookup"><span data-stu-id="90c5c-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="90c5c-147">**名稱**</span><span class="sxs-lookup"><span data-stu-id="90c5c-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="90c5c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-150">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-151">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="90c5c-151">Label by which the object is known.</span></span> <span data-ttu-id="90c5c-152">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="90c5c-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="90c5c-153">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90c5c-154">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="90c5c-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="90c5c-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-157">有關冗余群組狀態的資訊。</span><span class="sxs-lookup"><span data-stu-id="90c5c-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="90c5c-158">這個屬性繼承自 [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90c5c-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="90c5c-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="90c5c-160">不明。</span><span class="sxs-lookup"><span data-stu-id="90c5c-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="90c5c-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="90c5c-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="90c5c-162">其他。</span><span class="sxs-lookup"><span data-stu-id="90c5c-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="90c5c-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**完全多餘** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="90c5c-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="90c5c-164">所有設定的冗余都可供使用。</span><span class="sxs-lookup"><span data-stu-id="90c5c-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="90c5c-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**降級的冗余** (3) </span><span class="sxs-lookup"><span data-stu-id="90c5c-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="90c5c-166">因為某些失敗，所以可使用較少的可用冗余量。</span><span class="sxs-lookup"><span data-stu-id="90c5c-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="90c5c-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**遺失** (4) 的冗余</span><span class="sxs-lookup"><span data-stu-id="90c5c-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="90c5c-168">因為有足夠的失敗次數，所以無法使用冗余。</span><span class="sxs-lookup"><span data-stu-id="90c5c-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="90c5c-169">下一個失敗會導致整體失敗。</span><span class="sxs-lookup"><span data-stu-id="90c5c-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90c5c-170">**狀態**</span><span class="sxs-lookup"><span data-stu-id="90c5c-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c5c-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="90c5c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90c5c-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c5c-173">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="90c5c-174">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="90c5c-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="90c5c-175">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="90c5c-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="90c5c-176">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="90c5c-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="90c5c-177">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="90c5c-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="90c5c-178">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="90c5c-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="90c5c-179">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="90c5c-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="90c5c-180">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="90c5c-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="90c5c-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="90c5c-182">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="90c5c-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="90c5c-183">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="90c5c-184">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="90c5c-185">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90c5c-186">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="90c5c-187">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="90c5c-188">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="90c5c-189">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="90c5c-190">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="90c5c-191">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="90c5c-192">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="90c5c-193">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="90c5c-194">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="90c5c-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="90c5c-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="90c5c-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="90c5c-196">備註</span><span class="sxs-lookup"><span data-stu-id="90c5c-196">Remarks</span></span>

<span data-ttu-id="90c5c-197">**Cim \_ ExtraCapacityGroup** 類別衍生自 [**cim \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="90c5c-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="90c5c-198">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="90c5c-198">WMI does not implement this class.</span></span>

<span data-ttu-id="90c5c-199">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="90c5c-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="90c5c-200">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="90c5c-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c5c-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="90c5c-201">Requirements</span></span>



| <span data-ttu-id="90c5c-202">需求</span><span class="sxs-lookup"><span data-stu-id="90c5c-202">Requirement</span></span> | <span data-ttu-id="90c5c-203">值</span><span class="sxs-lookup"><span data-stu-id="90c5c-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c5c-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90c5c-204">Minimum supported client</span></span><br/> | <span data-ttu-id="90c5c-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90c5c-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90c5c-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90c5c-206">Minimum supported server</span></span><br/> | <span data-ttu-id="90c5c-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90c5c-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90c5c-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="90c5c-208">Namespace</span></span><br/>                | <span data-ttu-id="90c5c-209">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="90c5c-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90c5c-210">MOF</span><span class="sxs-lookup"><span data-stu-id="90c5c-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90c5c-211"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="90c5c-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90c5c-212">DLL</span><span class="sxs-lookup"><span data-stu-id="90c5c-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c5c-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90c5c-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c5c-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90c5c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c5c-215">**CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="90c5c-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

