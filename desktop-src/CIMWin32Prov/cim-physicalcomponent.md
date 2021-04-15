---
description: CIM \_ PhysicalComponent 類別代表封裝內的低層級或基本元件。 不是連結、連接器或封裝的實體元素是此類別 (或成員) 的子系。
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: CIM_PhysicalComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468348"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="db173-104">CIM \_ PhysicalComponent 類別</span><span class="sxs-lookup"><span data-stu-id="db173-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="db173-105">**CIM \_ PhysicalComponent** 類別代表封裝內的低層級或基本元件。</span><span class="sxs-lookup"><span data-stu-id="db173-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="db173-106">不是連結、連接器或封裝的實體元素是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="db173-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="db173-107">例如，內接式數據機卡上的 UART 晶片組會是子類別 (如果有定義其他屬性或關聯) 或 **CIM \_ PhysicalComponent** 的實例。</span><span class="sxs-lookup"><span data-stu-id="db173-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db173-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="db173-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="db173-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="db173-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="db173-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="db173-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="db173-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="db173-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="db173-112">語法</span><span class="sxs-lookup"><span data-stu-id="db173-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
};
```

## <a name="members"></a><span data-ttu-id="db173-113">成員</span><span class="sxs-lookup"><span data-stu-id="db173-113">Members</span></span>

<span data-ttu-id="db173-114">**CIM \_ PhysicalComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="db173-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="db173-115">屬性</span><span class="sxs-lookup"><span data-stu-id="db173-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db173-116">屬性</span><span class="sxs-lookup"><span data-stu-id="db173-116">Properties</span></span>

<span data-ttu-id="db173-117">**CIM \_ PhysicalComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="db173-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db173-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="db173-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="db173-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="db173-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="db173-122">A short textual description of the object.</span></span>

<span data-ttu-id="db173-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="db173-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-127">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="db173-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db173-128">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="db173-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="db173-129">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="db173-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="db173-130">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="db173-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-134">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="db173-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="db173-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="db173-135">A textual description of the object.</span></span>

<span data-ttu-id="db173-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-137">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="db173-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="db173-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db173-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db173-140">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="db173-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="db173-141">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="db173-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="db173-142">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="db173-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="db173-143">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="db173-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="db173-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="db173-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-145">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="db173-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="db173-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-147">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="db173-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="db173-148">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="db173-148">Indicates when the object was installed.</span></span> <span data-ttu-id="db173-149">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="db173-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="db173-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-151">**製造商**</span><span class="sxs-lookup"><span data-stu-id="db173-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-154">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="db173-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db173-155">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="db173-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="db173-156">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="db173-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="db173-157">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-158">**型號**</span><span class="sxs-lookup"><span data-stu-id="db173-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-161">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="db173-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="db173-162">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="db173-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="db173-163">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-164">**名稱**</span><span class="sxs-lookup"><span data-stu-id="db173-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-167">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="db173-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="db173-168">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="db173-168">Label by which the object is known.</span></span> <span data-ttu-id="db173-169">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="db173-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="db173-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="db173-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db173-174">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="db173-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="db173-175">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="db173-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="db173-176">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="db173-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="db173-177">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-178">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="db173-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-181">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="db173-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db173-182">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="db173-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="db173-183">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-184">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="db173-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-185">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="db173-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db173-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db173-187">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="db173-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="db173-188">否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="db173-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="db173-189">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-190">**移動**</span><span class="sxs-lookup"><span data-stu-id="db173-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-191">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="db173-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db173-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db173-193">若 **為 TRUE**，則會將這個專案設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="db173-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="db173-194">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="db173-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="db173-195">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="db173-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="db173-196">例如，「可升級處理器」晶片是卸載式的。</span><span class="sxs-lookup"><span data-stu-id="db173-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="db173-197">**更換**</span><span class="sxs-lookup"><span data-stu-id="db173-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-198">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="db173-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db173-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db173-200">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="db173-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="db173-201">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="db173-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="db173-202">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="db173-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="db173-203">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="db173-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="db173-204">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="db173-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-207">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="db173-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="db173-208">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="db173-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="db173-209">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-210">**SKU**</span><span class="sxs-lookup"><span data-stu-id="db173-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-213">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="db173-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="db173-214">此實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="db173-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="db173-215">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-216">**狀態**</span><span class="sxs-lookup"><span data-stu-id="db173-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-219">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="db173-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="db173-220">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="db173-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="db173-221">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="db173-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="db173-222">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="db173-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="db173-223">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="db173-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="db173-224">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="db173-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="db173-225">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="db173-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="db173-226">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="db173-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="db173-227">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="db173-228">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="db173-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="db173-229">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="db173-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="db173-230">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="db173-231">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db173-232">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="db173-233">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="db173-234">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="db173-235">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="db173-236">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="db173-237">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="db173-238">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="db173-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="db173-239">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="db173-240">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="db173-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db173-241">**Tag**</span><span class="sxs-lookup"><span data-stu-id="db173-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-244">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="db173-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db173-245">可唯一識別實體元素，並作為專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="db173-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="db173-246">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="db173-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="db173-247">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="db173-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="db173-248">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="db173-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="db173-249">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="db173-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="db173-250">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="db173-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="db173-251">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db173-252">**版本**</span><span class="sxs-lookup"><span data-stu-id="db173-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db173-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db173-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db173-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db173-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db173-255">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="db173-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="db173-256">指出實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="db173-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="db173-257">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db173-258">備註</span><span class="sxs-lookup"><span data-stu-id="db173-258">Remarks</span></span>

<span data-ttu-id="db173-259">**Cim \_ PhysicalComponent** 類別衍生自 [**cim \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="db173-260">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="db173-260">WMI does not implement this class.</span></span> <span data-ttu-id="db173-261">針對衍生自 **CIM \_ PHYSICALCOMPONENT** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="db173-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="db173-262">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="db173-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="db173-263">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="db173-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="db173-264">規格需求</span><span class="sxs-lookup"><span data-stu-id="db173-264">Requirements</span></span>



| <span data-ttu-id="db173-265">需求</span><span class="sxs-lookup"><span data-stu-id="db173-265">Requirement</span></span> | <span data-ttu-id="db173-266">值</span><span class="sxs-lookup"><span data-stu-id="db173-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db173-267">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db173-267">Minimum supported client</span></span><br/> | <span data-ttu-id="db173-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db173-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db173-269">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db173-269">Minimum supported server</span></span><br/> | <span data-ttu-id="db173-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db173-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db173-271">命名空間</span><span class="sxs-lookup"><span data-stu-id="db173-271">Namespace</span></span><br/>                | <span data-ttu-id="db173-272">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="db173-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db173-273">MOF</span><span class="sxs-lookup"><span data-stu-id="db173-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db173-274"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="db173-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db173-275">DLL</span><span class="sxs-lookup"><span data-stu-id="db173-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db173-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db173-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db173-277">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db173-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db173-278">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="db173-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

