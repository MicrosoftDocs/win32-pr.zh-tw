---
description: CIM \_ VideoBIOSElement 類別代表載入至非暫時性存放裝置的低層級軟體，可用來設定及存取電腦系統的視訊控制器和顯示器。
ms.assetid: f23d411f-4781-4727-abd1-61fe1a366bf0
ms.tgt_platform: multiple
title: CIM_VideoBIOSElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSElement
- CIM_VideoBIOSElement.BuildNumber
- CIM_VideoBIOSElement.Caption
- CIM_VideoBIOSElement.CodeSet
- CIM_VideoBIOSElement.Description
- CIM_VideoBIOSElement.IdentificationCode
- CIM_VideoBIOSElement.InstallDate
- CIM_VideoBIOSElement.IsShadowed
- CIM_VideoBIOSElement.LanguageEdition
- CIM_VideoBIOSElement.Manufacturer
- CIM_VideoBIOSElement.Name
- CIM_VideoBIOSElement.OtherTargetOS
- CIM_VideoBIOSElement.SerialNumber
- CIM_VideoBIOSElement.SoftwareElementID
- CIM_VideoBIOSElement.SoftwareElementState
- CIM_VideoBIOSElement.Status
- CIM_VideoBIOSElement.TargetOperatingSystem
- CIM_VideoBIOSElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d873b17f0bf0ea123d988d281c0cab728dd50f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936246"
---
# <a name="cim_videobioselement-class"></a><span data-ttu-id="0020a-103">CIM \_ VideoBIOSElement 類別</span><span class="sxs-lookup"><span data-stu-id="0020a-103">CIM\_VideoBIOSElement class</span></span>

