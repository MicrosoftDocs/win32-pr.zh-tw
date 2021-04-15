---
description: CIM \_ PhysicalLink 類別代表實體元素的纜線。
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: CIM_PhysicalLink 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510664"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="8e70e-103">CIM \_ PhysicalLink 類別</span><span class="sxs-lookup"><span data-stu-id="8e70e-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="8e70e-104">**CIM \_ PhysicalLink** 類別代表實體元素的纜線。</span><span class="sxs-lookup"><span data-stu-id="8e70e-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="8e70e-105">例如，序列或乙太網路纜線和紅外線連結會是子類別 (如果有定義其他屬性或關聯) 或 **CIM \_ PhysicalLink** 的實例。</span><span class="sxs-lookup"><span data-stu-id="8e70e-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="8e70e-106">一般來說，實體套件或網路內的許多實體纜線都不會進行模型化。</span><span class="sxs-lookup"><span data-stu-id="8e70e-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="8e70e-107">不過，當纜線或連結是公司的重要元件或已標記的資產時，就可以使用此類別或其中一個子代類別來具現化物件。</span><span class="sxs-lookup"><span data-stu-id="8e70e-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e70e-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8e70e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e70e-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e70e-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e70e-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8e70e-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8e70e-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e70e-112">語法</span><span class="sxs-lookup"><span data-stu-id="8e70e-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="8e70e-113">成員</span><span class="sxs-lookup"><span data-stu-id="8e70e-113">Members</span></span>

<span data-ttu-id="8e70e-114">**CIM \_ PhysicalLink** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e70e-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="8e70e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8e70e-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e70e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="8e70e-116">Properties</span></span>

<span data-ttu-id="8e70e-117">**CIM \_ PhysicalLink** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e70e-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e70e-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="8e70e-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="8e70e-122">Short textual description of the object.</span></span>

<span data-ttu-id="8e70e-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e70e-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-127">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="8e70e-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-128">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e70e-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8e70e-129">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="8e70e-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8e70e-130">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="8e70e-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-134">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="8e70e-135">Textual description of the object.</span></span>

<span data-ttu-id="8e70e-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e70e-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8e70e-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="8e70e-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-141">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8e70e-141">Date and time the object was installed.</span></span> <span data-ttu-id="8e70e-142">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="8e70e-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8e70e-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-144">**長度**</span><span class="sxs-lookup"><span data-stu-id="8e70e-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-145">資料類型： **real64**</span><span class="sxs-lookup"><span data-stu-id="8e70e-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-147">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「英尺」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-148">實體連結的目前長度（以英尺為限）。</span><span class="sxs-lookup"><span data-stu-id="8e70e-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="8e70e-149">針對某些連接（尤其是無線技術），此屬性可能不適用，而且應該保持未初始化。</span><span class="sxs-lookup"><span data-stu-id="8e70e-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-150">**製造商**</span><span class="sxs-lookup"><span data-stu-id="8e70e-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-153">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="8e70e-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-154">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="8e70e-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="8e70e-155">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8e70e-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="8e70e-156">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="8e70e-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-158">資料類型： **real64**</span><span class="sxs-lookup"><span data-stu-id="8e70e-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-160">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「英尺」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-161">實體連結的最大長度（以英尺為限）。</span><span class="sxs-lookup"><span data-stu-id="8e70e-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-162">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="8e70e-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e70e-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-165">傳輸信號通過的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="8e70e-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="8e70e-166">一般網路媒體包含雙絞線、同軸電纜和光纖纜線。</span><span class="sxs-lookup"><span data-stu-id="8e70e-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e70e-167">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8e70e-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e70e-168">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8e70e-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="8e70e-169">**Cat1** (2) </span><span class="sxs-lookup"><span data-stu-id="8e70e-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="8e70e-170">**Cat2** (3) </span><span class="sxs-lookup"><span data-stu-id="8e70e-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="8e70e-171">**Cat3** (4) </span><span class="sxs-lookup"><span data-stu-id="8e70e-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="8e70e-172">**Cat4** (5) </span><span class="sxs-lookup"><span data-stu-id="8e70e-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="8e70e-173">**Cat5** (6) </span><span class="sxs-lookup"><span data-stu-id="8e70e-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="8e70e-174">**50-歐姆同軸** (7) </span><span class="sxs-lookup"><span data-stu-id="8e70e-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="8e70e-175">**75-歐姆同軸** (8) </span><span class="sxs-lookup"><span data-stu-id="8e70e-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="8e70e-176">**100-歐姆同軸** (9) </span><span class="sxs-lookup"><span data-stu-id="8e70e-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="8e70e-177">**光纖** (10) </span><span class="sxs-lookup"><span data-stu-id="8e70e-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="8e70e-178">**UTP** (11) </span><span class="sxs-lookup"><span data-stu-id="8e70e-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="8e70e-179">**STP** (12) </span><span class="sxs-lookup"><span data-stu-id="8e70e-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="8e70e-180">**功能區纜線** (13) </span><span class="sxs-lookup"><span data-stu-id="8e70e-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="8e70e-181">**Twinaxial** (14) </span><span class="sxs-lookup"><span data-stu-id="8e70e-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="8e70e-182">**光學 9um** (15) </span><span class="sxs-lookup"><span data-stu-id="8e70e-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="8e70e-183">**光學 50um** (16) </span><span class="sxs-lookup"><span data-stu-id="8e70e-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="8e70e-184">**光學 62.5 um** (17) </span><span class="sxs-lookup"><span data-stu-id="8e70e-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e70e-185">**型號**</span><span class="sxs-lookup"><span data-stu-id="8e70e-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-188">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8e70e-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-189">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e70e-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="8e70e-190">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-191">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8e70e-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-194">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-195">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="8e70e-195">Label by which the object is known.</span></span> <span data-ttu-id="8e70e-196">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="8e70e-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8e70e-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8e70e-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-201">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="8e70e-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="8e70e-202">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="8e70e-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="8e70e-203">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="8e70e-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="8e70e-204">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-205">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="8e70e-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-208">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="8e70e-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-209">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="8e70e-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="8e70e-210">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-211">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="8e70e-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-212">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e70e-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-214">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="8e70e-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="8e70e-215">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-216">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8e70e-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-219">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8e70e-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-220">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="8e70e-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="8e70e-221">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-222">**SKU**</span><span class="sxs-lookup"><span data-stu-id="8e70e-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-225">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8e70e-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-226">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="8e70e-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="8e70e-227">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-228">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8e70e-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-231">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-232">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8e70e-232">Current status of the object.</span></span>

