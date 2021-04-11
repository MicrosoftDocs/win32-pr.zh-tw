---
description: Win32 \_ ONBOARDDEVICE WMI 類別代表內建于主機板 (系統面板) 內建的通用介面卡裝置。
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Win32_OnBoardDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191015"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="b050f-103">Win32 \_ OnBoardDevice 類別</span><span class="sxs-lookup"><span data-stu-id="b050f-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="b050f-104">**Win32 \_ OnBoardDevice** [WMI 類別](../wmisdk/retrieving-a-class.md)代表內建于主機板 (系統面板) 內建的通用介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="b050f-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="b050f-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b050f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b050f-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b050f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b050f-107">語法</span><span class="sxs-lookup"><span data-stu-id="b050f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="b050f-108">成員</span><span class="sxs-lookup"><span data-stu-id="b050f-108">Members</span></span>

<span data-ttu-id="b050f-109">**Win32 \_ OnBoardDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b050f-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="b050f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b050f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b050f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b050f-111">Properties</span></span>

<span data-ttu-id="b050f-112">**Win32 \_ OnBoardDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b050f-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b050f-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="b050f-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-117">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="b050f-117">Short description of the object.</span></span>

<span data-ttu-id="b050f-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b050f-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-122">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="b050f-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-123">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="b050f-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b050f-124">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="b050f-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b050f-125">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-126">**說明**</span><span class="sxs-lookup"><span data-stu-id="b050f-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-129">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Description" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 10 \| Description" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-130">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b050f-130">Description of the object.</span></span>

