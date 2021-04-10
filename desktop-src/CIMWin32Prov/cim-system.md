---
description: CIM \_ 系統類別會匯總 managed 系統專案的可列舉集合。
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: 'CIM_System 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936351"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="3ce6c-103">CIM_System 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3ce6c-104">**CIM \_ 系統** 類別會匯總 managed 系統專案的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="3ce6c-105">匯總會以整體功能的形式運作。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="3ce6c-106">在系統的任何特定子類別內，都有一個定義完善的 managed 系統專案類別清單，這些類別的實例必須加以匯總。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="3ce6c-107">**Cim \_ 系統** 物件及其衍生型為 cim 的最上層物件。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="3ce6c-108">它們提供許多元件的範圍，而且必須有唯一的系統金鑰。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ce6c-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3ce6c-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3ce6c-111">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3ce6c-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce6c-113">語法</span><span class="sxs-lookup"><span data-stu-id="3ce6c-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="3ce6c-114">成員</span><span class="sxs-lookup"><span data-stu-id="3ce6c-114">Members</span></span>

<span data-ttu-id="3ce6c-115">**CIM \_ 系統** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ce6c-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="3ce6c-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3ce6c-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ce6c-117">屬性</span><span class="sxs-lookup"><span data-stu-id="3ce6c-117">Properties</span></span>

<span data-ttu-id="3ce6c-118">**CIM \_ 系統** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ce6c-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-123">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-123">A short textual description of the object.</span></span>

<span data-ttu-id="3ce6c-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-128">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3ce6c-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-129">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3ce6c-130">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-134">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-135">A textual description of the object.</span></span>

<span data-ttu-id="3ce6c-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="3ce6c-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-141">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-141">Indicates when the object was installed.</span></span> <span data-ttu-id="3ce6c-142">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3ce6c-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-147">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ce6c-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-148">定義物件已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-152">使用子類別啟發學習法識別系統名稱的產生方式。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-153">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-156">如何聯繫主要系統擁有者 (例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-157">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-160">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-161">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-162">**角色**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-163">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3ce6c-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3ce6c-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-165">系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="3ce6c-166">系統的子類別可以覆寫這個屬性，以定義明確的角色值。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="3ce6c-167">或者，工作群組也可以描述指定角色的啟發學習法、慣例和指導方針。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="3ce6c-168">例如，如果是網路系統的實例，這個屬性可能會包含 "Switch" 或 "Bridge" 字串。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="3ce6c-169">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ce6c-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ce6c-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ce6c-172">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3ce6c-173">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="3ce6c-174">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3ce6c-175">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3ce6c-176">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3ce6c-177">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3ce6c-178">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3ce6c-179">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3ce6c-180">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3ce6c-181">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="3ce6c-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3ce6c-182">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3ce6c-183">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3ce6c-184">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ce6c-185">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3ce6c-186">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3ce6c-187">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3ce6c-188">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3ce6c-189">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3ce6c-190">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3ce6c-191">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3ce6c-192">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3ce6c-193">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="3ce6c-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="3ce6c-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3ce6c-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3ce6c-195">備註</span><span class="sxs-lookup"><span data-stu-id="3ce6c-195">Remarks</span></span>

<span data-ttu-id="3ce6c-196">**Cim \_ 系統** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="3ce6c-197">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-197">WMI does not implement this class.</span></span> <span data-ttu-id="3ce6c-198">針對衍生自 **CIM \_ 系統** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3ce6c-199">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3ce6c-200">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3ce6c-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce6c-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ce6c-201">Requirements</span></span>



| <span data-ttu-id="3ce6c-202">需求</span><span class="sxs-lookup"><span data-stu-id="3ce6c-202">Requirement</span></span> | <span data-ttu-id="3ce6c-203">值</span><span class="sxs-lookup"><span data-stu-id="3ce6c-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce6c-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ce6c-204">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce6c-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ce6c-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ce6c-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ce6c-206">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce6c-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ce6c-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ce6c-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="3ce6c-208">Namespace</span></span><br/>                | <span data-ttu-id="3ce6c-209">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3ce6c-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ce6c-210">MOF</span><span class="sxs-lookup"><span data-stu-id="3ce6c-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ce6c-211"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ce6c-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ce6c-212">DLL</span><span class="sxs-lookup"><span data-stu-id="3ce6c-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ce6c-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ce6c-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce6c-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ce6c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce6c-215">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="3ce6c-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

