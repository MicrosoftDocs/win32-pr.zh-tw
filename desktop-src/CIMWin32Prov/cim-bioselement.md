---
description: CIM \_ BIOSElement 類別代表載入至非暫時性儲存區中，用來啟動和設定電腦系統的低層級軟體。
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: 'CIM_BIOSElement 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025964"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="b5a74-103">CIM_BIOSElement 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="b5a74-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b5a74-104">**CIM \_ BIOSElement** 類別代表載入至非暫時性儲存區中，用來啟動和設定電腦系統的低層級軟體。</span><span class="sxs-lookup"><span data-stu-id="b5a74-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5a74-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b5a74-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5a74-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5a74-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b5a74-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b5a74-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b5a74-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a74-109">語法</span><span class="sxs-lookup"><span data-stu-id="b5a74-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="b5a74-110">成員</span><span class="sxs-lookup"><span data-stu-id="b5a74-110">Members</span></span>

<span data-ttu-id="b5a74-111">**CIM \_ BIOSElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5a74-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="b5a74-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b5a74-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5a74-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b5a74-113">Properties</span></span>

<span data-ttu-id="b5a74-114">**CIM \_ BIOSElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b5a74-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5a74-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="b5a74-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-118">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.4 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-119">此軟體專案之編譯的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5a74-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="b5a74-120">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="b5a74-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-124">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-125">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="b5a74-125">A short textual description of the object.</span></span>

<span data-ttu-id="b5a74-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-127">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="b5a74-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-130">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b5a74-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-131">Software 元素所使用的程式碼集。</span><span class="sxs-lookup"><span data-stu-id="b5a74-131">Code set used by the software element.</span></span>

<span data-ttu-id="b5a74-132">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-133">**說明**</span><span class="sxs-lookup"><span data-stu-id="b5a74-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-136">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-137">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="b5a74-137">A textual description of the object.</span></span>

<span data-ttu-id="b5a74-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="b5a74-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-142">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.7 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-143">製造商的軟體專案識別碼，通常是庫存單位 (SKU) 或元件編號。</span><span class="sxs-lookup"><span data-stu-id="b5a74-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="b5a74-144">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b5a74-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b5a74-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-149">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="b5a74-149">Indicates when the object was installed.</span></span> <span data-ttu-id="b5a74-150">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="b5a74-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b5a74-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="b5a74-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-155">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.6 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-156">Software 元素的語言版本。</span><span class="sxs-lookup"><span data-stu-id="b5a74-156">Language edition of the software element.</span></span> <span data-ttu-id="b5a74-157">應使用 ISO 639 中定義的語言代碼。</span><span class="sxs-lookup"><span data-stu-id="b5a74-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="b5a74-158">其中 software 元素代表產品的多語系或國際版本，因此應該使用「多語系」字串。</span><span class="sxs-lookup"><span data-stu-id="b5a74-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="b5a74-159">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-160">**製造商**</span><span class="sxs-lookup"><span data-stu-id="b5a74-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-163">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-164">BIOS 的製造商。</span><span class="sxs-lookup"><span data-stu-id="b5a74-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-165">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b5a74-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-168">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b5a74-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-169">用來識別此軟體元素的名稱</span><span class="sxs-lookup"><span data-stu-id="b5a74-169">The name used to identify this software element</span></span>

<span data-ttu-id="b5a74-170">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-171">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="b5a74-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-174">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OtherTypeDescription**") </span><span class="sxs-lookup"><span data-stu-id="b5a74-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-175">當 **TargetOperatingSystem** 屬性的值為 1 ( "Other" ) 時，軟體專案的製造商和作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="b5a74-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="b5a74-176">當 **TargetOperatingSystem** 屬性的值為1時，這個屬性必須具有非 null 值。</span><span class="sxs-lookup"><span data-stu-id="b5a74-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="b5a74-177">若為所有其他 **TargetOperatingSystem** 值，則此屬性為 null。</span><span class="sxs-lookup"><span data-stu-id="b5a74-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="b5a74-178">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-179">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="b5a74-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b5a74-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-182">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-183">若 **為 TRUE**，則這是電腦系統的主要 BIOS。</span><span class="sxs-lookup"><span data-stu-id="b5a74-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-184">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b5a74-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-187">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-188">軟體元素的序號。</span><span class="sxs-lookup"><span data-stu-id="b5a74-188">Serial number of the software element.</span></span>

<span data-ttu-id="b5a74-189">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-190">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="b5a74-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-193">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b5a74-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-194">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5a74-194">Identifier for the software element.</span></span> <span data-ttu-id="b5a74-195">它是設計來與其他金鑰搭配使用，以建立這個 [**CIM \_ SoftwareElement**](cim-softwareelement.md)的唯一標記法。</span><span class="sxs-lookup"><span data-stu-id="b5a74-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="b5a74-196">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a74-197">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="b5a74-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b5a74-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-200">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5a74-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-201">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="b5a74-201">State of a software element.</span></span>