<span data-ttu-id="b050f-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="b050f-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b050f-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-135">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 10 \| Device type n" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-136">所代表的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="b050f-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b050f-137">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b050f-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b050f-138">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b050f-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="b050f-139">**影片** (3) </span><span class="sxs-lookup"><span data-stu-id="b050f-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="b050f-140">**SCSI 控制器** (4) </span><span class="sxs-lookup"><span data-stu-id="b050f-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="b050f-141">**Ethernet** (5) </span><span class="sxs-lookup"><span data-stu-id="b050f-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="b050f-142">**權杖環** (6) </span><span class="sxs-lookup"><span data-stu-id="b050f-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="b050f-143">**音效** (7) </span><span class="sxs-lookup"><span data-stu-id="b050f-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b050f-144">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="b050f-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b050f-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-147">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 10 \| Device Status n" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-148">若為 **TRUE**，則表示可以使用板載裝置。</span><span class="sxs-lookup"><span data-stu-id="b050f-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="b050f-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="b050f-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-150">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b050f-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b050f-152">若為 **TRUE**，則實體封裝可進行熱交換 (如果可以將專案取代為實體不同但對等的專案，但包含的套件已套用電源) 。</span><span class="sxs-lookup"><span data-stu-id="b050f-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="b050f-153">例如，使用 SCA 連接器插入的磁片磁碟機套件會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b050f-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="b050f-154">所有可以熱交換的封裝，本質上都是卸載且可取代的。</span><span class="sxs-lookup"><span data-stu-id="b050f-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="b050f-155">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b050f-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-157">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b050f-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-159">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="b050f-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-160">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b050f-160">Date and time the object was installed.</span></span> <span data-ttu-id="b050f-161">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b050f-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b050f-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-163">**製造商**</span><span class="sxs-lookup"><span data-stu-id="b050f-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-166">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="b050f-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-167">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="b050f-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="b050f-168">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-169">**型號**</span><span class="sxs-lookup"><span data-stu-id="b050f-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-172">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="b050f-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-173">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="b050f-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="b050f-174">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-175">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b050f-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-178">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-179">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b050f-179">Label by which the object is known.</span></span> <span data-ttu-id="b050f-180">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b050f-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b050f-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b050f-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b050f-185">其他資料，除了資產標記資訊之外，還可以用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="b050f-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="b050f-186">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="b050f-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="b050f-187">請注意，如果只有條碼資料可供使用，而且是唯一的或可作為專案索引鍵，則這個屬性會是 **Null** ，而條碼資料會當做標記屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="b050f-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="b050f-188">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-189">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b050f-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-192">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="b050f-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-193">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="b050f-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="b050f-194">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-195">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="b050f-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b050f-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b050f-198">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="b050f-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="b050f-199">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-200">**移動**</span><span class="sxs-lookup"><span data-stu-id="b050f-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-201">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b050f-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b050f-203">若 **為 TRUE**，就會卸載實體封裝 (如果它是設計成要在通常找到它的實體容器中取出，則不會因而影響整體封裝) 的功能。</span><span class="sxs-lookup"><span data-stu-id="b050f-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="b050f-204">如果電源必須是「關閉」以執行移除，則套件仍可以卸載。</span><span class="sxs-lookup"><span data-stu-id="b050f-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="b050f-205">如果可以「開啟」電源，並移除該封裝，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b050f-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="b050f-206">例如，膝上型電腦中的額外電池會卸載，也就是使用 SCA 連接器插入的磁片磁碟機套件。</span><span class="sxs-lookup"><span data-stu-id="b050f-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="b050f-207">不過，後者可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="b050f-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="b050f-208">膝上型電腦的顯示器不是可移動的，也不是 nonredundant 電源供應器。</span><span class="sxs-lookup"><span data-stu-id="b050f-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="b050f-209">移除這些元件會影響整體封裝的功能，或由於封裝的緊密整合而無法進行。</span><span class="sxs-lookup"><span data-stu-id="b050f-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="b050f-210">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-211">**更換**</span><span class="sxs-lookup"><span data-stu-id="b050f-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-212">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b050f-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b050f-214">若為 **TRUE**，實體封裝可以更換 (如果可以更換、FRU 或升級，則為實體不同) 的元素。</span><span class="sxs-lookup"><span data-stu-id="b050f-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="b050f-215">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="b050f-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="b050f-216">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="b050f-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="b050f-217">另一個範例是掛接在滑動滑軌上的電源供應器套件。</span><span class="sxs-lookup"><span data-stu-id="b050f-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="b050f-218">所有卸載式套件本質上都是可取代的。</span><span class="sxs-lookup"><span data-stu-id="b050f-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="b050f-219">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b050f-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-223">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="b050f-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-224">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="b050f-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="b050f-225">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="b050f-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-229">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="b050f-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-230">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="b050f-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="b050f-231">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b050f-232">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b050f-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-235">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-236">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b050f-236">Current status of the object.</span></span> <span data-ttu-id="b050f-237">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="b050f-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b050f-238">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="b050f-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b050f-239">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="b050f-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b050f-240">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="b050f-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b050f-241">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="b050f-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b050f-242">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b050f-243">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b050f-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b050f-244">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b050f-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b050f-245">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b050f-246">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b050f-247">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b050f-248">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b050f-249">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b050f-250">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b050f-251">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b050f-252">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b050f-253">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b050f-254">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b050f-255">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="b050f-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b050f-256">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b050f-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-259">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="b050f-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b050f-260">連線到系統之內部裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b050f-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="b050f-261">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b050f-262">範例：「在面板裝置1」</span><span class="sxs-lookup"><span data-stu-id="b050f-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="b050f-263">**版本**</span><span class="sxs-lookup"><span data-stu-id="b050f-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050f-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b050f-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b050f-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b050f-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050f-266">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="b050f-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b050f-267">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="b050f-267">Version of the physical element.</span></span>

<span data-ttu-id="b050f-268">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b050f-269">備註</span><span class="sxs-lookup"><span data-stu-id="b050f-269">Remarks</span></span>

<span data-ttu-id="b050f-270">**Win32 \_ OnBoardDevice** 類別衍生自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="b050f-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b050f-271">規格需求</span><span class="sxs-lookup"><span data-stu-id="b050f-271">Requirements</span></span>



| <span data-ttu-id="b050f-272">需求</span><span class="sxs-lookup"><span data-stu-id="b050f-272">Requirement</span></span> | <span data-ttu-id="b050f-273">值</span><span class="sxs-lookup"><span data-stu-id="b050f-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b050f-274">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b050f-274">Minimum supported client</span></span><br/> | <span data-ttu-id="b050f-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b050f-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b050f-276">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b050f-276">Minimum supported server</span></span><br/> | <span data-ttu-id="b050f-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b050f-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b050f-278">命名空間</span><span class="sxs-lookup"><span data-stu-id="b050f-278">Namespace</span></span><br/>                | <span data-ttu-id="b050f-279">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b050f-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b050f-280">MOF</span><span class="sxs-lookup"><span data-stu-id="b050f-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b050f-281"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b050f-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b050f-282">DLL</span><span class="sxs-lookup"><span data-stu-id="b050f-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b050f-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b050f-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b050f-284">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b050f-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b050f-285">**CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="b050f-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="b050f-286">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="b050f-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
