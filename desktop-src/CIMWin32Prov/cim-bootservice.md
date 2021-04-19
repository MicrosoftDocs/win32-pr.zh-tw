---
description: CIM \_ BootService 類別代表裝置或軟體所提供的功能，或由網路所提供的功能，可將作業系統載入到單一電腦系統上。
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: CIM_BootService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991643"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="d9995-103">CIM \_ BootService 類別</span><span class="sxs-lookup"><span data-stu-id="d9995-103">CIM\_BootService class</span></span>

<span data-ttu-id="d9995-104">**CIM \_ BootService** 類別代表裝置或軟體所提供的功能，或由網路所提供的功能，可將作業系統載入到單一電腦系統上。</span><span class="sxs-lookup"><span data-stu-id="d9995-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9995-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d9995-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d9995-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d9995-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d9995-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9995-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d9995-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="d9995-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9995-109">語法</span><span class="sxs-lookup"><span data-stu-id="d9995-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="d9995-110">成員</span><span class="sxs-lookup"><span data-stu-id="d9995-110">Members</span></span>

<span data-ttu-id="d9995-111">**CIM \_ BootService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d9995-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="d9995-112">方法</span><span class="sxs-lookup"><span data-stu-id="d9995-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d9995-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d9995-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d9995-114">方法</span><span class="sxs-lookup"><span data-stu-id="d9995-114">Methods</span></span>

<span data-ttu-id="d9995-115">**CIM \_ BootService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d9995-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="d9995-116">方法</span><span class="sxs-lookup"><span data-stu-id="d9995-116">Method</span></span>                                                               | <span data-ttu-id="d9995-117">描述</span><span class="sxs-lookup"><span data-stu-id="d9995-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="d9995-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="d9995-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="d9995-119">將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="d9995-119">Puts the service in the started state.</span></span> <span data-ttu-id="d9995-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d9995-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="d9995-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="d9995-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="d9995-122">將服務置於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="d9995-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="d9995-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d9995-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d9995-124">屬性</span><span class="sxs-lookup"><span data-stu-id="d9995-124">Properties</span></span>

<span data-ttu-id="d9995-125">**CIM \_ BootService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d9995-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9995-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="d9995-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-129">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="d9995-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-130">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="d9995-130">A short textual description of the object.</span></span>

<span data-ttu-id="d9995-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d9995-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-135">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="d9995-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-136">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9995-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d9995-137">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="d9995-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d9995-138">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="d9995-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-142">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="d9995-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-143">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="d9995-143">A textual description of the object.</span></span>

<span data-ttu-id="d9995-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d9995-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d9995-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="d9995-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-149">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="d9995-149">Indicates when the object was installed.</span></span> <span data-ttu-id="d9995-150">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d9995-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d9995-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-152">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d9995-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-155">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9995-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9995-156">Name 屬性可唯一識別服務，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="d9995-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="d9995-157">此功能在物件的 **Description** 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="d9995-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="d9995-158">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-159">**已開始**</span><span class="sxs-lookup"><span data-stu-id="d9995-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-160">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d9995-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-162">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-163">若 **為 TRUE**，表示服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="d9995-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="d9995-164">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-165">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="d9995-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-168">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-169">指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="d9995-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="d9995-170">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="d9995-171">**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="d9995-172">**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9995-173">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d9995-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-176">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="d9995-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-177">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="d9995-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="d9995-178">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="d9995-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d9995-179">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="d9995-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d9995-180">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="d9995-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d9995-181">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d9995-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d9995-182">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="d9995-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d9995-183">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d9995-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d9995-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d9995-185">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="d9995-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d9995-186">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d9995-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d9995-187">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d9995-188">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d9995-189">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d9995-190">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d9995-191">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d9995-192">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d9995-193">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d9995-194">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d9995-195">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="d9995-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d9995-196">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d9995-197">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="d9995-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9995-198">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d9995-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-201">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="d9995-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-202">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="d9995-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="d9995-203">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9995-204">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d9995-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d9995-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d9995-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-207">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="d9995-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d9995-208">裝載服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="d9995-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="d9995-209">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9995-210">備註</span><span class="sxs-lookup"><span data-stu-id="d9995-210">Remarks</span></span>

<span data-ttu-id="d9995-211">**Cim \_ BootService** 類別衍生自 [**cim \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d9995-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="d9995-212">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="d9995-212">WMI does not implement this class.</span></span>

<span data-ttu-id="d9995-213">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d9995-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d9995-214">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d9995-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9995-215">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9995-215">Requirements</span></span>



| <span data-ttu-id="d9995-216">需求</span><span class="sxs-lookup"><span data-stu-id="d9995-216">Requirement</span></span> | <span data-ttu-id="d9995-217">值</span><span class="sxs-lookup"><span data-stu-id="d9995-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9995-218">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9995-218">Minimum supported client</span></span><br/> | <span data-ttu-id="d9995-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9995-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9995-220">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9995-220">Minimum supported server</span></span><br/> | <span data-ttu-id="d9995-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9995-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9995-222">命名空間</span><span class="sxs-lookup"><span data-stu-id="d9995-222">Namespace</span></span><br/>                | <span data-ttu-id="d9995-223">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d9995-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9995-224">MOF</span><span class="sxs-lookup"><span data-stu-id="d9995-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9995-225"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9995-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9995-226">DLL</span><span class="sxs-lookup"><span data-stu-id="d9995-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9995-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9995-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9995-228">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9995-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9995-229">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="d9995-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

