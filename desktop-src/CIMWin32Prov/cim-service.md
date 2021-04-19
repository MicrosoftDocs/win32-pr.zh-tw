---
description: CIM \_ 服務類別代表邏輯元素，其中包含的資訊可代表和管理裝置或軟體功能所提供的功能。
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: 'CIM_Service 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972963"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="04374-103">CIM_Service 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="04374-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="04374-104">**CIM \_ 服務** 類別代表邏輯元素，其中包含的資訊可代表和管理裝置或軟體功能所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="04374-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="04374-105">服務是一般用途的物件，用來設定及管理功能的執行;這並不是功能本身。</span><span class="sxs-lookup"><span data-stu-id="04374-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04374-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="04374-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="04374-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="04374-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="04374-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="04374-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="04374-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="04374-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="04374-110">語法</span><span class="sxs-lookup"><span data-stu-id="04374-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="04374-111">成員</span><span class="sxs-lookup"><span data-stu-id="04374-111">Members</span></span>

<span data-ttu-id="04374-112">**CIM \_ 服務** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04374-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="04374-113">方法</span><span class="sxs-lookup"><span data-stu-id="04374-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="04374-114">屬性</span><span class="sxs-lookup"><span data-stu-id="04374-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04374-115">方法</span><span class="sxs-lookup"><span data-stu-id="04374-115">Methods</span></span>

<span data-ttu-id="04374-116">**CIM \_ 服務** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="04374-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="04374-117">方法</span><span class="sxs-lookup"><span data-stu-id="04374-117">Method</span></span>                                                           | <span data-ttu-id="04374-118">描述</span><span class="sxs-lookup"><span data-stu-id="04374-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04374-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="04374-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="04374-120">嘗試讓服務進入啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="04374-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="04374-121">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="04374-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="04374-122">**StopService**</span><span class="sxs-lookup"><span data-stu-id="04374-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="04374-123">將服務置於已停止狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="04374-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="04374-124">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="04374-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="04374-125">屬性</span><span class="sxs-lookup"><span data-stu-id="04374-125">Properties</span></span>

<span data-ttu-id="04374-126">**CIM \_ 服務** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04374-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04374-127">**標題**</span><span class="sxs-lookup"><span data-stu-id="04374-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-130">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="04374-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="04374-131">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="04374-131">A short textual description of the object.</span></span>

<span data-ttu-id="04374-132">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="04374-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04374-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04374-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-136">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="04374-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="04374-137">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="04374-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="04374-138">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="04374-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="04374-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="04374-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-142">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="04374-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="04374-143">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="04374-143">A textual description of the object.</span></span>

<span data-ttu-id="04374-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="04374-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04374-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="04374-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="04374-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04374-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="04374-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="04374-149">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="04374-149">Indicates when the object was installed.</span></span> <span data-ttu-id="04374-150">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="04374-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="04374-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="04374-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04374-152">**名稱**</span><span class="sxs-lookup"><span data-stu-id="04374-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-155">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="04374-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="04374-156">Name 屬性可唯一識別服務，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="04374-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="04374-157">此功能在物件的 Description 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="04374-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="04374-158">**已開始**</span><span class="sxs-lookup"><span data-stu-id="04374-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-159">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04374-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04374-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-161">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="04374-162">若 **為 TRUE**，表示服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="04374-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="04374-163">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="04374-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-166">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="04374-167">指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="04374-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="04374-168">**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="04374-169">**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04374-170">**狀態**</span><span class="sxs-lookup"><span data-stu-id="04374-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-173">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="04374-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="04374-174">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="04374-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="04374-175">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="04374-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="04374-176">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="04374-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="04374-177">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="04374-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="04374-178">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="04374-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="04374-179">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="04374-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="04374-180">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="04374-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="04374-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="04374-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="04374-182">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="04374-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="04374-183">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="04374-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="04374-184">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="04374-185">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04374-186">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="04374-187">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="04374-188">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="04374-189">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="04374-190">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="04374-191">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="04374-192">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="04374-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="04374-193">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="04374-194">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="04374-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04374-195">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04374-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-198">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="04374-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="04374-199">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="04374-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="04374-200">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="04374-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04374-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04374-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04374-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04374-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04374-203">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="04374-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="04374-204">裝載服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="04374-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04374-205">備註</span><span class="sxs-lookup"><span data-stu-id="04374-205">Remarks</span></span>

<span data-ttu-id="04374-206">**Cim \_ 服務** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="04374-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="04374-207">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="04374-207">WMI does not implement this class.</span></span> <span data-ttu-id="04374-208">針對衍生自 **CIM \_ 服務** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="04374-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="04374-209">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="04374-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="04374-210">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="04374-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="04374-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="04374-211">Requirements</span></span>



| <span data-ttu-id="04374-212">需求</span><span class="sxs-lookup"><span data-stu-id="04374-212">Requirement</span></span> | <span data-ttu-id="04374-213">值</span><span class="sxs-lookup"><span data-stu-id="04374-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04374-214">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04374-214">Minimum supported client</span></span><br/> | <span data-ttu-id="04374-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04374-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04374-216">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04374-216">Minimum supported server</span></span><br/> | <span data-ttu-id="04374-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04374-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04374-218">命名空間</span><span class="sxs-lookup"><span data-stu-id="04374-218">Namespace</span></span><br/>                | <span data-ttu-id="04374-219">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="04374-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04374-220">MOF</span><span class="sxs-lookup"><span data-stu-id="04374-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04374-221"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="04374-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04374-222">DLL</span><span class="sxs-lookup"><span data-stu-id="04374-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04374-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04374-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04374-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04374-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04374-225">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="04374-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

