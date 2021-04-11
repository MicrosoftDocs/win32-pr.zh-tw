---
description: CIM \_ SoftwareElement 類別會將 cim \_ SoftwareFeature 物件分解至特定平臺的一組個別可管理或可部署的元件中。
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: 'CIM_SoftwareElement 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110816"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="c3cd6-103">CIM_SoftwareElement 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c3cd6-104">**Cim \_ SoftwareElement** 類別會將 [**cim \_ SoftwareFeature**](cim-softwarefeature.md)物件分解至特定平臺的一組個別可管理或可部署的元件中。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="c3cd6-105">軟體專案的平臺是由其基礎硬體架構和作業系統來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="c3cd6-106">因此，若要瞭解如何在特定平臺上提供特定軟體功能的詳細資料，則 [**cim \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)關聯所參考的 **cim \_ SoftwareElement** 物件，會根據 **TargetOperatingSystem** 屬性組織在斷續的集合中。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="c3cd6-107">**CIM \_ SoftwareElement** 物件會以 **SoftwareElementState** 屬性所特性的四種狀態之一來捕捉元件或元件的管理細節。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3cd6-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c3cd6-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c3cd6-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c3cd6-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cd6-112">語法</span><span class="sxs-lookup"><span data-stu-id="c3cd6-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
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

## <a name="members"></a><span data-ttu-id="c3cd6-113">成員</span><span class="sxs-lookup"><span data-stu-id="c3cd6-113">Members</span></span>

<span data-ttu-id="c3cd6-114">**CIM \_ SoftwareElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c3cd6-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c3cd6-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c3cd6-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3cd6-116">屬性</span><span class="sxs-lookup"><span data-stu-id="c3cd6-116">Properties</span></span>

<span data-ttu-id="c3cd6-117">**CIM \_ SoftwareElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3cd6-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-121">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.4 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-122">此軟體專案之編譯的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-123">**標題**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-126">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-127">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-127">Short textual description of the object.</span></span>

<span data-ttu-id="c3cd6-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-129">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-132">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-133">Software 元素所使用的程式碼集。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-134">**說明**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-137">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-138">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-138">Textual description of the object.</span></span>

<span data-ttu-id="c3cd6-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-140">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-143">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.7 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-144">製造商的軟體專案識別碼，通常是庫存單位 (SKU) 或元件編號。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-149">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-149">Date and time the object was installed.</span></span> <span data-ttu-id="c3cd6-150">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c3cd6-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-155">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.6 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-156">Software 元素的語言版本。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-156">Language edition of the software element.</span></span> <span data-ttu-id="c3cd6-157">應使用 ISO 639 中定義的語言代碼。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="c3cd6-158">其中 software 元素代表產品的多語系或國際版本，因此應該使用「多語系」字串。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-159">**製造商**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-162">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-163">軟體元素的製造商。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-164">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-167">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-168">用來識別軟體專案的名稱。此屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-169">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-172">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OtherTypeDescription**") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-173">當 **TargetOperatingSystem** 屬性的值為 1 ( "Other" ) 時，軟體專案的製造商和作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="c3cd6-174">當 **TargetOperatingSystem** 屬性的值為1時，這個屬性必須具有非 null 值。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="c3cd6-175">若為所有其他 **TargetOperatingSystem** 值，則此屬性為 null。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-176">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-179">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-180">軟體元素的序號。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-181">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-184">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-185">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-185">Identifier for the software element.</span></span> <span data-ttu-id="c3cd6-186">它是設計來與其他金鑰搭配使用，以建立這個 **CIM \_ SoftwareElement** 的唯一標記法。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd6-187">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-190">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3cd6-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-191">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="c3cd6-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-193">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="c3cd6-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-195">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="c3cd6-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-197">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c3cd6-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-199">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3cd6-200">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-203">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-204">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-204">Current status of the object.</span></span>

