---
description: CIM \_ RedundancyGroup 類別代表 managed 系統專案的集合，這些元素表示匯總的元件會一起提供冗余。
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: CIM_RedundancyGroup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847054"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="4dd01-103">CIM \_ RedundancyGroup 類別</span><span class="sxs-lookup"><span data-stu-id="4dd01-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="4dd01-104">**CIM \_ RedundancyGroup** 類別代表 managed 系統專案的集合，這些元素表示匯總的元件會一起提供冗余。</span><span class="sxs-lookup"><span data-stu-id="4dd01-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="4dd01-105">在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。</span><span class="sxs-lookup"><span data-stu-id="4dd01-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dd01-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4dd01-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4dd01-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4dd01-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4dd01-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4dd01-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4dd01-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd01-110">語法</span><span class="sxs-lookup"><span data-stu-id="4dd01-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="4dd01-111">成員</span><span class="sxs-lookup"><span data-stu-id="4dd01-111">Members</span></span>

<span data-ttu-id="4dd01-112">**CIM \_ RedundancyGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4dd01-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="4dd01-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4dd01-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dd01-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4dd01-114">Properties</span></span>

<span data-ttu-id="4dd01-115">**CIM \_ RedundancyGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4dd01-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dd01-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="4dd01-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dd01-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-120">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4dd01-120">A short textual description of the object.</span></span>

<span data-ttu-id="4dd01-121">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dd01-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4dd01-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dd01-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="4dd01-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-126">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dd01-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4dd01-127">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4dd01-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="4dd01-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="4dd01-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dd01-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-131">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-132">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4dd01-132">A textual description of the object.</span></span>

<span data-ttu-id="4dd01-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dd01-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4dd01-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-135">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4dd01-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-137">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4dd01-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-138">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="4dd01-138">Indicates when the object was installed.</span></span> <span data-ttu-id="4dd01-139">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="4dd01-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4dd01-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dd01-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4dd01-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dd01-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-144">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-145">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4dd01-145">Label by which the object is known.</span></span> <span data-ttu-id="4dd01-146">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4dd01-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4dd01-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dd01-148">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="4dd01-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4dd01-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-151">有關冗余群組狀態的資訊。</span><span class="sxs-lookup"><span data-stu-id="4dd01-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4dd01-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4dd01-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4dd01-153">不明。</span><span class="sxs-lookup"><span data-stu-id="4dd01-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4dd01-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4dd01-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4dd01-155">其他。</span><span class="sxs-lookup"><span data-stu-id="4dd01-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="4dd01-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**完全多餘** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4dd01-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4dd01-157">所有設定的冗余都可供使用。</span><span class="sxs-lookup"><span data-stu-id="4dd01-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="4dd01-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**降級的冗余** (3) </span><span class="sxs-lookup"><span data-stu-id="4dd01-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4dd01-159">因為某些失敗，所以可使用較少的可用冗余量。</span><span class="sxs-lookup"><span data-stu-id="4dd01-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="4dd01-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**遺失** (4) 的冗余</span><span class="sxs-lookup"><span data-stu-id="4dd01-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4dd01-161">因為有足夠的失敗次數，所以無法使用冗余。</span><span class="sxs-lookup"><span data-stu-id="4dd01-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="4dd01-162">下一個失敗會導致整體失敗。</span><span class="sxs-lookup"><span data-stu-id="4dd01-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4dd01-163">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4dd01-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dd01-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4dd01-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dd01-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dd01-166">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4dd01-167">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="4dd01-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="4dd01-168">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd01-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4dd01-169">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="4dd01-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4dd01-170">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="4dd01-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4dd01-171">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4dd01-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4dd01-172">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="4dd01-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4dd01-173">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd01-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4dd01-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4dd01-175">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4dd01-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4dd01-176">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4dd01-177">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4dd01-178">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4dd01-179">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4dd01-180">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4dd01-181">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4dd01-182">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4dd01-183">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4dd01-184">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4dd01-185">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4dd01-186">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4dd01-187">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4dd01-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4dd01-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4dd01-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4dd01-189">備註</span><span class="sxs-lookup"><span data-stu-id="4dd01-189">Remarks</span></span>

<span data-ttu-id="4dd01-190">**Cim \_ RedundancyGroup** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd01-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="4dd01-191">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4dd01-191">WMI does not implement this class.</span></span>

<span data-ttu-id="4dd01-192">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4dd01-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4dd01-193">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4dd01-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd01-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dd01-194">Requirements</span></span>



| <span data-ttu-id="4dd01-195">需求</span><span class="sxs-lookup"><span data-stu-id="4dd01-195">Requirement</span></span> | <span data-ttu-id="4dd01-196">值</span><span class="sxs-lookup"><span data-stu-id="4dd01-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd01-197">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dd01-197">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd01-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4dd01-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4dd01-199">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dd01-199">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd01-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4dd01-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4dd01-201">命名空間</span><span class="sxs-lookup"><span data-stu-id="4dd01-201">Namespace</span></span><br/>                | <span data-ttu-id="4dd01-202">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4dd01-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4dd01-203">MOF</span><span class="sxs-lookup"><span data-stu-id="4dd01-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dd01-204"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4dd01-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dd01-205">DLL</span><span class="sxs-lookup"><span data-stu-id="4dd01-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dd01-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dd01-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd01-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dd01-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd01-208">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4dd01-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

