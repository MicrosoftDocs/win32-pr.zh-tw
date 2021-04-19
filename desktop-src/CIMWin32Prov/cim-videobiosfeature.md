---
description: CIM \_ VideoBIOSFeature 類別代表用來設定及存取電腦系統之視訊控制器和顯示器的低層級軟體的功能。
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986254"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="e383e-103">CIM \_ VideoBIOSFeature 類別</span><span class="sxs-lookup"><span data-stu-id="e383e-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="e383e-104">**CIM \_ VideoBIOSFeature** 類別代表用來設定及存取電腦系統之視訊控制器和顯示器的低層級軟體的功能。</span><span class="sxs-lookup"><span data-stu-id="e383e-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e383e-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e383e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e383e-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e383e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e383e-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e383e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e383e-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e383e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e383e-109">語法</span><span class="sxs-lookup"><span data-stu-id="e383e-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="e383e-110">成員</span><span class="sxs-lookup"><span data-stu-id="e383e-110">Members</span></span>

<span data-ttu-id="e383e-111">**CIM \_ VideoBIOSFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e383e-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="e383e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e383e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e383e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e383e-113">Properties</span></span>

<span data-ttu-id="e383e-114">**CIM \_ VideoBIOSFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e383e-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e383e-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="e383e-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e383e-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e383e-119">Short textual description of the object.</span></span>

<span data-ttu-id="e383e-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e383e-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-122">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e383e-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e383e-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-124">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| VIDEO BIOS 特性 \| 001.4 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**。**特性**") </span><span class="sxs-lookup"><span data-stu-id="e383e-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-125">提供 **特性** 陣列中所指出的影片 BIOS 功能詳細描述的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="e383e-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="e383e-126">這個陣列的每個專案都與 **特性** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="e383e-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="e383e-127">**特性**</span><span class="sxs-lookup"><span data-stu-id="e383e-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-128">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e383e-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e383e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-130">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| VIDEO BIOS 特性 \| 001.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**。**CharacteristicDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="e383e-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-131">影片 BIOS 所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="e383e-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="e383e-132">例如，可能會指出支援 VESA 電源管理或影片 BIOS 遮蔽。</span><span class="sxs-lookup"><span data-stu-id="e383e-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="e383e-133">值 3 ( 「未知」 ) 在 CIM 架構中無效，因為它代表 DMI 中不支援任何 BIOS 功能。</span><span class="sxs-lookup"><span data-stu-id="e383e-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="e383e-134">在這種情況下，不應該具現化物件。</span><span class="sxs-lookup"><span data-stu-id="e383e-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e383e-135">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e383e-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e383e-136">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e383e-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e383e-137">**未定義** (3) </span><span class="sxs-lookup"><span data-stu-id="e383e-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="e383e-138">**標準 VIDEO BIOS** (4) </span><span class="sxs-lookup"><span data-stu-id="e383e-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="e383e-139"> (5) **支援 VESA BIOS 擴充** 功能</span><span class="sxs-lookup"><span data-stu-id="e383e-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="e383e-140">**支援的 VESA 電源管理** (6) </span><span class="sxs-lookup"><span data-stu-id="e383e-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="e383e-141">**支援的 VESA 顯示資料通道** (7) </span><span class="sxs-lookup"><span data-stu-id="e383e-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="e383e-142">允許 (8) 的 **影片 BIOS 遮蔽**</span><span class="sxs-lookup"><span data-stu-id="e383e-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="e383e-143"> (9) 的 **影片 BIOS 可升級**</span><span class="sxs-lookup"><span data-stu-id="e383e-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e383e-144">**說明**</span><span class="sxs-lookup"><span data-stu-id="e383e-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-147">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e383e-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-148">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e383e-148">Textual description of the object.</span></span>

<span data-ttu-id="e383e-149">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="e383e-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-153">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**IdentifyingNumber**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="e383e-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-154">產品識別，例如軟體上的序號或硬體晶片上的骰子編號。</span><span class="sxs-lookup"><span data-stu-id="e383e-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="e383e-155">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e383e-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-157">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e383e-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-159">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e383e-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-160">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e383e-160">Date and time the object was installed.</span></span> <span data-ttu-id="e383e-161">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e383e-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e383e-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-163">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e383e-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-166">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e383e-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e383e-167">資料處理系統外部已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e383e-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="e383e-168">此標籤是可唯一識別元素命名空間內容中專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e383e-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="e383e-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="e383e-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-173">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Name**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="e383e-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-174">常用的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="e383e-174">Commonly used product name.</span></span>

<span data-ttu-id="e383e-175">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-176">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e383e-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-179">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e383e-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-180">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e383e-180">Current status of the object.</span></span> <span data-ttu-id="e383e-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e383e-182">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e383e-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e383e-183">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e383e-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e383e-184">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e383e-185">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e383e-186">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e383e-187">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e383e-188">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e383e-189">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e383e-190">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e383e-191">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e383e-192">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e383e-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e383e-193">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e383e-194">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e383e-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e383e-195">**廠商**</span><span class="sxs-lookup"><span data-stu-id="e383e-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-198">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**廠商**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="e383e-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-199">產品供應商的名稱，其對應至「DMTF 解決方案交換標準 (SE) 之 product 物件中的「 **廠商** 」屬性。</span><span class="sxs-lookup"><span data-stu-id="e383e-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="e383e-200">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="e383e-201">**版本**</span><span class="sxs-lookup"><span data-stu-id="e383e-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e383e-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e383e-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e383e-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e383e-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e383e-204">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Version**") 、 [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="e383e-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e383e-205">產品版本資訊，對應至 DMTF SES product 物件中的 **version** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e383e-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="e383e-206">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e383e-207">備註</span><span class="sxs-lookup"><span data-stu-id="e383e-207">Remarks</span></span>

<span data-ttu-id="e383e-208">**Cim \_ VideoBIOSFeature** 類別衍生自 [**cim \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="e383e-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="e383e-209">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e383e-209">WMI does not implement this class.</span></span>

<span data-ttu-id="e383e-210">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e383e-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e383e-211">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e383e-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e383e-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="e383e-212">Requirements</span></span>



| <span data-ttu-id="e383e-213">需求</span><span class="sxs-lookup"><span data-stu-id="e383e-213">Requirement</span></span> | <span data-ttu-id="e383e-214">值</span><span class="sxs-lookup"><span data-stu-id="e383e-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e383e-215">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e383e-215">Minimum supported client</span></span><br/> | <span data-ttu-id="e383e-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e383e-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e383e-217">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e383e-217">Minimum supported server</span></span><br/> | <span data-ttu-id="e383e-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e383e-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e383e-219">命名空間</span><span class="sxs-lookup"><span data-stu-id="e383e-219">Namespace</span></span><br/>                | <span data-ttu-id="e383e-220">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e383e-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e383e-221">MOF</span><span class="sxs-lookup"><span data-stu-id="e383e-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e383e-222"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e383e-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e383e-223">DLL</span><span class="sxs-lookup"><span data-stu-id="e383e-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e383e-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e383e-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e383e-225">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e383e-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e383e-226">**CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="e383e-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

