---
description: CIM \_ SpareGroup 類別衍生自 cim \_ RedundancyGroup 類別，並指出一或多個匯總的元素可以被用。
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: CIM_SpareGroup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688592"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="72033-103">CIM \_ SpareGroup 類別</span><span class="sxs-lookup"><span data-stu-id="72033-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="72033-104">**Cim \_ SpareGroup** 類別衍生自 [**cim \_ RedundancyGroup**](cim-redundancygroup.md)類別，並指出一或多個匯總的元素可以被用。</span><span class="sxs-lookup"><span data-stu-id="72033-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="72033-105">您可以使用 [**CIM \_ ActsAsSpare**](cim-actsasspare.md) 關聯來定義備用。</span><span class="sxs-lookup"><span data-stu-id="72033-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="72033-106">備用的 Nic 範例是在電腦系統中使用多餘的 Nic，其中一個 NIC 是主要的，另一個則是備用。</span><span class="sxs-lookup"><span data-stu-id="72033-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="72033-107">主要 NIC 會是備用群組的成員，並使用 [**cim \_ RedundancyComponent**](cim-redundancycomponent.md) 類別建立關聯，而其他 nic 則會使用 **cim \_ ActsAsSpare** 關聯性建立關聯。</span><span class="sxs-lookup"><span data-stu-id="72033-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72033-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="72033-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="72033-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="72033-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="72033-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="72033-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="72033-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="72033-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72033-112">語法</span><span class="sxs-lookup"><span data-stu-id="72033-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="72033-113">成員</span><span class="sxs-lookup"><span data-stu-id="72033-113">Members</span></span>

<span data-ttu-id="72033-114">**CIM \_ SpareGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="72033-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="72033-115">屬性</span><span class="sxs-lookup"><span data-stu-id="72033-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72033-116">屬性</span><span class="sxs-lookup"><span data-stu-id="72033-116">Properties</span></span>

<span data-ttu-id="72033-117">**CIM \_ SpareGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="72033-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72033-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="72033-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72033-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72033-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72033-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="72033-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="72033-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="72033-122">A short textual description of the object.</span></span>

<span data-ttu-id="72033-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72033-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="72033-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72033-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72033-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72033-127">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="72033-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="72033-128">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="72033-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="72033-129">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="72033-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="72033-130">這個屬性繼承自 [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="72033-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="72033-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72033-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72033-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72033-134">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="72033-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="72033-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="72033-135">A textual description of the object.</span></span>

<span data-ttu-id="72033-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72033-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="72033-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="72033-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72033-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72033-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="72033-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="72033-141">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="72033-141">Indicates when the object was installed.</span></span> <span data-ttu-id="72033-142">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="72033-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="72033-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72033-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="72033-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72033-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72033-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72033-147">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="72033-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="72033-148">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="72033-148">Label by which the object is known.</span></span> <span data-ttu-id="72033-149">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="72033-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="72033-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72033-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="72033-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-152">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="72033-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72033-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72033-154">有關冗余群組狀態的資訊。</span><span class="sxs-lookup"><span data-stu-id="72033-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="72033-155">這個屬性繼承自 [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72033-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="72033-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="72033-157">不明。</span><span class="sxs-lookup"><span data-stu-id="72033-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="72033-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="72033-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="72033-159">其他。</span><span class="sxs-lookup"><span data-stu-id="72033-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="72033-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**完全多餘** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="72033-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="72033-161">所有設定的冗余都可供使用。</span><span class="sxs-lookup"><span data-stu-id="72033-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="72033-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**降級的冗余** (3) </span><span class="sxs-lookup"><span data-stu-id="72033-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="72033-163">因為某些失敗，所以可使用較少的可用冗余量。</span><span class="sxs-lookup"><span data-stu-id="72033-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="72033-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**遺失** (4) 的冗余</span><span class="sxs-lookup"><span data-stu-id="72033-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="72033-165">因為有足夠的失敗次數，所以無法使用冗余。</span><span class="sxs-lookup"><span data-stu-id="72033-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="72033-166">下一個失敗會導致整體失敗。</span><span class="sxs-lookup"><span data-stu-id="72033-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72033-167">**狀態**</span><span class="sxs-lookup"><span data-stu-id="72033-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72033-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72033-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72033-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72033-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72033-170">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="72033-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="72033-171">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="72033-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="72033-172">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="72033-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="72033-173">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="72033-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="72033-174">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="72033-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="72033-175">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="72033-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="72033-176">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="72033-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="72033-177">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="72033-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="72033-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="72033-179">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="72033-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="72033-180">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="72033-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="72033-181">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="72033-182">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72033-183">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="72033-184">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="72033-185">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="72033-186">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="72033-187">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="72033-188">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="72033-189">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="72033-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="72033-190">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="72033-191">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="72033-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="72033-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="72033-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="72033-193">備註</span><span class="sxs-lookup"><span data-stu-id="72033-193">Remarks</span></span>

<span data-ttu-id="72033-194">**Cim \_ SpareGroup** 類別衍生自 [**cim \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="72033-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="72033-195">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="72033-195">WMI does not implement this class.</span></span>

<span data-ttu-id="72033-196">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="72033-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="72033-197">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="72033-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="72033-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="72033-198">Requirements</span></span>



| <span data-ttu-id="72033-199">需求</span><span class="sxs-lookup"><span data-stu-id="72033-199">Requirement</span></span> | <span data-ttu-id="72033-200">值</span><span class="sxs-lookup"><span data-stu-id="72033-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72033-201">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72033-201">Minimum supported client</span></span><br/> | <span data-ttu-id="72033-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72033-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72033-203">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72033-203">Minimum supported server</span></span><br/> | <span data-ttu-id="72033-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72033-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72033-205">命名空間</span><span class="sxs-lookup"><span data-stu-id="72033-205">Namespace</span></span><br/>                | <span data-ttu-id="72033-206">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="72033-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72033-207">MOF</span><span class="sxs-lookup"><span data-stu-id="72033-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72033-208"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="72033-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72033-209">DLL</span><span class="sxs-lookup"><span data-stu-id="72033-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72033-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72033-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72033-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72033-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72033-212">**CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="72033-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

