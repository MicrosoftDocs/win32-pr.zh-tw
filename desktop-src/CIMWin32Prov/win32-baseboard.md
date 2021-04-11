---
description: 代表基礎板，也稱為主機板或系統面板。
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Win32_BaseBoard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026004"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="b1ecf-103">Win32 基礎板 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="b1ecf-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="b1ecf-104">**\_ Win32** 基礎板 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表一種基礎板，也稱為主機板或系統面板。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="b1ecf-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ecf-106">語法</span><span class="sxs-lookup"><span data-stu-id="b1ecf-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="b1ecf-107">成員</span><span class="sxs-lookup"><span data-stu-id="b1ecf-107">Members</span></span>

<span data-ttu-id="b1ecf-108">**Win32 基礎 \_** 板類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b1ecf-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="b1ecf-109">方法</span><span class="sxs-lookup"><span data-stu-id="b1ecf-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1ecf-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b1ecf-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1ecf-111">方法</span><span class="sxs-lookup"><span data-stu-id="b1ecf-111">Methods</span></span>

<span data-ttu-id="b1ecf-112">**Win32 基礎 \_** 板類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="b1ecf-113">方法</span><span class="sxs-lookup"><span data-stu-id="b1ecf-113">Method</span></span>           | <span data-ttu-id="b1ecf-114">描述</span><span class="sxs-lookup"><span data-stu-id="b1ecf-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="b1ecf-115">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-115">**IsCompatible**</span></span> | <span data-ttu-id="b1ecf-116">未實作。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1ecf-117">屬性</span><span class="sxs-lookup"><span data-stu-id="b1ecf-117">Properties</span></span>

<span data-ttu-id="b1ecf-118">**Win32 基礎 \_** 板類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1ecf-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-123">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b1ecf-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-125">**ConfigOptions**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-126">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b1ecf-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 12 \| Configuration Options Strings" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-129">代表位於基礎板上的跳線和交換器設定的陣列。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="b1ecf-130">範例： ".JP2：1-2 快取大小為256K，2-3 快取大小為512K，SW1-1：關閉以停用面板影片"</span><span class="sxs-lookup"><span data-stu-id="b1ecf-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-134">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-135">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b1ecf-136">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b1ecf-137">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-138">**深度**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-139">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-141">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-142">實體套件的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="b1ecf-143">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-144">**說明**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-147">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-148">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-148">Description of the object.</span></span>

