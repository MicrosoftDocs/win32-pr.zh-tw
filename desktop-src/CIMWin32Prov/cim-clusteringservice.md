---
description: CIM \_ ClusteringService 類別代表叢集所提供的功能。 例如，容錯移轉功能可以模型化為容錯移轉叢集的服務。
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: CIM_ClusteringService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973174"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="4986f-104">CIM \_ ClusteringService 類別</span><span class="sxs-lookup"><span data-stu-id="4986f-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="4986f-105">**CIM \_ ClusteringService** 類別代表叢集所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="4986f-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="4986f-106">例如，容錯移轉功能可以模型化為容錯移轉叢集的服務。</span><span class="sxs-lookup"><span data-stu-id="4986f-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4986f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4986f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4986f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4986f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4986f-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4986f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4986f-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4986f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4986f-111">語法</span><span class="sxs-lookup"><span data-stu-id="4986f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="4986f-112">成員</span><span class="sxs-lookup"><span data-stu-id="4986f-112">Members</span></span>

<span data-ttu-id="4986f-113">**CIM \_ ClusteringService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4986f-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="4986f-114">方法</span><span class="sxs-lookup"><span data-stu-id="4986f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="4986f-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4986f-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4986f-116">方法</span><span class="sxs-lookup"><span data-stu-id="4986f-116">Methods</span></span>

<span data-ttu-id="4986f-117">**CIM \_ ClusteringService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4986f-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="4986f-118">方法</span><span class="sxs-lookup"><span data-stu-id="4986f-118">Method</span></span>                                                                     | <span data-ttu-id="4986f-119">描述</span><span class="sxs-lookup"><span data-stu-id="4986f-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4986f-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="4986f-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="4986f-121">將新電腦系統帶入叢集中的類別方法。</span><span class="sxs-lookup"><span data-stu-id="4986f-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="4986f-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="4986f-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="4986f-123">**EvictNode**</span><span class="sxs-lookup"><span data-stu-id="4986f-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="4986f-124">從叢集中移除電腦系統的類別方法。</span><span class="sxs-lookup"><span data-stu-id="4986f-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="4986f-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="4986f-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="4986f-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4986f-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="4986f-127">嘗試將服務置於啟動狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="4986f-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="4986f-128">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="4986f-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="4986f-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4986f-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="4986f-130">將服務置於已停止狀態的類別方法。</span><span class="sxs-lookup"><span data-stu-id="4986f-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="4986f-131">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="4986f-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="4986f-132">屬性</span><span class="sxs-lookup"><span data-stu-id="4986f-132">Properties</span></span>

<span data-ttu-id="4986f-133">**CIM \_ ClusteringService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4986f-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4986f-134">**標題**</span><span class="sxs-lookup"><span data-stu-id="4986f-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-137">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4986f-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-138">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4986f-138">A short textual description of the object.</span></span>

<span data-ttu-id="4986f-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-140">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4986f-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-143">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="4986f-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-144">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4986f-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4986f-145">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4986f-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4986f-146">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-147">**說明**</span><span class="sxs-lookup"><span data-stu-id="4986f-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-150">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4986f-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-151">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4986f-151">A textual description of the object.</span></span>

<span data-ttu-id="4986f-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4986f-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-154">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4986f-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-156">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4986f-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-157">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="4986f-157">Indicates when the object was installed.</span></span> <span data-ttu-id="4986f-158">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="4986f-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4986f-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-160">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4986f-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-163">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4986f-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4986f-164">Name 屬性可唯一識別服務，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="4986f-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="4986f-165">此功能在物件的 Description 屬性中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="4986f-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="4986f-166">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-167">**已開始**</span><span class="sxs-lookup"><span data-stu-id="4986f-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4986f-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-170">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-171">若 **為 TRUE**，表示服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="4986f-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="4986f-172">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-173">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4986f-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-176">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-177">指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="4986f-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="4986f-178">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="4986f-179">**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4986f-180">**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4986f-181">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4986f-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-184">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4986f-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-185">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="4986f-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="4986f-186">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="4986f-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4986f-187">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="4986f-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4986f-188">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="4986f-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4986f-189">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4986f-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4986f-190">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="4986f-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4986f-191">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4986f-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4986f-192">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4986f-193">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4986f-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4986f-194">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4986f-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4986f-195">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4986f-196">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4986f-197">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4986f-198">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4986f-199">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4986f-200">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4986f-201">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4986f-202">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4986f-203">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4986f-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4986f-204">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4986f-205">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4986f-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4986f-206">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4986f-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-209">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="4986f-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-210">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="4986f-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="4986f-211">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4986f-212">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4986f-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4986f-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4986f-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4986f-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4986f-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4986f-215">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="4986f-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="4986f-216">裝載服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="4986f-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="4986f-217">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4986f-218">備註</span><span class="sxs-lookup"><span data-stu-id="4986f-218">Remarks</span></span>

<span data-ttu-id="4986f-219">**Cim \_ ClusteringService** 類別衍生自 [**cim \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="4986f-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="4986f-220">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4986f-220">WMI does not implement this class.</span></span>

<span data-ttu-id="4986f-221">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4986f-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4986f-222">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4986f-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4986f-223">規格需求</span><span class="sxs-lookup"><span data-stu-id="4986f-223">Requirements</span></span>



| <span data-ttu-id="4986f-224">需求</span><span class="sxs-lookup"><span data-stu-id="4986f-224">Requirement</span></span> | <span data-ttu-id="4986f-225">值</span><span class="sxs-lookup"><span data-stu-id="4986f-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4986f-226">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4986f-226">Minimum supported client</span></span><br/> | <span data-ttu-id="4986f-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4986f-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4986f-228">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4986f-228">Minimum supported server</span></span><br/> | <span data-ttu-id="4986f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4986f-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4986f-230">命名空間</span><span class="sxs-lookup"><span data-stu-id="4986f-230">Namespace</span></span><br/>                | <span data-ttu-id="4986f-231">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4986f-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4986f-232">MOF</span><span class="sxs-lookup"><span data-stu-id="4986f-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4986f-233"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4986f-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4986f-234">DLL</span><span class="sxs-lookup"><span data-stu-id="4986f-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4986f-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4986f-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4986f-236">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4986f-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4986f-237">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="4986f-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