<span data-ttu-id="c3cd6-205">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c3cd6-206">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c3cd6-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c3cd6-207">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c3cd6-208">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c3cd6-209">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3cd6-210">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c3cd6-211">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c3cd6-212">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c3cd6-213">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c3cd6-214">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c3cd6-215">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c3cd6-216">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c3cd6-217">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c3cd6-218">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3cd6-219">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-220">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-222">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Component Information \| 002.5 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OSType**") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-223">作業系統環境。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-223">Operating system environment.</span></span> <span data-ttu-id="c3cd6-224">這個屬性的值不能確保二進位 executability，需要更多資訊。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="c3cd6-225">作業系統版本必須使用作業系統版本檢查來指定。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="c3cd6-226">此外，也需要作業系統執行所在的架構。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="c3cd6-227">這些結構的組合可讓提供者清楚地識別特定軟體元素所需的作業系統層級。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3cd6-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c3cd6-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="c3cd6-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-231">Mac OS</span><span class="sxs-lookup"><span data-stu-id="c3cd6-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="c3cd6-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-233">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="c3cd6-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="c3cd6-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="c3cd6-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="c3cd6-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="c3cd6-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-238">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="c3cd6-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="c3cd6-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="c3cd6-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="c3cd6-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="c3cd6-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="c3cd6-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="c3cd6-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="c3cd6-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-246">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="c3cd6-247"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="c3cd6-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-249">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="c3cd6-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="c3cd6-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="c3cd6-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="c3cd6-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c3cd6-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="c3cd6-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c3cd6-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="c3cd6-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="c3cd6-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="c3cd6-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-259">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="c3cd6-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="c3cd6-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="c3cd6-261"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="c3cd6-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="c3cd6-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="c3cd6-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="c3cd6-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="c3cd6-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="c3cd6-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="c3cd6-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="c3cd6-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="c3cd6-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="c3cd6-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-272">系列</span><span class="sxs-lookup"><span data-stu-id="c3cd6-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="c3cd6-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-274">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="c3cd6-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="c3cd6-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-276">將 NT</span><span class="sxs-lookup"><span data-stu-id="c3cd6-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="c3cd6-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="c3cd6-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="c3cd6-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="c3cd6-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="c3cd6-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="c3cd6-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="c3cd6-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="c3cd6-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-285">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="c3cd6-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="c3cd6-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="c3cd6-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="c3cd6-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="c3cd6-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="c3cd6-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="c3cd6-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="c3cd6-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="c3cd6-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="c3cd6-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="c3cd6-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="c3cd6-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="c3cd6-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="c3cd6-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="c3cd6-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="c3cd6-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="c3cd6-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="c3cd6-302">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="c3cd6-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="c3cd6-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="c3cd6-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="c3cd6-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="c3cd6-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="c3cd6-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="c3cd6-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3cd6-308">**版本**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cd6-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3cd6-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cd6-311">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="c3cd6-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c3cd6-312">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-312">Version of the operation.</span></span>

<span data-ttu-id="c3cd6-313">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="c3cd6-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="c3cd6-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="c3cd6-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="c3cd6-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="c3cd6-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3cd6-316">備註</span><span class="sxs-lookup"><span data-stu-id="c3cd6-316">Remarks</span></span>

<span data-ttu-id="c3cd6-317">**Cim \_ SoftwareElement** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="c3cd6-318">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-318">WMI does not implement this class.</span></span> <span data-ttu-id="c3cd6-319">針對衍生自 **CIM \_ SOFTWAREELEMENT** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c3cd6-320">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c3cd6-321">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c3cd6-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cd6-322">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3cd6-322">Requirements</span></span>



| <span data-ttu-id="c3cd6-323">需求</span><span class="sxs-lookup"><span data-stu-id="c3cd6-323">Requirement</span></span> | <span data-ttu-id="c3cd6-324">值</span><span class="sxs-lookup"><span data-stu-id="c3cd6-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cd6-325">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3cd6-325">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cd6-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3cd6-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3cd6-327">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3cd6-327">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cd6-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3cd6-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3cd6-329">命名空間</span><span class="sxs-lookup"><span data-stu-id="c3cd6-329">Namespace</span></span><br/>                | <span data-ttu-id="c3cd6-330">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c3cd6-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3cd6-331">MOF</span><span class="sxs-lookup"><span data-stu-id="c3cd6-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3cd6-332"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3cd6-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3cd6-333">DLL</span><span class="sxs-lookup"><span data-stu-id="c3cd6-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3cd6-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3cd6-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cd6-335">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3cd6-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cd6-336">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c3cd6-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

