---
description: CIM 非 \_ 實例類別代表 cim ManagedSystemElement 實例的特殊集合 \_ 。
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: 'CIM_ComputerSystem 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468353"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="aef03-103">CIM_ComputerSystem 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="aef03-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="aef03-104">**Cim 非 \_** 實例類別代表 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)實例的特殊集合。</span><span class="sxs-lookup"><span data-stu-id="aef03-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="aef03-105">此集合提供電腦功能，並可做為匯總點，以建立下列一或多個專案的關聯：檔案系統、作業系統、處理器和記憶體 (volatile 和非暫時性儲存) 。</span><span class="sxs-lookup"><span data-stu-id="aef03-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="aef03-106">此類別衍生自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aef03-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="aef03-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aef03-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="aef03-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aef03-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aef03-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aef03-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="aef03-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef03-111">語法</span><span class="sxs-lookup"><span data-stu-id="aef03-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="aef03-112">成員</span><span class="sxs-lookup"><span data-stu-id="aef03-112">Members</span></span>

<span data-ttu-id="aef03-113">**CIM 同 \_** 型類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aef03-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="aef03-114">屬性</span><span class="sxs-lookup"><span data-stu-id="aef03-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aef03-115">屬性</span><span class="sxs-lookup"><span data-stu-id="aef03-115">Properties</span></span>

<span data-ttu-id="aef03-116">**CIM 無 \_** 類別類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aef03-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aef03-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="aef03-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aef03-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="aef03-121">A short textual description of the object.</span></span>

<span data-ttu-id="aef03-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aef03-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-126">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aef03-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aef03-127">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="aef03-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="aef03-128">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="aef03-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aef03-129">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-130">**說明**</span><span class="sxs-lookup"><span data-stu-id="aef03-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-133">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aef03-134">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="aef03-134">A textual description of the object.</span></span>

<span data-ttu-id="aef03-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aef03-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-137">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="aef03-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="aef03-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aef03-140">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="aef03-140">Indicates when the object was installed.</span></span> <span data-ttu-id="aef03-141">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="aef03-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="aef03-142">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="aef03-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aef03-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aef03-147">定義物件已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="aef03-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="aef03-148">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="aef03-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-152">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NameFormat" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="aef03-153">使用啟發學習法來識別電腦系統名稱的產生方式。</span><span class="sxs-lookup"><span data-stu-id="aef03-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="aef03-154">啟發學習法的詳細說明，位於 CIM V2 的一般模型規格中。</span><span class="sxs-lookup"><span data-stu-id="aef03-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="aef03-155">它假設已記載的規則會依序進行，以決定並指派名稱。</span><span class="sxs-lookup"><span data-stu-id="aef03-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="aef03-156">**NameFormat** 值清單會定義指派電腦系統名稱的優先順序。</span><span class="sxs-lookup"><span data-stu-id="aef03-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="aef03-157">有幾個規則會對應到相同的值。</span><span class="sxs-lookup"><span data-stu-id="aef03-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="aef03-158">請注意，物件的 **名稱** 是使用啟發學習法的系統金鑰值來計算。</span><span class="sxs-lookup"><span data-stu-id="aef03-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="aef03-159">您可以使用別名，為更適合商務的物件指派和使用其他名稱。</span><span class="sxs-lookup"><span data-stu-id="aef03-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="aef03-160">**Ip** ( 「ip」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="aef03-161">**撥號** ( 「撥號」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="aef03-162">**Hid** ( "hid" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="aef03-163">**NWA** ( "NWA" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="aef03-164">**HWA** ( "HWA" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="aef03-165">**X25** ( "x25" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="aef03-166">**Isdn** ( "isdn" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="aef03-167">**Ipx** ( 「ipx」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="aef03-168">**DCC** ( "DCC" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="aef03-169">**Icd** ( 「icd」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="aef03-170">**E.** ( "e. 164" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="aef03-171">**Sna** ( 「sna」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="aef03-172">**Oid/osi** ( "OID/osi" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aef03-173">**其他** ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aef03-174">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="aef03-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef03-177">如何聯繫主要系統擁有者 (例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="aef03-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="aef03-178">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-179">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="aef03-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-182">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="aef03-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aef03-183">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="aef03-183">Name of the primary system owner.</span></span>

<span data-ttu-id="aef03-184">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-185">**角色**</span><span class="sxs-lookup"><span data-stu-id="aef03-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-186">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="aef03-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aef03-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aef03-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aef03-188">系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="aef03-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="aef03-189">系統的子類別可以覆寫這個屬性，以定義明確的角色值。</span><span class="sxs-lookup"><span data-stu-id="aef03-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="aef03-190">或者，工作群組也可以描述指定角色的啟發學習法、慣例和指導方針。</span><span class="sxs-lookup"><span data-stu-id="aef03-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="aef03-191">例如，如果是網路系統的實例，這個屬性可能會包含 "Switch" 或 "Bridge" 字串。</span><span class="sxs-lookup"><span data-stu-id="aef03-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="aef03-192">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef03-193">**狀態**</span><span class="sxs-lookup"><span data-stu-id="aef03-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef03-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef03-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef03-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef03-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef03-196">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aef03-197">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="aef03-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="aef03-198">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="aef03-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="aef03-199">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="aef03-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="aef03-200">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="aef03-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="aef03-201">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="aef03-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aef03-202">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="aef03-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aef03-203">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="aef03-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aef03-204">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aef03-205">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="aef03-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aef03-206">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="aef03-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aef03-207">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aef03-208">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef03-209">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aef03-210">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aef03-211">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aef03-212">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aef03-213">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aef03-214">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aef03-215">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="aef03-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aef03-216">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aef03-217">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="aef03-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="aef03-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aef03-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="aef03-219">備註</span><span class="sxs-lookup"><span data-stu-id="aef03-219">Remarks</span></span>

<span data-ttu-id="aef03-220">**Cim 系統 \_** 類型衍生自 [**cim \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="aef03-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="aef03-221">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="aef03-221">WMI does not implement this class.</span></span> <span data-ttu-id="aef03-222">如需有關衍生自 CIM 的類別之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。 **\_**</span><span class="sxs-lookup"><span data-stu-id="aef03-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aef03-223">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="aef03-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aef03-224">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="aef03-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef03-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="aef03-225">Requirements</span></span>



| <span data-ttu-id="aef03-226">需求</span><span class="sxs-lookup"><span data-stu-id="aef03-226">Requirement</span></span> | <span data-ttu-id="aef03-227">值</span><span class="sxs-lookup"><span data-stu-id="aef03-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aef03-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aef03-228">Minimum supported client</span></span><br/> | <span data-ttu-id="aef03-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aef03-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aef03-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aef03-230">Minimum supported server</span></span><br/> | <span data-ttu-id="aef03-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aef03-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aef03-232">命名空間</span><span class="sxs-lookup"><span data-stu-id="aef03-232">Namespace</span></span><br/>                | <span data-ttu-id="aef03-233">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aef03-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aef03-234">MOF</span><span class="sxs-lookup"><span data-stu-id="aef03-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef03-235"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="aef03-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef03-236">DLL</span><span class="sxs-lookup"><span data-stu-id="aef03-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef03-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aef03-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef03-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aef03-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef03-239">**CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="aef03-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