<span data-ttu-id="8e70e-233">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e70e-234">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="8e70e-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e70e-235">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e70e-236">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e70e-237">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e70e-238">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e70e-239">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e70e-240">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e70e-241">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e70e-242">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e70e-243">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e70e-244">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e70e-245">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e70e-246">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="8e70e-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e70e-247">**Tag**</span><span class="sxs-lookup"><span data-stu-id="8e70e-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-250">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="8e70e-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-251">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="8e70e-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="8e70e-252">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="8e70e-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="8e70e-253">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="8e70e-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="8e70e-254">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="8e70e-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="8e70e-255">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="8e70e-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="8e70e-256">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="8e70e-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="8e70e-257">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-258">**版本**</span><span class="sxs-lookup"><span data-stu-id="8e70e-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-259">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e70e-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-261">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8e70e-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-262">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="8e70e-262">Version of the physical element.</span></span>

<span data-ttu-id="8e70e-263">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e70e-264">**有線**</span><span class="sxs-lookup"><span data-stu-id="8e70e-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e70e-265">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e70e-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e70e-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e70e-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e70e-267">若 **為 TRUE**，則實體連結為纜線。</span><span class="sxs-lookup"><span data-stu-id="8e70e-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="8e70e-268">否則，它是無線連接。</span><span class="sxs-lookup"><span data-stu-id="8e70e-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e70e-269">備註</span><span class="sxs-lookup"><span data-stu-id="8e70e-269">Remarks</span></span>

<span data-ttu-id="8e70e-270">**Cim \_ PhysicalLink** 類別衍生自 [**cim \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e70e-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="8e70e-271">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="8e70e-271">WMI does not implement this class.</span></span>

<span data-ttu-id="8e70e-272">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8e70e-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e70e-273">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8e70e-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e70e-274">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e70e-274">Requirements</span></span>



| <span data-ttu-id="8e70e-275">需求</span><span class="sxs-lookup"><span data-stu-id="8e70e-275">Requirement</span></span> | <span data-ttu-id="8e70e-276">值</span><span class="sxs-lookup"><span data-stu-id="8e70e-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e70e-277">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e70e-277">Minimum supported client</span></span><br/> | <span data-ttu-id="8e70e-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e70e-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e70e-279">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e70e-279">Minimum supported server</span></span><br/> | <span data-ttu-id="8e70e-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e70e-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e70e-281">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e70e-281">Namespace</span></span><br/>                | <span data-ttu-id="8e70e-282">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e70e-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e70e-283">MOF</span><span class="sxs-lookup"><span data-stu-id="8e70e-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e70e-284"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e70e-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e70e-285">DLL</span><span class="sxs-lookup"><span data-stu-id="8e70e-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e70e-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e70e-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e70e-287">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e70e-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e70e-288">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="8e70e-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

