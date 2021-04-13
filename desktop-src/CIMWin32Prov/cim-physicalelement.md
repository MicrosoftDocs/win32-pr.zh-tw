---
description: CIM \_ PhysicalElement 子類別會定義具有不同實體身分識別之系統的任何元件。 可以實體附加至物件的標籤可以定義這個類別的實例。
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: CIM_PhysicalElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510441"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="53021-104">CIM \_ PhysicalElement 類別</span><span class="sxs-lookup"><span data-stu-id="53021-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="53021-105">**CIM \_ PhysicalElement** 子類別會定義具有不同實體身分識別之系統的任何元件。</span><span class="sxs-lookup"><span data-stu-id="53021-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="53021-106">可以實體附加至物件的標籤可以定義這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="53021-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="53021-107">所有的處理常式、檔案和邏輯裝置都不會被視為實體元素。</span><span class="sxs-lookup"><span data-stu-id="53021-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="53021-108">例如，無法將標籤附加至數據機;您只能將標籤附加到可執行數據機的卡片上。</span><span class="sxs-lookup"><span data-stu-id="53021-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="53021-109">相同的卡片也可以執行局域網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="53021-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="53021-110">有形的受管理系統元素 (通常) 的硬體專案具有實體的表現。</span><span class="sxs-lookup"><span data-stu-id="53021-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="53021-111">受管理的系統元素不一定是離散元件。</span><span class="sxs-lookup"><span data-stu-id="53021-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="53021-112">例如，單一卡片 (一種實體元素類型，) 裝載多個邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="53021-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="53021-113">卡片會以與多個邏輯裝置相關聯的單一實體元素表示。</span><span class="sxs-lookup"><span data-stu-id="53021-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53021-114">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="53021-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="53021-115">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="53021-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="53021-116">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="53021-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="53021-117">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="53021-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53021-118">語法</span><span class="sxs-lookup"><span data-stu-id="53021-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
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
};
```

## <a name="members"></a><span data-ttu-id="53021-119">成員</span><span class="sxs-lookup"><span data-stu-id="53021-119">Members</span></span>

<span data-ttu-id="53021-120">**CIM \_ PhysicalElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="53021-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="53021-121">屬性</span><span class="sxs-lookup"><span data-stu-id="53021-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53021-122">屬性</span><span class="sxs-lookup"><span data-stu-id="53021-122">Properties</span></span>

<span data-ttu-id="53021-123">**CIM \_ PhysicalElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="53021-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53021-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="53021-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="53021-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="53021-128">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="53021-128">A short textual description of the object.</span></span>

<span data-ttu-id="53021-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="53021-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53021-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="53021-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-133">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53021-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53021-134">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="53021-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="53021-135">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="53021-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="53021-136">**說明**</span><span class="sxs-lookup"><span data-stu-id="53021-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-139">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="53021-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="53021-140">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="53021-140">A textual description of the object.</span></span>

<span data-ttu-id="53021-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="53021-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53021-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="53021-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-143">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="53021-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="53021-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-145">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="53021-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="53021-146">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="53021-146">Indicates when the object was installed.</span></span> <span data-ttu-id="53021-147">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="53021-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="53021-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="53021-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53021-149">**製造商**</span><span class="sxs-lookup"><span data-stu-id="53021-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-152">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53021-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53021-153">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="53021-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="53021-154">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="53021-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="53021-155">**型號**</span><span class="sxs-lookup"><span data-stu-id="53021-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-158">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="53021-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53021-159">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="53021-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="53021-160">**名稱**</span><span class="sxs-lookup"><span data-stu-id="53021-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-163">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="53021-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="53021-164">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="53021-164">Label by which the object is known.</span></span> <span data-ttu-id="53021-165">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="53021-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="53021-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="53021-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53021-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="53021-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53021-170">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="53021-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="53021-171">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="53021-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="53021-172">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="53021-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="53021-173">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="53021-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-176">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53021-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53021-177">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="53021-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="53021-178">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="53021-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-179">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="53021-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53021-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53021-181">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="53021-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="53021-182">否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="53021-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="53021-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="53021-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-186">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="53021-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53021-187">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="53021-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="53021-188">**SKU**</span><span class="sxs-lookup"><span data-stu-id="53021-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-191">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="53021-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53021-192">此實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="53021-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="53021-193">**狀態**</span><span class="sxs-lookup"><span data-stu-id="53021-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-196">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="53021-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="53021-197">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="53021-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="53021-198">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="53021-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="53021-199">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="53021-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="53021-200">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="53021-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="53021-201">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="53021-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="53021-202">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="53021-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="53021-203">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="53021-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="53021-204">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="53021-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="53021-205">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="53021-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="53021-206">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="53021-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="53021-207">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="53021-208">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53021-209">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="53021-210">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="53021-211">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="53021-212">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="53021-213">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="53021-214">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="53021-215">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="53021-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="53021-216">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="53021-217">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="53021-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53021-218">**Tag**</span><span class="sxs-lookup"><span data-stu-id="53021-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-221">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53021-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53021-222">可唯一識別實體元素，並作為專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="53021-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="53021-223">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="53021-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="53021-224">在物件階層中， **CIM \_ PhysicalElement** 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="53021-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="53021-225">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="53021-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="53021-226">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="53021-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="53021-227">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="53021-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="53021-228">**版本**</span><span class="sxs-lookup"><span data-stu-id="53021-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53021-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53021-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53021-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53021-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53021-231">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="53021-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53021-232">指出實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="53021-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53021-233">備註</span><span class="sxs-lookup"><span data-stu-id="53021-233">Remarks</span></span>

<span data-ttu-id="53021-234">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="53021-234">WMI does not implement this class.</span></span> <span data-ttu-id="53021-235">針對衍生自 **CIM \_ PHYSICALELEMENT** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="53021-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="53021-236">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="53021-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="53021-237">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="53021-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53021-238">規格需求</span><span class="sxs-lookup"><span data-stu-id="53021-238">Requirements</span></span>



| <span data-ttu-id="53021-239">需求</span><span class="sxs-lookup"><span data-stu-id="53021-239">Requirement</span></span> | <span data-ttu-id="53021-240">值</span><span class="sxs-lookup"><span data-stu-id="53021-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53021-241">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53021-241">Minimum supported client</span></span><br/> | <span data-ttu-id="53021-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53021-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53021-243">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53021-243">Minimum supported server</span></span><br/> | <span data-ttu-id="53021-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53021-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53021-245">命名空間</span><span class="sxs-lookup"><span data-stu-id="53021-245">Namespace</span></span><br/>                | <span data-ttu-id="53021-246">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="53021-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53021-247">MOF</span><span class="sxs-lookup"><span data-stu-id="53021-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53021-248"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="53021-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53021-249">DLL</span><span class="sxs-lookup"><span data-stu-id="53021-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53021-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53021-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53021-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53021-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53021-252">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="53021-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