<span data-ttu-id="0020a-104">**CIM \_ VideoBIOSElement** 類別代表載入至非暫時性存放裝置的低層級軟體，可用來設定及存取電腦系統的視訊控制器和顯示器。</span><span class="sxs-lookup"><span data-stu-id="0020a-104">The **CIM\_VideoBIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0020a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0020a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0020a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0020a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0020a-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0020a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0020a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0020a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0020a-109">語法</span><span class="sxs-lookup"><span data-stu-id="0020a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{76148BF6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VideoBIOSElement : CIM_SoftwareElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  boolean  IsShadowed;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="0020a-110">成員</span><span class="sxs-lookup"><span data-stu-id="0020a-110">Members</span></span>

<span data-ttu-id="0020a-111">**CIM \_ VideoBIOSElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0020a-111">The **CIM\_VideoBIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="0020a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0020a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0020a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0020a-113">Properties</span></span>

<span data-ttu-id="0020a-114">**CIM \_ VideoBIOSElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0020a-114">The **CIM\_VideoBIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0020a-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="0020a-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-118">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.4 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-119">此軟體專案之編譯的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="0020a-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="0020a-120">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="0020a-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-124">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0020a-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-125">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0020a-125">Short textual description of the object.</span></span>

<span data-ttu-id="0020a-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-127">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="0020a-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-130">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0020a-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0020a-131">Software 元素所使用的程式碼集。</span><span class="sxs-lookup"><span data-stu-id="0020a-131">Code set used by the software element.</span></span>

<span data-ttu-id="0020a-132">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-133">**說明**</span><span class="sxs-lookup"><span data-stu-id="0020a-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-136">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0020a-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-137">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0020a-137">Textual description of the object.</span></span>

<span data-ttu-id="0020a-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="0020a-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-142">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.7 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-143">軟體元素的製造商識別碼，例如庫存單位 (SKU) 或元件編號。</span><span class="sxs-lookup"><span data-stu-id="0020a-143">Manufacturer's identifier for the software element, such as a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="0020a-144">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0020a-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0020a-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-149">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0020a-149">Date and time the object was installed.</span></span> <span data-ttu-id="0020a-150">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="0020a-150">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0020a-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-152">**IsShadowed**</span><span class="sxs-lookup"><span data-stu-id="0020a-152">**IsShadowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-153">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0020a-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-155">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| VIDEO BIOS \| 001.5」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-156">若 **為 TRUE**，則會將影片 BIOS 遮蔽。</span><span class="sxs-lookup"><span data-stu-id="0020a-156">If **TRUE**, the video BIOS is shadowed.</span></span>

</dd> <dt>

<span data-ttu-id="0020a-157">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="0020a-157">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-160">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.6 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-160">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-161">Software 元素的語言版本。</span><span class="sxs-lookup"><span data-stu-id="0020a-161">Language edition of the software element.</span></span> <span data-ttu-id="0020a-162">應使用 ISO 639 中定義的語言代碼。</span><span class="sxs-lookup"><span data-stu-id="0020a-162">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="0020a-163">當 software 專案代表多語系或國際版的產品時，應該使用「多語系」字串。</span><span class="sxs-lookup"><span data-stu-id="0020a-163">When the software element represents a multilingual or international version of a product, the string "Multilingual" should be used.</span></span>

<span data-ttu-id="0020a-164">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-164">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-165">**製造商**</span><span class="sxs-lookup"><span data-stu-id="0020a-165">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-168">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-168">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-169">Software 專案的製造商：此屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-169">Manufacturer of the software element This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-170">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0020a-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-173">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0020a-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0020a-174">用來識別軟體專案的名稱。此屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-174">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-175">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="0020a-175">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-178">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OtherTypeDescription**") </span><span class="sxs-lookup"><span data-stu-id="0020a-178">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-179">當 **TargetOperatingSystem** 屬性的值為 1 ( "Other" ) 時，軟體專案的製造商和作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="0020a-179">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="0020a-180">當 **TargetOperatingSystem** 屬性的值為1時，這個屬性必須具有非 null 值。</span><span class="sxs-lookup"><span data-stu-id="0020a-180">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="0020a-181">若為所有其他 **TargetOperatingSystem** 值，則此屬性為 null。</span><span class="sxs-lookup"><span data-stu-id="0020a-181">For all other **TargetOperatingSystem** values, this property is null.</span></span> <span data-ttu-id="0020a-182">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-182">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0020a-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-186">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-186">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-187">軟體元素的已指派序號。</span><span class="sxs-lookup"><span data-stu-id="0020a-187">Assigned serial number of the software element.</span></span>

<span data-ttu-id="0020a-188">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-188">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-189">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="0020a-189">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-192">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0020a-192">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0020a-193">設計用來與其他金鑰搭配使用的 software 專案的識別碼，以建立 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 類別的唯一標記法。</span><span class="sxs-lookup"><span data-stu-id="0020a-193">Identifier for the software element that is designed to be used in conjunction with other keys to create a unique representation of the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

<span data-ttu-id="0020a-194">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-194">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0020a-195">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="0020a-195">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0020a-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-198">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0020a-198">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0020a-199">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="0020a-199">State of a software element.</span></span>

<span data-ttu-id="0020a-200">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-200">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="0020a-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0020a-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-202">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="0020a-202">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="0020a-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="0020a-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-204">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="0020a-204">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="0020a-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="0020a-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-206">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="0020a-206">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="0020a-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="0020a-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-208">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0020a-208">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0020a-209">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0020a-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-212">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0020a-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-213">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0020a-213">Current status of the object.</span></span> <span data-ttu-id="0020a-214">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0020a-215">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0020a-215">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0020a-216">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0020a-216">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0020a-217">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-217">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0020a-218">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-218">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0020a-219">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-219">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0020a-220">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-220">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0020a-221">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-221">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0020a-222">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-222">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0020a-223">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-223">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0020a-224">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-224">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0020a-225">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0020a-225">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0020a-226">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-226">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0020a-227">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0020a-227">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0020a-228">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="0020a-228">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-229">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0020a-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-231">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Component Information \| 002.5 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OSType**") </span><span class="sxs-lookup"><span data-stu-id="0020a-231">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-232">作業系統環境。</span><span class="sxs-lookup"><span data-stu-id="0020a-232">Operating system environment.</span></span> <span data-ttu-id="0020a-233">這個屬性的值不能確保二進位執行。</span><span class="sxs-lookup"><span data-stu-id="0020a-233">The value of this property does not ensure binary execution.</span></span> <span data-ttu-id="0020a-234">您必須使用作業系統版本檢查來指定作業系統的版本。</span><span class="sxs-lookup"><span data-stu-id="0020a-234">The version of the operating system must be specified using the operating system version check.</span></span> <span data-ttu-id="0020a-235">此外，也必須是作業系統執行所在的架構。</span><span class="sxs-lookup"><span data-stu-id="0020a-235">Also required is the architecture on which the operating system runs.</span></span> <span data-ttu-id="0020a-236">這些結構的組合可讓提供者清楚地識別特定軟體元素所需的作業系統層級。</span><span class="sxs-lookup"><span data-stu-id="0020a-236">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="0020a-237">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-237">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0020a-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0020a-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0020a-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0020a-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="0020a-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="0020a-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-241">Mac OS</span><span class="sxs-lookup"><span data-stu-id="0020a-241">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="0020a-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="0020a-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-243">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="0020a-243">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="0020a-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="0020a-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="0020a-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="0020a-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="0020a-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="0020a-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="0020a-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="0020a-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-248">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="0020a-248">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="0020a-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="0020a-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-250">HP-UX</span><span class="sxs-lookup"><span data-stu-id="0020a-250">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="0020a-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="0020a-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="0020a-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="0020a-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="0020a-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="0020a-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="0020a-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="0020a-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="0020a-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="0020a-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-256">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="0020a-256">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="0020a-257"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="0020a-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="0020a-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="0020a-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-259">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="0020a-259">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="0020a-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="0020a-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-261">Windows 95</span><span class="sxs-lookup"><span data-stu-id="0020a-261">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="0020a-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="0020a-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-263">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0020a-263">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="0020a-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="0020a-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-265">Windows NT</span><span class="sxs-lookup"><span data-stu-id="0020a-265">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="0020a-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="0020a-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-267">Windows CE</span><span class="sxs-lookup"><span data-stu-id="0020a-267">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="0020a-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="0020a-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-269">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="0020a-269">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="0020a-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="0020a-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="0020a-271"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="0020a-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="0020a-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="0020a-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="0020a-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="0020a-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="0020a-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="0020a-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="0020a-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="0020a-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="0020a-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="0020a-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="0020a-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="0020a-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="0020a-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="0020a-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="0020a-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="0020a-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="0020a-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="0020a-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="0020a-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="0020a-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-282">系列</span><span class="sxs-lookup"><span data-stu-id="0020a-282">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="0020a-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="0020a-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-284">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="0020a-284">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="0020a-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="0020a-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-286">將 NT</span><span class="sxs-lookup"><span data-stu-id="0020a-286">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="0020a-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="0020a-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-288">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="0020a-288">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="0020a-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="0020a-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="0020a-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="0020a-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="0020a-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="0020a-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="0020a-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="0020a-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="0020a-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="0020a-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="0020a-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="0020a-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-295">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="0020a-295">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="0020a-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="0020a-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="0020a-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="0020a-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="0020a-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="0020a-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="0020a-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="0020a-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-300">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="0020a-300">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="0020a-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="0020a-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="0020a-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="0020a-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="0020a-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="0020a-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="0020a-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="0020a-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="0020a-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="0020a-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="0020a-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="0020a-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="0020a-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="0020a-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="0020a-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="0020a-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="0020a-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="0020a-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="0020a-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="0020a-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="0020a-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="0020a-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="0020a-312">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="0020a-312">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="0020a-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="0020a-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="0020a-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="0020a-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="0020a-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="0020a-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="0020a-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="0020a-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="0020a-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="0020a-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0020a-318">**版本**</span><span class="sxs-lookup"><span data-stu-id="0020a-318">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0020a-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0020a-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0020a-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0020a-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0020a-321">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="0020a-321">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0020a-322">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="0020a-322">Version of the operation.</span></span>

<span data-ttu-id="0020a-323">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="0020a-323">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="0020a-324"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="0020a-324"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="0020a-325"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="0020a-325"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="0020a-326">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="0020a-326">This property is inherited from the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0020a-327">備註</span><span class="sxs-lookup"><span data-stu-id="0020a-327">Remarks</span></span>

<span data-ttu-id="0020a-328">**Cim \_ VideoBIOSElement** 類別衍生自 [**cim \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0020a-328">The **CIM\_VideoBIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="0020a-329">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0020a-329">WMI does not implement this class.</span></span>

<span data-ttu-id="0020a-330">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0020a-330">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0020a-331">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0020a-331">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0020a-332">規格需求</span><span class="sxs-lookup"><span data-stu-id="0020a-332">Requirements</span></span>



| <span data-ttu-id="0020a-333">需求</span><span class="sxs-lookup"><span data-stu-id="0020a-333">Requirement</span></span> | <span data-ttu-id="0020a-334">值</span><span class="sxs-lookup"><span data-stu-id="0020a-334">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0020a-335">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0020a-335">Minimum supported client</span></span><br/> | <span data-ttu-id="0020a-336">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0020a-336">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0020a-337">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0020a-337">Minimum supported server</span></span><br/> | <span data-ttu-id="0020a-338">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0020a-338">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0020a-339">命名空間</span><span class="sxs-lookup"><span data-stu-id="0020a-339">Namespace</span></span><br/>                | <span data-ttu-id="0020a-340">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0020a-340">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0020a-341">MOF</span><span class="sxs-lookup"><span data-stu-id="0020a-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0020a-342"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0020a-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0020a-343">DLL</span><span class="sxs-lookup"><span data-stu-id="0020a-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0020a-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0020a-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0020a-345">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0020a-345">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0020a-346">**CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="0020a-346">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

