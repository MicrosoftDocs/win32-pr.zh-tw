---
description: CIM \_ StorageRedundancyGroup 類別代表大量儲存體相關的重複資訊。
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: CIM_StorageRedundancyGroup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972326"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="3d1e0-103">CIM \_ StorageRedundancyGroup 類別</span><span class="sxs-lookup"><span data-stu-id="3d1e0-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="3d1e0-104">**CIM \_ StorageRedundancyGroup** 類別代表大量儲存體相關的重複資訊。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="3d1e0-105">儲存體冗余群組是用來保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="3d1e0-106">它們是由一或多個實體範圍，或一或多個匯總實體範圍所組成。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="3d1e0-107">儲存體冗余群組可能會重迭;但是，重迭內的基礎範圍不應該包含任何檢查資料。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d1e0-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d1e0-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d1e0-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3d1e0-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1e0-112">語法</span><span class="sxs-lookup"><span data-stu-id="3d1e0-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="3d1e0-113">成員</span><span class="sxs-lookup"><span data-stu-id="3d1e0-113">Members</span></span>

<span data-ttu-id="3d1e0-114">**CIM \_ StorageRedundancyGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3d1e0-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="3d1e0-115">屬性</span><span class="sxs-lookup"><span data-stu-id="3d1e0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d1e0-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3d1e0-116">Properties</span></span>

<span data-ttu-id="3d1e0-117">**CIM \_ StorageRedundancyGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d1e0-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-122">A short textual description of the object.</span></span>

<span data-ttu-id="3d1e0-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1e0-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-127">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-128">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3d1e0-129">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3d1e0-130">這個屬性繼承自 [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1e0-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-134">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-135">A textual description of the object.</span></span>

<span data-ttu-id="3d1e0-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1e0-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="3d1e0-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-141">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-141">Indicates when the object was installed.</span></span> <span data-ttu-id="3d1e0-142">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3d1e0-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1e0-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-147">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-148">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-148">Label by which the object is known.</span></span> <span data-ttu-id="3d1e0-149">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3d1e0-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1e0-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-152">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-154">有關冗余群組狀態的資訊。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="3d1e0-155">這個屬性繼承自 [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d1e0-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3d1e0-157">不明。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d1e0-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3d1e0-159">其他。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="3d1e0-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**完全多餘** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3d1e0-161">所有設定的冗余都可供使用。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="3d1e0-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**降級的冗余** (3) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3d1e0-163">因為某些失敗，所以可使用較少的可用冗余量。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="3d1e0-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**遺失** (4) 的冗余</span><span class="sxs-lookup"><span data-stu-id="3d1e0-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3d1e0-165">因為有足夠的失敗次數，所以無法使用冗余。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="3d1e0-166">下一個失敗會導致整體失敗。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d1e0-167">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-170">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-171">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="3d1e0-172">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3d1e0-173">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3d1e0-174">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3d1e0-175">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3d1e0-176">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3d1e0-177">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3d1e0-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3d1e0-179">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="3d1e0-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3d1e0-180">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3d1e0-181">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3d1e0-182">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d1e0-183">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3d1e0-184">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3d1e0-185">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3d1e0-186">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3d1e0-187">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3d1e0-188">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3d1e0-189">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3d1e0-190">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3d1e0-191">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d1e0-192">**TypeOfAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1e0-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d1e0-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1e0-195">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 冗余群組 \| 001.2」 ) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="3d1e0-196">用於資料冗余和重建的演算法。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="3d1e0-197">在 CIM 架構中，值0是不正確，因為它代表 DMI 中沒有任何冗余存在。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="3d1e0-198">在這種情況下，不應該具現化物件。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3d1e0-199">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="3d1e0-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d1e0-200">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d1e0-201">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="3d1e0-202">**複製** (3) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="3d1e0-203">**XOR** (4) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="3d1e0-204">**P + Q** (5) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="3d1e0-205">**S** (6) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="3d1e0-206">**P + S** (7) </span><span class="sxs-lookup"><span data-stu-id="3d1e0-206">**P+S** (7)</span></span>


<span data-ttu-id="3d1e0-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3d1e0-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3d1e0-208">備註</span><span class="sxs-lookup"><span data-stu-id="3d1e0-208">Remarks</span></span>

<span data-ttu-id="3d1e0-209">**Cim \_ StorageRedundancyGroup** 類別衍生自 [**cim \_ RedundancyGroup**](cim-redundancygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="3d1e0-210">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-210">WMI does not implement this class.</span></span>

<span data-ttu-id="3d1e0-211">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d1e0-212">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3d1e0-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1e0-213">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d1e0-213">Requirements</span></span>



| <span data-ttu-id="3d1e0-214">需求</span><span class="sxs-lookup"><span data-stu-id="3d1e0-214">Requirement</span></span> | <span data-ttu-id="3d1e0-215">值</span><span class="sxs-lookup"><span data-stu-id="3d1e0-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1e0-216">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d1e0-216">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1e0-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d1e0-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d1e0-218">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d1e0-218">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1e0-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d1e0-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d1e0-220">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d1e0-220">Namespace</span></span><br/>                | <span data-ttu-id="3d1e0-221">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d1e0-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d1e0-222">MOF</span><span class="sxs-lookup"><span data-stu-id="3d1e0-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d1e0-223"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d1e0-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d1e0-224">DLL</span><span class="sxs-lookup"><span data-stu-id="3d1e0-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d1e0-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d1e0-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1e0-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d1e0-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1e0-227">**CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="3d1e0-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