<span data-ttu-id="b1ecf-149">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-150">**高度**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-151">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-153">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-154">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="b1ecf-155">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-156">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-157">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-159">若 **為 TRUE**，則表示卡片是主機板或底座中的基礎板。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="b1ecf-160">這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-161">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-162">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-164">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="b1ecf-165">如果您可以將專案取代為實體不同但對等的元素，而包含的套件已套用電源（也就是開啟時），則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="b1ecf-166">例如，使用 SCA 連接器插入的磁片磁碟機套件會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="b1ecf-167">所有可以熱交換的封裝，本質上都是卸載且可取代的。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="b1ecf-168">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-170">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-172">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="b1ecf-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-173">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-173">Date and time the object was installed.</span></span> <span data-ttu-id="b1ecf-174">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b1ecf-175">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-176">**製造商**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-179">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-180">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="b1ecf-181">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-182">**型號**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-185">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-186">已知實體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="b1ecf-187">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-188">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-191">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-192">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-192">Label by which the object is known.</span></span> <span data-ttu-id="b1ecf-193">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b1ecf-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-198">會捕捉資產標籤資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="b1ecf-199">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="b1ecf-200">請注意，如果只有條碼資料可供使用，而且是唯一的或可作為專案索引鍵，則屬性值會是 **Null** ，而條碼資料會在標記屬性中當做類別機碼使用。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="b1ecf-201">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-202">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-205">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-206">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="b1ecf-207">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-208">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-209">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-211">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="b1ecf-212">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-213">**產品**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-216">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 2 \| Product" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-217">製造商所定義的基礎板零件編號。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-218">**移動**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-221">若 **為 TRUE**，則會卸載套件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="b1ecf-222">如果實體封裝的設計目的是要將它放入和移出實體容器（通常是在不因而影響整體封裝的函式的情況下找到），則會卸載。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="b1ecf-223">如果電源必須關閉才能執行移除，則套件仍可以卸載。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="b1ecf-224">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="b1ecf-225">例如，膝上型電腦中的額外電池會卸載，也就是使用 SCA 連接器插入的磁片磁碟機套件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="b1ecf-226">不過，後者也可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="b1ecf-227">膝上型電腦的顯示器不是可移動的，也不是 nonredundant 電源供應器。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="b1ecf-228">移除這些元件會影響整體封裝的功能，或由於封裝的緊密整合而無法進行。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="b1ecf-229">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-230">**更換**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-233">若 **為 TRUE**，則可替換套件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="b1ecf-234">如果可以更換 (FRU 或升級) 具有實體不同的元素，則可以更換實體套件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="b1ecf-235">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="b1ecf-236">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="b1ecf-237">另一個範例是掛接在滑動滑軌上的電源供應器套件。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="b1ecf-238">所有卸載式套件本質上都是可取代的。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="b1ecf-239">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-240">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-243">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 卡**](cim-card.md)」。**SpecialRequirements**") </span><span class="sxs-lookup"><span data-stu-id="b1ecf-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-244">描述此卡片與其他卡片實際獨特之方式的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="b1ecf-245">當對應的布林值屬性 **SpecialRequirements** 設為 **TRUE** 時，屬性才有意義。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="b1ecf-246">這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-247">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-248">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-250">若 **為 TRUE**，則至少需要一個 daughterboard 或輔助卡才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="b1ecf-251">這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-252">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-255">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-256">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="b1ecf-257">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-258">**SKU**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-259">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-261">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-262">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="b1ecf-263">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-264">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-265">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-267">描述位置位置、一般使用方式、限制、個別位置間距或卡片上任何其他相關資訊的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="b1ecf-268">這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-269">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-270">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-272">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 卡**](cim-card.md)」。**RequirementsDescription**") </span><span class="sxs-lookup"><span data-stu-id="b1ecf-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-273">若 **為 TRUE**，則這張卡片與相同類型的其他卡片實際上是唯一的，因此需要特殊的位置。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="b1ecf-274">例如，雙卡片需要兩個插槽。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="b1ecf-275">另一個範例是，特定卡片可用於與其他卡片相同的一般功能，但需要特殊插槽 (例如，額外的長) ，而其他卡片則可以放置在任何可用的位置。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="b1ecf-276">如果設定為 **TRUE**，則對應的屬性 **RequirementsDescription** 應該指定卡片唯一性或用途的本質。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="b1ecf-277">這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-278">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-281">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-282">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-282">Current status of the object.</span></span> <span data-ttu-id="b1ecf-283">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b1ecf-284">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b1ecf-285">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b1ecf-286">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b1ecf-287">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b1ecf-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b1ecf-289">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b1ecf-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1ecf-290">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1ecf-291">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1ecf-292">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ecf-293">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1ecf-294">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1ecf-295">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1ecf-296">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1ecf-297">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1ecf-298">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1ecf-299">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1ecf-300">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1ecf-301">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ecf-302">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-305">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Tag" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-306">系統基礎板的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="b1ecf-307">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b1ecf-308">範例：「基本板」</span><span class="sxs-lookup"><span data-stu-id="b1ecf-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-309">**版本**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-312">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-313">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-313">Version of the physical element.</span></span>

<span data-ttu-id="b1ecf-314">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-315">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-316">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-318">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-319">實體套件的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="b1ecf-320">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ecf-321">**寬度**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ecf-322">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1ecf-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ecf-324">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="b1ecf-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b1ecf-325">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="b1ecf-326">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1ecf-327">備註</span><span class="sxs-lookup"><span data-stu-id="b1ecf-327">Remarks</span></span>

<span data-ttu-id="b1ecf-328">**Win32 基礎 \_** 板類別衍生自 cim [**\_ 卡**](cim-card.md)，這是從 [**cim \_ PhysicalPackage**](cim-physicalelement.md)衍生的。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b1ecf-329">範例</span><span class="sxs-lookup"><span data-stu-id="b1ecf-329">Examples</span></span>

<span data-ttu-id="b1ecf-330">[列出電腦](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8)基礎板屬性 Perl 範例會傳回電腦基礎板的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="b1ecf-331">[列出電腦](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9)基礎板屬性 PowerShell 範例會傳回電腦基礎板的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="b1ecf-332">下列 VBScript 範例也會傳回電腦基礎板的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b1ecf-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="b1ecf-333">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1ecf-333">Requirements</span></span>



| <span data-ttu-id="b1ecf-334">需求</span><span class="sxs-lookup"><span data-stu-id="b1ecf-334">Requirement</span></span> | <span data-ttu-id="b1ecf-335">值</span><span class="sxs-lookup"><span data-stu-id="b1ecf-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ecf-336">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1ecf-336">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ecf-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1ecf-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1ecf-338">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1ecf-338">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ecf-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1ecf-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1ecf-340">MOF</span><span class="sxs-lookup"><span data-stu-id="b1ecf-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1ecf-341"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1ecf-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1ecf-342">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ecf-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1ecf-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1ecf-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ecf-344">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1ecf-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ecf-345">**CIM \_ 卡片**</span><span class="sxs-lookup"><span data-stu-id="b1ecf-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="b1ecf-346">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="b1ecf-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

