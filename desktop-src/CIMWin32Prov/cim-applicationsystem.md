---
description: CIM \_ ApplicationSystem 類別代表支援特定商務功能的應用程式或軟體系統，可作為獨立的單位來管理。
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: CIM_ApplicationSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998049"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="5f02c-103">CIM \_ ApplicationSystem 類別</span><span class="sxs-lookup"><span data-stu-id="5f02c-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="5f02c-104">**CIM \_ ApplicationSystem** 類別代表支援特定商務功能的應用程式或軟體系統，可作為獨立的單位來管理。</span><span class="sxs-lookup"><span data-stu-id="5f02c-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="5f02c-105">這類系統可使用 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) 類別分解為其功能性元件。</span><span class="sxs-lookup"><span data-stu-id="5f02c-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="5f02c-106">特定應用程式或軟體系統的軟體功能位於使用 [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="5f02c-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f02c-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5f02c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5f02c-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5f02c-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5f02c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5f02c-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5f02c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f02c-111">語法</span><span class="sxs-lookup"><span data-stu-id="5f02c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="5f02c-112">成員</span><span class="sxs-lookup"><span data-stu-id="5f02c-112">Members</span></span>

<span data-ttu-id="5f02c-113">**CIM \_ ApplicationSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5f02c-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="5f02c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5f02c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f02c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="5f02c-115">Properties</span></span>

<span data-ttu-id="5f02c-116">**CIM \_ ApplicationSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5f02c-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f02c-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="5f02c-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="5f02c-121">A short textual description of the object.</span></span>

<span data-ttu-id="5f02c-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5f02c-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-126">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f02c-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-127">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f02c-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5f02c-128">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="5f02c-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5f02c-129">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-130">**說明**</span><span class="sxs-lookup"><span data-stu-id="5f02c-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-133">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-134">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="5f02c-134">A textual description of the object.</span></span>

<span data-ttu-id="5f02c-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5f02c-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-137">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5f02c-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="5f02c-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-140">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="5f02c-140">Indicates when the object was installed.</span></span> <span data-ttu-id="5f02c-141">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="5f02c-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5f02c-142">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5f02c-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f02c-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-147">定義物件已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="5f02c-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="5f02c-148">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="5f02c-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-152">使用子類別啟發學習法識別系統名稱的產生方式。</span><span class="sxs-lookup"><span data-stu-id="5f02c-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="5f02c-153">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-154">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="5f02c-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-157">如何聯繫主要系統擁有者 (例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="5f02c-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="5f02c-158">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-159">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="5f02c-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-162">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="5f02c-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-163">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f02c-163">Name of the primary system owner.</span></span>

<span data-ttu-id="5f02c-164">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-165">**角色**</span><span class="sxs-lookup"><span data-stu-id="5f02c-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-166">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5f02c-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5f02c-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-168">系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="5f02c-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="5f02c-169">系統的子類別可以覆寫這個屬性，以定義明確的角色值。</span><span class="sxs-lookup"><span data-stu-id="5f02c-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="5f02c-170">或者，工作群組也可以描述指定角色的啟發學習法、慣例和指導方針。</span><span class="sxs-lookup"><span data-stu-id="5f02c-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="5f02c-171">例如，如果是網路系統的實例，這個屬性可能會包含 "Switch" 或 "Bridge" 字串。</span><span class="sxs-lookup"><span data-stu-id="5f02c-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="5f02c-172">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f02c-173">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5f02c-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f02c-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f02c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f02c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f02c-176">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5f02c-177">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="5f02c-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="5f02c-178">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="5f02c-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5f02c-179">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="5f02c-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5f02c-180">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="5f02c-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5f02c-181">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="5f02c-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5f02c-182">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="5f02c-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5f02c-183">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="5f02c-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5f02c-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5f02c-185">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="5f02c-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5f02c-186">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5f02c-187">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5f02c-188">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f02c-189">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5f02c-190">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5f02c-191">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5f02c-192">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5f02c-193">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5f02c-194">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5f02c-195">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5f02c-196">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5f02c-197">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="5f02c-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5f02c-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5f02c-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5f02c-199">備註</span><span class="sxs-lookup"><span data-stu-id="5f02c-199">Remarks</span></span>

<span data-ttu-id="5f02c-200">**Cim \_ ApplicationSystem** 類別衍生自 [**cim \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="5f02c-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="5f02c-201">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5f02c-201">WMI does not implement this class.</span></span>

<span data-ttu-id="5f02c-202">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5f02c-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5f02c-203">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5f02c-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f02c-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f02c-204">Requirements</span></span>



| <span data-ttu-id="5f02c-205">需求</span><span class="sxs-lookup"><span data-stu-id="5f02c-205">Requirement</span></span> | <span data-ttu-id="5f02c-206">值</span><span class="sxs-lookup"><span data-stu-id="5f02c-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f02c-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f02c-207">Minimum supported client</span></span><br/> | <span data-ttu-id="5f02c-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f02c-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f02c-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f02c-209">Minimum supported server</span></span><br/> | <span data-ttu-id="5f02c-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f02c-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f02c-211">命名空間</span><span class="sxs-lookup"><span data-stu-id="5f02c-211">Namespace</span></span><br/>                | <span data-ttu-id="5f02c-212">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5f02c-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f02c-213">MOF</span><span class="sxs-lookup"><span data-stu-id="5f02c-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f02c-214"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f02c-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f02c-215">DLL</span><span class="sxs-lookup"><span data-stu-id="5f02c-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f02c-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f02c-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f02c-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f02c-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f02c-218">**CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="5f02c-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

