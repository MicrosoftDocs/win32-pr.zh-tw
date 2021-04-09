---
description: CIM \_ JobDestination 類別代表提交工作以進行處理的位置。
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: CIM_JobDestination 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847352"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="d7d77-103">CIM \_ JobDestination 類別</span><span class="sxs-lookup"><span data-stu-id="d7d77-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="d7d77-104">**CIM \_ JobDestination** 類別代表提交工作以進行處理的位置。</span><span class="sxs-lookup"><span data-stu-id="d7d77-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="d7d77-105">它可以參考包含零或多個作業的佇列，例如包含列印工作的列印佇列。</span><span class="sxs-lookup"><span data-stu-id="d7d77-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="d7d77-106">作業目的地裝載于系統上，類似于在系統上託管服務的方式。</span><span class="sxs-lookup"><span data-stu-id="d7d77-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7d77-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d7d77-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d7d77-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d7d77-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7d77-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d7d77-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="d7d77-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d77-111">語法</span><span class="sxs-lookup"><span data-stu-id="d7d77-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="d7d77-112">成員</span><span class="sxs-lookup"><span data-stu-id="d7d77-112">Members</span></span>

<span data-ttu-id="d7d77-113">**CIM \_ JobDestination** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7d77-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="d7d77-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d7d77-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7d77-115">屬性</span><span class="sxs-lookup"><span data-stu-id="d7d77-115">Properties</span></span>

<span data-ttu-id="d7d77-116">**CIM \_ JobDestination** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7d77-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7d77-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="d7d77-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="d7d77-121">A short textual description of the object.</span></span>

<span data-ttu-id="d7d77-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d77-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d7d77-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-126">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d7d77-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-127">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7d77-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d7d77-128">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="d7d77-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="d7d77-129">**說明**</span><span class="sxs-lookup"><span data-stu-id="d7d77-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-132">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-133">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="d7d77-133">A textual description of the object.</span></span>

<span data-ttu-id="d7d77-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d77-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d7d77-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-136">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d7d77-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="d7d77-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-139">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="d7d77-139">Indicates when the object was installed.</span></span> <span data-ttu-id="d7d77-140">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d7d77-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d7d77-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d77-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d7d77-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-145">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-146">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="d7d77-146">Label by which the object is known.</span></span> <span data-ttu-id="d7d77-147">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="d7d77-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d7d77-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d77-149">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d7d77-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-152">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-153">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="d7d77-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="d7d77-154">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="d7d77-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d7d77-155">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="d7d77-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d7d77-156">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="d7d77-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d7d77-157">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d7d77-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d7d77-158">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="d7d77-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d7d77-159">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d7d77-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d7d77-160">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d7d77-161">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="d7d77-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d7d77-162">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d7d77-163">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d7d77-164">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d7d77-165">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d7d77-166">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d7d77-167">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d7d77-168">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d7d77-169">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d7d77-170">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d7d77-171">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d7d77-172">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d7d77-173">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="d7d77-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d7d77-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d7d77-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-177">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="d7d77-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-178">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="d7d77-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d7d77-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d7d77-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7d77-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7d77-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7d77-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7d77-182">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="d7d77-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="d7d77-183">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="d7d77-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7d77-184">備註</span><span class="sxs-lookup"><span data-stu-id="d7d77-184">Remarks</span></span>

<span data-ttu-id="d7d77-185">**Cim \_ JobDestination** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d77-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="d7d77-186">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="d7d77-186">WMI does not implement this class.</span></span>

<span data-ttu-id="d7d77-187">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d7d77-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d7d77-188">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d7d77-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d77-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7d77-189">Requirements</span></span>



| <span data-ttu-id="d7d77-190">需求</span><span class="sxs-lookup"><span data-stu-id="d7d77-190">Requirement</span></span> | <span data-ttu-id="d7d77-191">值</span><span class="sxs-lookup"><span data-stu-id="d7d77-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d77-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7d77-192">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d77-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7d77-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7d77-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7d77-194">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d77-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7d77-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7d77-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7d77-196">Namespace</span></span><br/>                | <span data-ttu-id="d7d77-197">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d7d77-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7d77-198">MOF</span><span class="sxs-lookup"><span data-stu-id="d7d77-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7d77-199"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7d77-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7d77-200">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d77-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7d77-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7d77-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d77-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7d77-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d77-203">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d7d77-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

