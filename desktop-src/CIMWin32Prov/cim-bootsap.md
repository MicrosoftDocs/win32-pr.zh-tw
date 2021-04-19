---
description: CIM \_ BootSAP 類別代表開機服務的存取點。
ms.assetid: eea6d6c5-3930-4e20-b7d3-b6d5722662cd
ms.tgt_platform: multiple
title: CIM_BootSAP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootSAP
- CIM_BootSAP.Caption
- CIM_BootSAP.Description
- CIM_BootSAP.InstallDate
- CIM_BootSAP.Status
- CIM_BootSAP.CreationClassName
- CIM_BootSAP.Name
- CIM_BootSAP.SystemCreationClassName
- CIM_BootSAP.SystemName
- CIM_BootSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4868497c2d604457a45273b1c0cc609ae361ad9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970329"
---
# <a name="cim_bootsap-class"></a><span data-ttu-id="dfba0-103">CIM \_ BootSAP 類別</span><span class="sxs-lookup"><span data-stu-id="dfba0-103">CIM\_BootSAP class</span></span>

<span data-ttu-id="dfba0-104">**CIM \_ BootSAP** 類別代表開機服務的存取點。</span><span class="sxs-lookup"><span data-stu-id="dfba0-104">The **CIM\_BootSAP** class represents the access points of a boot service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfba0-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="dfba0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dfba0-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dfba0-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dfba0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dfba0-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="dfba0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfba0-109">語法</span><span class="sxs-lookup"><span data-stu-id="dfba0-109">Syntax</span></span>

``` syntax
[UUID("{F6FEF20A-E3D2-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootSAP : CIM_ServiceAccessPoint
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

## <a name="members"></a><span data-ttu-id="dfba0-110">成員</span><span class="sxs-lookup"><span data-stu-id="dfba0-110">Members</span></span>

<span data-ttu-id="dfba0-111">**CIM \_ BootSAP** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dfba0-111">The **CIM\_BootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="dfba0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="dfba0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfba0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="dfba0-113">Properties</span></span>

<span data-ttu-id="dfba0-114">**CIM \_ BootSAP** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dfba0-114">The **CIM\_BootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfba0-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="dfba0-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="dfba0-119">A short textual description of the object.</span></span>

<span data-ttu-id="dfba0-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dfba0-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-124">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="dfba0-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-125">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfba0-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dfba0-126">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="dfba0-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dfba0-127">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="dfba0-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-131">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-132">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="dfba0-132">A textual description of the object.</span></span>

<span data-ttu-id="dfba0-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dfba0-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-135">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dfba0-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-137">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="dfba0-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-138">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="dfba0-138">Indicates when the object was installed.</span></span> <span data-ttu-id="dfba0-139">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="dfba0-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="dfba0-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="dfba0-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-144">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="dfba0-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-145">可唯一識別服務存取點，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="dfba0-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="dfba0-146">此功能在物件的 Description 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="dfba0-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="dfba0-147">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-148">**狀態**</span><span class="sxs-lookup"><span data-stu-id="dfba0-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-152">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="dfba0-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="dfba0-153">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="dfba0-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="dfba0-154">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="dfba0-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="dfba0-155">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="dfba0-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="dfba0-156">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="dfba0-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dfba0-157">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="dfba0-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dfba0-158">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="dfba0-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dfba0-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dfba0-160">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="dfba0-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dfba0-161">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dfba0-162">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dfba0-163">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfba0-164">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dfba0-165">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dfba0-166">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dfba0-167">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dfba0-168">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dfba0-169">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dfba0-170">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dfba0-171">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dfba0-172">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dfba0-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dfba0-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-176">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="dfba0-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-177">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="dfba0-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="dfba0-178">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dfba0-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfba0-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-182">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="dfba0-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-183">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfba0-183">The scoping system's name.</span></span>

<span data-ttu-id="dfba0-184">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfba0-185">**型別**</span><span class="sxs-lookup"><span data-stu-id="dfba0-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfba0-186">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dfba0-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfba0-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfba0-188">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="dfba0-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dfba0-189">SAP 的類型，例如 [已連接] 或 [已重新導向]。</span><span class="sxs-lookup"><span data-stu-id="dfba0-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="dfba0-190">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="dfba0-191">**寫入** (1) </span><span class="sxs-lookup"><span data-stu-id="dfba0-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="dfba0-192">**閱讀** (2) </span><span class="sxs-lookup"><span data-stu-id="dfba0-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="dfba0-193">重新 **導向** (4) </span><span class="sxs-lookup"><span data-stu-id="dfba0-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="dfba0-194">**Net \_附加** (8) </span><span class="sxs-lookup"><span data-stu-id="dfba0-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfba0-195">**未知** 的 (16) </span><span class="sxs-lookup"><span data-stu-id="dfba0-195">**unknown** (16)</span></span>


<span data-ttu-id="dfba0-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dfba0-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dfba0-197">備註</span><span class="sxs-lookup"><span data-stu-id="dfba0-197">Remarks</span></span>

<span data-ttu-id="dfba0-198">**Cim \_ BootSAP** 類別衍生自 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="dfba0-198">The **CIM\_BootSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="dfba0-199">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="dfba0-199">WMI does not implement this class.</span></span>

<span data-ttu-id="dfba0-200">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="dfba0-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dfba0-201">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dfba0-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfba0-202">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfba0-202">Requirements</span></span>



| <span data-ttu-id="dfba0-203">需求</span><span class="sxs-lookup"><span data-stu-id="dfba0-203">Requirement</span></span> | <span data-ttu-id="dfba0-204">值</span><span class="sxs-lookup"><span data-stu-id="dfba0-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfba0-205">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfba0-205">Minimum supported client</span></span><br/> | <span data-ttu-id="dfba0-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfba0-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfba0-207">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfba0-207">Minimum supported server</span></span><br/> | <span data-ttu-id="dfba0-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfba0-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfba0-209">命名空間</span><span class="sxs-lookup"><span data-stu-id="dfba0-209">Namespace</span></span><br/>                | <span data-ttu-id="dfba0-210">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfba0-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfba0-211">MOF</span><span class="sxs-lookup"><span data-stu-id="dfba0-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfba0-212"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfba0-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfba0-213">DLL</span><span class="sxs-lookup"><span data-stu-id="dfba0-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfba0-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfba0-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfba0-215">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfba0-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfba0-216">**CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="dfba0-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

