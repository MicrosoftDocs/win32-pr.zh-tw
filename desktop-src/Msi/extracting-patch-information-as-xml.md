---
description: MsiExtractPatchXMLData 函式或 ExtractPatchXMLData 方法所傳回的修補程式排序和適用性資訊，是 XML blob 的格式，其中包含本主題中所識別的元素和屬性。
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: 將修補程式資訊以 XML 形式解壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114564"
---
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="2d277-103">將修補程式資訊以 XML 形式解壓縮</span><span class="sxs-lookup"><span data-stu-id="2d277-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="2d277-104">[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)函式或 [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)方法所傳回的修補程式排序和適用性資訊，是 XML blob 的格式，其中包含本主題中所識別的元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="2d277-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="2d277-105">XML blob 可提供至 [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) 和 [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) ，而不是完整的修補檔案。</span><span class="sxs-lookup"><span data-stu-id="2d277-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="2d277-106">MsiPatch 元素是 XML blob 的最上層元素，包含修補程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d277-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="2d277-107">SchemaVersion 屬性會指定架構定義的版本。</span><span class="sxs-lookup"><span data-stu-id="2d277-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="2d277-108">架構是由 MSIPatchApplicability 指定，而目前的架構版本是1.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="2d277-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="2d277-109">PatchGUID 屬性的值是修補程式套件的 GUID 修補程式碼，從修補程式 [摘要資訊資料流程](summary-information-stream.md)中的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="2d277-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="2d277-110">MinMsiVersion 是安裝從 [ [**字數統計] 摘要**](word-count-summary.md) 屬性取得之修補程式所需 Windows Installer 的最小版本。</span><span class="sxs-lookup"><span data-stu-id="2d277-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="2d277-111">TargetProduct 元素是一個容器元素，可取得修補程式目標應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d277-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="2d277-112">如果 patch 可以套用至多個應用程式，則可以有多個 TargetProduct 元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="2d277-113">TargetProduct 元素中的資訊會從內嵌于修補程式的轉換中解壓縮。</span><span class="sxs-lookup"><span data-stu-id="2d277-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="2d277-114">TargetProductCode 元素包含目標應用程式的 [ [**ProductCode**](productcode.md) ] 屬性值，然後再套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="2d277-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="2d277-115">如果 patch 可以套用至多個應用程式，則可以有多個 TargetProductCode 元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="2d277-116">UpdatedProductCode 元素包含套用修補程式之後，目標應用程式的產品代碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="2d277-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="2d277-117">只有當 patch 變更 [ [**ProductCode**](productcode.md) ] 屬性的值時，才會出現這個元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="2d277-118">變更 **ProductCode** 的修補程式稱為 [主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="2d277-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="2d277-119">TargetVersion 元素包含目標應用程式的 [**ProductVersion**](productversion.md) 屬性，再套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="2d277-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="2d277-120">UpdateVersion 元素包含套用修補程式之後，目標應用程式的 [**ProductVersion**](productversion.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="2d277-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="2d277-121">只有當 patch 變更 [**ProductVersion**](productversion.md) 屬性的值時，才會出現這個元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="2d277-122">執行 [小型更新](small-updates.md)（也稱為 QFE）之修補程式的 XML blob 將不會包含此元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="2d277-123">執行次要升級的修補程式（也稱為 service pack）的 XML blob 將包含此元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="2d277-124">TargetLanguage 元素包含目標應用程式的 [**ProductLanguage**](productlanguage.md) 屬性值，再套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="2d277-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="2d277-125">UpdatedLanguages 元素包含套用修補程式之後的 [**ProductLanguage**](productlanguage.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="2d277-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="2d277-126">UpgradeCode 元素包含目標應用程式的 [**UpgradeCode**](upgradecode.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="2d277-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="2d277-127">ObsoletedPatch 元素包含修補程式碼 (Guid) 這些修補程式指定為過時的修補程式。</span><span class="sxs-lookup"><span data-stu-id="2d277-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="2d277-128">已淘汰的修補程式清單取自修補程式 [摘要資訊資料流程](summary-information-stream.md)中的 [**修訂編號摘要**](revision-number-summary.md)。</span><span class="sxs-lookup"><span data-stu-id="2d277-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="2d277-129">SequenceData 元素包含修補程式的修補程式排序資訊。</span><span class="sxs-lookup"><span data-stu-id="2d277-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="2d277-130">XML blob 中可以有多個 SequenceData 元素。</span><span class="sxs-lookup"><span data-stu-id="2d277-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="2d277-131">每個 SequenceData 專案都包含修補程式 [MsiPatchSequence 資料表](msipatchsequence-table.md) 中一個資料列的資訊。</span><span class="sxs-lookup"><span data-stu-id="2d277-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="2d277-132">SequenceData 元素包含 MsiPatchSequence 資料表中對應欄位中資訊的 ProductCode、Sequence 和 Attributes 子項目。</span><span class="sxs-lookup"><span data-stu-id="2d277-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="2d277-133">如需每個欄位的描述，請參閱 [MsiPatchSequence 資料表](msipatchsequence-table.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="2d277-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="2d277-134">解壓縮適用性資訊</span><span class="sxs-lookup"><span data-stu-id="2d277-134">Extracting Applicability Information</span></span>

<span data-ttu-id="2d277-135">下列範例示範如何使用 [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)，將 Windows Installer 修補程式 ( .msp 檔案的適用性資訊解壓縮) 。</span><span class="sxs-lookup"><span data-stu-id="2d277-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="2d277-136">已解壓縮的 XML blob 會以 MSIPatchApplicability 中的架構定義為基礎，並傳回至 szXMLData。</span><span class="sxs-lookup"><span data-stu-id="2d277-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



<span data-ttu-id="2d277-137">下列範例示範如何將 Windows Installer 修補程式 ( .msp 檔的適用性資訊解壓縮) XML 格式。</span><span class="sxs-lookup"><span data-stu-id="2d277-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="2d277-138">已解壓縮的 XML blob 會以 MSIPatchApplicability 中的架構定義為基礎，並在 strPatchXML 中傳回。</span><span class="sxs-lookup"><span data-stu-id="2d277-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="2d277-139">修補適用性架構定義</span><span class="sxs-lookup"><span data-stu-id="2d277-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="2d277-140">將下列文字複製到 [記事本] 或其他文字編輯器，以針對 XML blob 中的修補程式適用性資訊建立架構定義檔。</span><span class="sxs-lookup"><span data-stu-id="2d277-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="2d277-141">將這個檔案命名為 MSIPatchApplicability .XSD。</span><span class="sxs-lookup"><span data-stu-id="2d277-141">Name this file MSIPatchApplicability.XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a><span data-ttu-id="2d277-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d277-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d277-143">**ExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="2d277-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="2d277-144">**MsiDeterminePatchSequence**</span><span class="sxs-lookup"><span data-stu-id="2d277-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="2d277-145">**MsiDetermineApplicablePatches**</span><span class="sxs-lookup"><span data-stu-id="2d277-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="2d277-146">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="2d277-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



