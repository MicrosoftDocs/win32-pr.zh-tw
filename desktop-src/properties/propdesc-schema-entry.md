---
description: 本主題介紹 Shell 屬性系統所使用的屬性描述架構。
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: 瞭解屬性描述架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026519"
---
# <a name="understanding-the-property-description-schema"></a>瞭解屬性描述架構

本主題介紹 Shell 屬性系統所使用的屬性描述架構。

引進 Windows Vista 和更新版本的新功能需要將現有的 Shell 屬性系統延伸至：

-   支援豐富且可擴充的屬性描述系統，以提供屬性的相關資訊，包括顯示名稱、類型、顯示類型、排序和群組行為，以及呈現和操作屬性所需的其他屬性。
-   支援屬性類型的庫存清單 (與可在不同的視圖中編輯這些類型的 UI （例如 listview、預覽窗格、屬性對話方塊等），以及可與各種屬性相關聯的) 。
-   提供屬性描述清單，定義各種不同視圖中所顯示的屬性集。
-   提供簡化的介面 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)，以便更輕鬆地撰寫屬性處理常式，因此可以將屬性保存到檔案中。
-   支援非檔案屬性處理常式以公開視圖中的屬性。

這些功能是在提供 Shell 專案屬性之抽象存取的架構上達成。 此抽象概念稱為 Shell 屬性系統。

-   [什麼是屬性描述架構？](#what-is-the-property-description-schema)
-   [為什麼要使用架構？](#why-use-a-schema)
-   [主要的架構元件有哪些？](#what-are-the-major-schema-parts)
-   [Windows 7 的變更](#changes-for-windows-7)
-   [相關主題](#related-topics)

## <a name="what-is-the-property-description-schema"></a>什麼是屬性描述架構？

架構子系統包含下列各項：

-   定義屬性描述的一或多個 propdesc 架構檔案。 屬性描述架構是在 XML 架構檔案的集合中定義 (在系統的執行時間) 使用 propdesc 副檔名。 當屬性系統的一部分需要這些檔案時，這些檔案會延遲載入。
-   記憶體中的架構快取，用來儲存剖析的架構檔案，其中包含引入子系統的所有屬性描述。 不需要重新分析描述架構的 propdesc 設定檔。 如需詳細資訊，請參閱 [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema)、 [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)和 [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema)。
-   執行 [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)的子系統物件，用來取得或使用屬性描述。
-   執行 [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)的子系統物件，此物件可用來根據屬性描述來通知和操作。
-   執行 [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)的子系統物件，此物件會用來做為屬性描述的集合。

> [!Note]  
> 您必須將新增 `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` 至 propdesc 檔案的根架構元素。

 

## <a name="why-use-a-schema"></a>為什麼要使用架構？

屬性本身不是型別安全。 元件可以將數值指派給 system.string 屬性或 AlbumTitle 屬性的 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 日期戳記，而且如果沒有任何進一步的強制或指引，屬性存放區將會允許它。 因此，我們需要一個概念來「schematize」屬性，這會將我們帶入架構子系統。

## <a name="what-are-the-major-schema-parts"></a>主要的架構元件有哪些？

Shell 屬性系統所使用的屬性描述架構是由單一 [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) 元素和 *schemaVersion* 屬性所組成，這表示此架構定義格式的版本。 注意：值必須是 "1.0"。


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



[PropertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)包含一或多個 [propertyDescription](./propdesc-schema-propertydescription.md)元素，以及 *發行者* 和 *產品* 屬性。


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



[PropertyDescription](./propdesc-schema-propertydescription.md)由一個 [searchInfo](./propdesc-schema-searchinfo.md) 、零個或一個 [labelInfo](./propdesc-schema-labelinfo.md)、 [typeInfo](./propdesc-schema-typeinfo.md)和 [displayInfo](./propdesc-schema-displayinfo.md)元素所組成，以及 *formatID*、 *propID*、 *propstr* 和 *name* 屬性。

針對要在系統中提供的每個唯一標準屬性名稱，應該要有一個 [propertyDescription](./propdesc-schema-propertydescription.md) 元素。 字串屬性的限制為512個字元。 超過512個字元的值會被截斷。


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a>Windows 7 的變更

Windows 7 的屬性描述架構已變更。 這些都是不中斷的變更。 如果 Windows 7 中已不再支援屬性專案或屬性，則 Windows 7 作業系統會忽略 Windows Vista 元素或屬性。 同樣地，Windows Vista 也會忽略新的 Windows 7 屬性元素或屬性。

不過，建議您更新 Windows 7 的自訂屬性，以提供更佳且更一致的使用者體驗。

以下是新的元素和屬性：

-   [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) 和 [relatedProperty](./propdesc-schema-relatedproperty.md) 元素
-   [image](./propdesc-schema-image.md) 元素
-   [searchInfo](./propdesc-schema-searchinfo.md)元素的助憶鍵屬性
-   [enum](./propdesc-schema-enum.md)元素的助憶鍵屬性
-   [typeInfo](./propdesc-schema-typeinfo.md)元素的 searchRawValue 屬性

下列元素和屬性已變更：

-   [enumeratedList](./propdesc-schema-enumeratedlist.md)、 [enum](./propdesc-schema-enum.md)和 [enumRange](./propdesc-schema-enumrange.md) 元素
-   [drawControl](./propdesc-schema-drawcontrol.md) 元素
-   [editControl](./propdesc-schema-editcontrol.md) 元素
-   [propertyDescription](./propdesc-schema-propertydescription.md)元素的 propID 屬性
-   [searchInfo](./propdesc-schema-searchinfo.md)元素的 columnIndexType 屬性

已移除下列元素和屬性：

-   [queryControl](./propdesc-schema-querycontrol.md) 元素
-   [typeInfo](./propdesc-schema-typeinfo.md)元素的 isQueryable 屬性
-   [typeInfo](./propdesc-schema-typeinfo.md)元素的 includeInFullTextQuery 屬性

## <a name="related-topics"></a>相關主題

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[>cultureinfo.numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