<span data-ttu-id="b5a74-202">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="b5a74-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b5a74-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-204">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="b5a74-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="b5a74-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="b5a74-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-206">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="b5a74-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="b5a74-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="b5a74-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-208">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="b5a74-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="b5a74-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="b5a74-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-210">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b5a74-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b5a74-211">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b5a74-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-214">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-215">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="b5a74-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="b5a74-216">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="b5a74-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b5a74-217">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="b5a74-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b5a74-218">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="b5a74-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b5a74-219">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="b5a74-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b5a74-220">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="b5a74-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b5a74-221">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="b5a74-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b5a74-222">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b5a74-223">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b5a74-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b5a74-224">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b5a74-225">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b5a74-226">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5a74-227">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b5a74-228">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b5a74-229">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b5a74-230">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b5a74-231">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b5a74-232">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b5a74-233">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b5a74-234">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b5a74-235">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="b5a74-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5a74-236">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="b5a74-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b5a74-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-239">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Component Information \| 002.5 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OSType**") </span><span class="sxs-lookup"><span data-stu-id="b5a74-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-240">作業系統環境。</span><span class="sxs-lookup"><span data-stu-id="b5a74-240">Operating system environment.</span></span> <span data-ttu-id="b5a74-241">這個屬性的值不能確保二進位 executability，需要更多資訊。</span><span class="sxs-lookup"><span data-stu-id="b5a74-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="b5a74-242">作業系統版本必須使用作業系統版本檢查來指定。</span><span class="sxs-lookup"><span data-stu-id="b5a74-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="b5a74-243">此外，也需要作業系統執行所在的架構。</span><span class="sxs-lookup"><span data-stu-id="b5a74-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="b5a74-244">這些結構的組合可讓提供者清楚地識別特定軟體元素所需的作業系統層級。</span><span class="sxs-lookup"><span data-stu-id="b5a74-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="b5a74-245">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5a74-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b5a74-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b5a74-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b5a74-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="b5a74-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="b5a74-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-249">Mac OS</span><span class="sxs-lookup"><span data-stu-id="b5a74-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="b5a74-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="b5a74-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-251">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="b5a74-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="b5a74-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="b5a74-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="b5a74-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="b5a74-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="b5a74-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="b5a74-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="b5a74-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="b5a74-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-256">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="b5a74-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="b5a74-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="b5a74-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="b5a74-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="b5a74-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="b5a74-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="b5a74-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="b5a74-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="b5a74-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="b5a74-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="b5a74-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="b5a74-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="b5a74-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="b5a74-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-264">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="b5a74-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="b5a74-265"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="b5a74-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="b5a74-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="b5a74-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-267">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="b5a74-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="b5a74-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="b5a74-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="b5a74-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="b5a74-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="b5a74-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b5a74-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="b5a74-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="b5a74-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="b5a74-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="b5a74-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="b5a74-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="b5a74-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="b5a74-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="b5a74-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-277">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="b5a74-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="b5a74-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="b5a74-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="b5a74-279"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="b5a74-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="b5a74-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="b5a74-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="b5a74-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="b5a74-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="b5a74-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="b5a74-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="b5a74-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="b5a74-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="b5a74-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="b5a74-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="b5a74-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="b5a74-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="b5a74-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="b5a74-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="b5a74-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="b5a74-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="b5a74-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="b5a74-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="b5a74-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="b5a74-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-290">系列</span><span class="sxs-lookup"><span data-stu-id="b5a74-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="b5a74-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="b5a74-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-292">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="b5a74-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="b5a74-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="b5a74-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-294">將 NT</span><span class="sxs-lookup"><span data-stu-id="b5a74-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="b5a74-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="b5a74-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="b5a74-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="b5a74-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="b5a74-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="b5a74-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="b5a74-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="b5a74-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="b5a74-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="b5a74-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="b5a74-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="b5a74-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="b5a74-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="b5a74-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="b5a74-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-303">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="b5a74-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="b5a74-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="b5a74-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="b5a74-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="b5a74-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="b5a74-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="b5a74-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="b5a74-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="b5a74-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="b5a74-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="b5a74-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="b5a74-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="b5a74-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="b5a74-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="b5a74-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="b5a74-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="b5a74-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="b5a74-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="b5a74-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="b5a74-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="b5a74-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="b5a74-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="b5a74-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="b5a74-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="b5a74-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="b5a74-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="b5a74-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="b5a74-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="b5a74-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="b5a74-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="b5a74-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="b5a74-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="b5a74-320">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="b5a74-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="b5a74-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="b5a74-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="b5a74-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="b5a74-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="b5a74-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="b5a74-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="b5a74-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="b5a74-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="b5a74-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="b5a74-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5a74-326">**版本**</span><span class="sxs-lookup"><span data-stu-id="b5a74-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a74-327">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b5a74-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a74-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a74-329">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="b5a74-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b5a74-330">BIOS 的版本。</span><span class="sxs-lookup"><span data-stu-id="b5a74-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5a74-331">備註</span><span class="sxs-lookup"><span data-stu-id="b5a74-331">Remarks</span></span>

<span data-ttu-id="b5a74-332">**Cim \_ BIOSElement** 類別衍生自 [**cim \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="b5a74-333">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b5a74-333">WMI does not implement this class.</span></span> <span data-ttu-id="b5a74-334">如需衍生自 **CIM \_ BIOSElement** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b5a74-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b5a74-335">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b5a74-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5a74-336">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b5a74-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a74-337">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5a74-337">Requirements</span></span>



| <span data-ttu-id="b5a74-338">需求</span><span class="sxs-lookup"><span data-stu-id="b5a74-338">Requirement</span></span> | <span data-ttu-id="b5a74-339">值</span><span class="sxs-lookup"><span data-stu-id="b5a74-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a74-340">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5a74-340">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a74-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5a74-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5a74-342">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5a74-342">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a74-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5a74-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5a74-344">命名空間</span><span class="sxs-lookup"><span data-stu-id="b5a74-344">Namespace</span></span><br/>                | <span data-ttu-id="b5a74-345">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b5a74-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5a74-346">MOF</span><span class="sxs-lookup"><span data-stu-id="b5a74-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5a74-347"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5a74-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5a74-348">DLL</span><span class="sxs-lookup"><span data-stu-id="b5a74-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a74-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5a74-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a74-350">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5a74-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a74-351">**CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="b5a74-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

