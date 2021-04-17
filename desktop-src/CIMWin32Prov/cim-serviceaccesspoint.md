---
description: CIM \_ ServiceAccessPoint 類別代表使用或叫用服務的能力。 存取點代表可供其他實體使用的服務。
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: 'CIM_ServiceAccessPoint 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510532"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="710bb-104">CIM_ServiceAccessPoint 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="710bb-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="710bb-105">**CIM \_ ServiceAccessPoint** 類別代表使用或叫用服務的能力。</span><span class="sxs-lookup"><span data-stu-id="710bb-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="710bb-106">存取點代表可供其他實體使用的服務。</span><span class="sxs-lookup"><span data-stu-id="710bb-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="710bb-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="710bb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="710bb-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="710bb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="710bb-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="710bb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="710bb-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="710bb-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="710bb-111">語法</span><span class="sxs-lookup"><span data-stu-id="710bb-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="710bb-112">成員</span><span class="sxs-lookup"><span data-stu-id="710bb-112">Members</span></span>

<span data-ttu-id="710bb-113">**CIM \_ ServiceAccessPoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="710bb-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="710bb-114">屬性</span><span class="sxs-lookup"><span data-stu-id="710bb-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="710bb-115">屬性</span><span class="sxs-lookup"><span data-stu-id="710bb-115">Properties</span></span>

<span data-ttu-id="710bb-116">**CIM \_ ServiceAccessPoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="710bb-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="710bb-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="710bb-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="710bb-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="710bb-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="710bb-121">A short textual description of the object.</span></span>

<span data-ttu-id="710bb-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="710bb-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="710bb-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="710bb-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-126">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="710bb-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="710bb-127">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="710bb-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="710bb-128">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="710bb-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="710bb-129">**說明**</span><span class="sxs-lookup"><span data-stu-id="710bb-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-132">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="710bb-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="710bb-133">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="710bb-133">A textual description of the object.</span></span>

<span data-ttu-id="710bb-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="710bb-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="710bb-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="710bb-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-136">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="710bb-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="710bb-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="710bb-139">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="710bb-139">Indicates when the object was installed.</span></span> <span data-ttu-id="710bb-140">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="710bb-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="710bb-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="710bb-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="710bb-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="710bb-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-145">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="710bb-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="710bb-146">可唯一識別服務存取點，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="710bb-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="710bb-147">此功能在物件的 Description 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="710bb-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="710bb-148">**狀態**</span><span class="sxs-lookup"><span data-stu-id="710bb-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="710bb-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="710bb-152">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="710bb-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="710bb-153">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="710bb-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="710bb-154">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="710bb-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="710bb-155">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="710bb-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="710bb-156">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="710bb-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="710bb-157">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="710bb-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="710bb-158">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="710bb-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="710bb-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="710bb-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="710bb-160">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="710bb-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="710bb-161">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="710bb-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="710bb-162">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="710bb-163">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="710bb-164">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="710bb-165">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="710bb-166">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="710bb-167">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="710bb-168">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="710bb-169">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="710bb-170">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="710bb-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="710bb-171">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="710bb-172">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="710bb-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="710bb-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="710bb-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-176">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="710bb-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="710bb-177">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="710bb-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="710bb-178">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="710bb-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="710bb-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-181">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="710bb-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="710bb-182">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="710bb-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="710bb-183">**型別**</span><span class="sxs-lookup"><span data-stu-id="710bb-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="710bb-184">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="710bb-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="710bb-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="710bb-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="710bb-186">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="710bb-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="710bb-187">SAP 的類型，例如 [已連接] 或 [已重新導向]。</span><span class="sxs-lookup"><span data-stu-id="710bb-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="710bb-188">**寫入** (1) </span><span class="sxs-lookup"><span data-stu-id="710bb-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="710bb-189">**閱讀** (2) </span><span class="sxs-lookup"><span data-stu-id="710bb-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="710bb-190">重新 **導向** (4) </span><span class="sxs-lookup"><span data-stu-id="710bb-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="710bb-191">**Net \_附加** (8) </span><span class="sxs-lookup"><span data-stu-id="710bb-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="710bb-192">**未知** 的 (16) </span><span class="sxs-lookup"><span data-stu-id="710bb-192">**unknown** (16)</span></span>


<span data-ttu-id="710bb-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="710bb-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="710bb-194">備註</span><span class="sxs-lookup"><span data-stu-id="710bb-194">Remarks</span></span>

<span data-ttu-id="710bb-195">**Cim \_ ServiceAccessPoint** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="710bb-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="710bb-196">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="710bb-196">WMI does not implement this class.</span></span> <span data-ttu-id="710bb-197">針對衍生自 **CIM \_ SERVICEACCESSPOINT** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="710bb-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="710bb-198">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="710bb-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="710bb-199">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="710bb-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="710bb-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="710bb-200">Requirements</span></span>



| <span data-ttu-id="710bb-201">需求</span><span class="sxs-lookup"><span data-stu-id="710bb-201">Requirement</span></span> | <span data-ttu-id="710bb-202">值</span><span class="sxs-lookup"><span data-stu-id="710bb-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="710bb-203">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="710bb-203">Minimum supported client</span></span><br/> | <span data-ttu-id="710bb-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="710bb-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="710bb-205">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="710bb-205">Minimum supported server</span></span><br/> | <span data-ttu-id="710bb-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="710bb-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="710bb-207">命名空間</span><span class="sxs-lookup"><span data-stu-id="710bb-207">Namespace</span></span><br/>                | <span data-ttu-id="710bb-208">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="710bb-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="710bb-209">MOF</span><span class="sxs-lookup"><span data-stu-id="710bb-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="710bb-210"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="710bb-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="710bb-211">DLL</span><span class="sxs-lookup"><span data-stu-id="710bb-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="710bb-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="710bb-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710bb-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="710bb-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710bb-214">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="710bb-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

