---
description: 代表載入至非暫時性存放裝置的低層級軟體，用來啟動和設定電腦系統 (CIM 無系統 \_) 。
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: 'CIM_BIOSElement 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986404"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="fbc0d-103">CIM_BIOSElement 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="fbc0d-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="fbc0d-104">代表載入至非暫時性存放裝置的低層級軟體，用來啟動和設定電腦系統 (CIM 無系統) [**\_**](cim-computersystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc0d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbc0d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="fbc0d-106">成員</span><span class="sxs-lookup"><span data-stu-id="fbc0d-106">Members</span></span>

<span data-ttu-id="fbc0d-107">**CIM \_ BIOSElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fbc0d-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="fbc0d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="fbc0d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbc0d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="fbc0d-109">Properties</span></span>

<span data-ttu-id="fbc0d-110">**CIM \_ BIOSElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbc0d-111">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ BIOSElement**.**ListOfLanguages**") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-115">BIOS 目前選取的語言。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="fbc0d-116">這項資訊可從系統管理 BIOS (SMBIOS) 使用類型13結構的目前語言屬性來編制索引，以在結構後面的字串清單中編制索引。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="fbc0d-117">這個屬性會使用 ISO 639 語言名稱進行格式化，並可在後面加上 ISO 3166 區功能變數名稱稱和編碼方法。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-118">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-119">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fbc0d-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-121">適用于 BIOS 的可安裝語言清單。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="fbc0d-122">此資訊可以從 SMBIOS 取得，從類型13結構後面的字串清單中取得。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="fbc0d-123">必須使用 ISO 639 語言名稱來指定 BIOS 可安裝的語言。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="fbc0d-124">您也可以依照語言名稱，指定 ISO 3166 區功能變數名稱稱和編碼方法。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-125">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.6 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-129">BIOS 所佔用記憶體的結束位址。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-130">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-131">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-133">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-134">BIOS 所佔用記憶體的起始位址。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-135">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-138">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| SYSTEM BIOS \| 001.7 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-139">一個自由格式字串，描述更新 **CIM \_ BIOSElement** 物件所需的 BIOS flash/載入公用程式。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="fbc0d-140">版本和其他資訊可能會顯示在此屬性中。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-141">**製造商**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-144">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-145">軟體元素的製造商。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-146">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-149">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-150">如果這是電腦系統的主要 BIOS，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-151">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-152">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fbc0d-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-154">BIOS 執行符合的 BIOS 屬性登錄的發佈位置。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-155">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-156">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-158">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.8 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-159">此 BIOS 的發行日期。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="fbc0d-160">**版本**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbc0d-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fbc0d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbc0d-163">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="fbc0d-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="fbc0d-164">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="fbc0d-164">The version of the operation.</span></span> <span data-ttu-id="fbc0d-165">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="fbc0d-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="fbc0d-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="fbc0d-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="fbc0d-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="fbc0d-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbc0d-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbc0d-168">Requirements</span></span>



| <span data-ttu-id="fbc0d-169">需求</span><span class="sxs-lookup"><span data-stu-id="fbc0d-169">Requirement</span></span> | <span data-ttu-id="fbc0d-170">值</span><span class="sxs-lookup"><span data-stu-id="fbc0d-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc0d-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbc0d-171">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc0d-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fbc0d-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fbc0d-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbc0d-173">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc0d-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbc0d-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fbc0d-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="fbc0d-175">Namespace</span></span><br/>                | <span data-ttu-id="fbc0d-176">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fbc0d-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fbc0d-177">MOF</span><span class="sxs-lookup"><span data-stu-id="fbc0d-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbc0d-178"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fbc0d-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbc0d-179">DLL</span><span class="sxs-lookup"><span data-stu-id="fbc0d-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbc0d-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbc0d-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbc0d-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbc0d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc0d-182">**CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="fbc0d-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

