---
description: MsiExtractPatchXMLData 函式或 ExtractPatchXMLData 方法所傳回的修補程式排序和適用性資訊，是 XML blob 的格式，其中包含本主題中所識別的元素和屬性。
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: 將修補程式資訊以 XML 形式解壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0574d953609b467c42467853f540dc85c9c24a31c07b3b3d006eaa6633472d53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821678"
---
# <a name="extracting-patch-information-as-xml"></a>將修補程式資訊以 XML 形式解壓縮

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)函式或 [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)方法所傳回的修補程式排序和適用性資訊，是 XML blob 的格式，其中包含本主題中所識別的元素和屬性。 XML blob 可提供至 [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) 和 [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) ，而不是完整的修補檔案。

-   MsiPatch 元素是 XML blob 的最上層元素，包含修補程式的相關資訊。

    SchemaVersion 屬性會指定架構定義的版本。 架構是由 MSIPatchApplicability 指定，而目前的架構版本是1.0.0.0。 PatchGUID 屬性的值是修補程式套件的 GUID 修補程式碼，從修補程式 [摘要資訊資料流程](summary-information-stream.md)中的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性取得。 MinMsiVersion 是安裝從 [[**字數統計] 摘要**](word-count-summary.md)屬性取得之修補程式所需 Windows Installer 的最小版本。

-   TargetProduct 元素是一個容器元素，可取得修補程式目標應用程式的相關資訊。

    如果 patch 可以套用至多個應用程式，則可以有多個 TargetProduct 元素。 TargetProduct 元素中的資訊會從內嵌于修補程式的轉換中解壓縮。

-   TargetProductCode 元素包含目標應用程式的 [ [**ProductCode**](productcode.md) ] 屬性值，然後再套用修補程式。

    如果 patch 可以套用至多個應用程式，則可以有多個 TargetProductCode 元素。

-   UpdatedProductCode 元素包含套用修補程式之後，目標應用程式的產品代碼 GUID。

    只有當 patch 變更 [ [**ProductCode**](productcode.md) ] 屬性的值時，才會出現這個元素。 變更 **ProductCode** 的修補程式稱為 [主要升級](major-upgrades.md)。

-   TargetVersion 元素包含目標應用程式的 [**ProductVersion**](productversion.md) 屬性，再套用修補程式。
-   UpdateVersion 元素包含套用修補程式之後，目標應用程式的 [**ProductVersion**](productversion.md) 屬性值。

    只有當 patch 變更 [**ProductVersion**](productversion.md) 屬性的值時，才會出現這個元素。 執行 [小型更新](small-updates.md)（也稱為 QFE）之修補程式的 XML blob 將不會包含此元素。 執行次要升級的修補程式（也稱為 service pack）的 XML blob 將包含此元素。

-   TargetLanguage 元素包含目標應用程式的 [**ProductLanguage**](productlanguage.md) 屬性值，再套用修補程式。
-   UpdatedLanguages 元素包含套用修補程式之後的 [**ProductLanguage**](productlanguage.md) 屬性值。
-   UpgradeCode 元素包含目標應用程式的 [**UpgradeCode**](upgradecode.md) 屬性值。
-   ObsoletedPatch 元素包含修補程式碼 (Guid) 這些修補程式指定為過時的修補程式。

    已淘汰的修補程式清單取自修補程式 [摘要資訊資料流程](summary-information-stream.md)中的 [**修訂編號摘要**](revision-number-summary.md)。

-   SequenceData 元素包含修補程式的修補程式排序資訊。

    XML blob 中可以有多個 SequenceData 元素。 每個 SequenceData 專案都包含修補程式 [MsiPatchSequence 資料表](msipatchsequence-table.md) 中一個資料列的資訊。 SequenceData 元素包含 MsiPatchSequence 資料表中對應欄位中資訊的 ProductCode、Sequence 和 Attributes 子項目。 如需每個欄位的描述，請參閱 [MsiPatchSequence 資料表](msipatchsequence-table.md) 一節。

## <a name="extracting-applicability-information"></a>解壓縮適用性資訊

下列範例示範如何使用 [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)，將 Windows Installer 修補程式 ( .msp 檔案的適用性資訊解壓縮) 。 已解壓縮的 XML blob 會以 MSIPatchApplicability 中的架構定義為基礎，並傳回至 szXMLData。


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



下列範例示範如何將 Windows Installer 修補程式 ( .msp 檔的適用性資訊解壓縮) XML 格式。 已解壓縮的 XML blob 會以 MSIPatchApplicability 中的架構定義為基礎，並在 strPatchXML 中傳回。

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>修補適用性架構定義

將下列文字複製到記事本或其他文字編輯器，以針對 XML blob 中的修補程式適用性資訊建立架構定義檔。 將這個檔案命名為 MSIPatchApplicability .XSD。

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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ExtractPatchXMLData**](installer-extractpatchxmldata.md)
</dt> <dt>

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



