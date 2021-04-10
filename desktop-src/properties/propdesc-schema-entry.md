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
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="a9358-103">瞭解屬性描述架構</span><span class="sxs-lookup"><span data-stu-id="a9358-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="a9358-104">本主題介紹 Shell 屬性系統所使用的屬性描述架構。</span><span class="sxs-lookup"><span data-stu-id="a9358-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="a9358-105">引進 Windows Vista 和更新版本的新功能需要將現有的 Shell 屬性系統延伸至：</span><span class="sxs-lookup"><span data-stu-id="a9358-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="a9358-106">支援豐富且可擴充的屬性描述系統，以提供屬性的相關資訊，包括顯示名稱、類型、顯示類型、排序和群組行為，以及呈現和操作屬性所需的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="a9358-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="a9358-107">支援屬性類型的庫存清單 (與可在不同的視圖中編輯這些類型的 UI （例如 listview、預覽窗格、屬性對話方塊等），以及可與各種屬性相關聯的) 。</span><span class="sxs-lookup"><span data-stu-id="a9358-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="a9358-108">提供屬性描述清單，定義各種不同視圖中所顯示的屬性集。</span><span class="sxs-lookup"><span data-stu-id="a9358-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="a9358-109">提供簡化的介面 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)，以便更輕鬆地撰寫屬性處理常式，因此可以將屬性保存到檔案中。</span><span class="sxs-lookup"><span data-stu-id="a9358-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="a9358-110">支援非檔案屬性處理常式以公開視圖中的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9358-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="a9358-111">這些功能是在提供 Shell 專案屬性之抽象存取的架構上達成。</span><span class="sxs-lookup"><span data-stu-id="a9358-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="a9358-112">此抽象概念稱為 Shell 屬性系統。</span><span class="sxs-lookup"><span data-stu-id="a9358-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="a9358-113">什麼是屬性描述架構？</span><span class="sxs-lookup"><span data-stu-id="a9358-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="a9358-114">為什麼要使用架構？</span><span class="sxs-lookup"><span data-stu-id="a9358-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="a9358-115">主要的架構元件有哪些？</span><span class="sxs-lookup"><span data-stu-id="a9358-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="a9358-116">Windows 7 的變更</span><span class="sxs-lookup"><span data-stu-id="a9358-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="a9358-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9358-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="a9358-118">什麼是屬性描述架構？</span><span class="sxs-lookup"><span data-stu-id="a9358-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="a9358-119">架構子系統包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="a9358-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="a9358-120">定義屬性描述的一或多個 propdesc 架構檔案。</span><span class="sxs-lookup"><span data-stu-id="a9358-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="a9358-121">屬性描述架構是在 XML 架構檔案的集合中定義 (在系統的執行時間) 使用 propdesc 副檔名。</span><span class="sxs-lookup"><span data-stu-id="a9358-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="a9358-122">當屬性系統的一部分需要這些檔案時，這些檔案會延遲載入。</span><span class="sxs-lookup"><span data-stu-id="a9358-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="a9358-123">記憶體中的架構快取，用來儲存剖析的架構檔案，其中包含引入子系統的所有屬性描述。</span><span class="sxs-lookup"><span data-stu-id="a9358-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="a9358-124">不需要重新分析描述架構的 propdesc 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9358-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="a9358-125">如需詳細資訊，請參閱 [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema)、 [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)和 [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema)。</span><span class="sxs-lookup"><span data-stu-id="a9358-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="a9358-126">執行 [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)的子系統物件，用來取得或使用屬性描述。</span><span class="sxs-lookup"><span data-stu-id="a9358-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="a9358-127">執行 [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)的子系統物件，此物件可用來根據屬性描述來通知和操作。</span><span class="sxs-lookup"><span data-stu-id="a9358-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="a9358-128">執行 [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)的子系統物件，此物件會用來做為屬性描述的集合。</span><span class="sxs-lookup"><span data-stu-id="a9358-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="a9358-129">您必須將新增 `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` 至 propdesc 檔案的根架構元素。</span><span class="sxs-lookup"><span data-stu-id="a9358-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="a9358-130">為什麼要使用架構？</span><span class="sxs-lookup"><span data-stu-id="a9358-130">Why Use a Schema?</span></span>

<span data-ttu-id="a9358-131">屬性本身不是型別安全。</span><span class="sxs-lookup"><span data-stu-id="a9358-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="a9358-132">元件可以將數值指派給 system.string 屬性或 AlbumTitle 屬性的 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 日期戳記，而且如果沒有任何進一步的強制或指引，屬性存放區將會允許它。</span><span class="sxs-lookup"><span data-stu-id="a9358-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="a9358-133">因此，我們需要一個概念來「schematize」屬性，這會將我們帶入架構子系統。</span><span class="sxs-lookup"><span data-stu-id="a9358-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="a9358-134">主要的架構元件有哪些？</span><span class="sxs-lookup"><span data-stu-id="a9358-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="a9358-135">Shell 屬性系統所使用的屬性描述架構是由單一 [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) 元素和 *schemaVersion* 屬性所組成，這表示此架構定義格式的版本。</span><span class="sxs-lookup"><span data-stu-id="a9358-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="a9358-136">注意：值必須是 "1.0"。</span><span class="sxs-lookup"><span data-stu-id="a9358-136">Note: value must be "1.0".</span></span>


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



<span data-ttu-id="a9358-137">[PropertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)包含一或多個 [propertyDescription](./propdesc-schema-propertydescription.md)元素，以及 *發行者* 和 *產品* 屬性。</span><span class="sxs-lookup"><span data-stu-id="a9358-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


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



<span data-ttu-id="a9358-138">[PropertyDescription](./propdesc-schema-propertydescription.md)由一個 [searchInfo](./propdesc-schema-searchinfo.md) 、零個或一個 [labelInfo](./propdesc-schema-labelinfo.md)、 [typeInfo](./propdesc-schema-typeinfo.md)和 [displayInfo](./propdesc-schema-displayinfo.md)元素所組成，以及 *formatID*、 *propID*、 *propstr* 和 *name* 屬性。</span><span class="sxs-lookup"><span data-stu-id="a9358-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="a9358-139">針對要在系統中提供的每個唯一標準屬性名稱，應該要有一個 [propertyDescription](./propdesc-schema-propertydescription.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="a9358-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="a9358-140">字串屬性的限制為512個字元。</span><span class="sxs-lookup"><span data-stu-id="a9358-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="a9358-141">超過512個字元的值會被截斷。</span><span class="sxs-lookup"><span data-stu-id="a9358-141">Values longer than 512 characters are truncated.</span></span>


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



## <a name="changes-for-windows-7"></a><span data-ttu-id="a9358-142">Windows 7 的變更</span><span class="sxs-lookup"><span data-stu-id="a9358-142">Changes for Windows 7</span></span>

<span data-ttu-id="a9358-143">Windows 7 的屬性描述架構已變更。</span><span class="sxs-lookup"><span data-stu-id="a9358-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="a9358-144">這些都是不中斷的變更。</span><span class="sxs-lookup"><span data-stu-id="a9358-144">These are non-breaking changes.</span></span> <span data-ttu-id="a9358-145">如果 Windows 7 中已不再支援屬性專案或屬性，則 Windows 7 作業系統會忽略 Windows Vista 元素或屬性。</span><span class="sxs-lookup"><span data-stu-id="a9358-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="a9358-146">同樣地，Windows Vista 也會忽略新的 Windows 7 屬性元素或屬性。</span><span class="sxs-lookup"><span data-stu-id="a9358-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="a9358-147">不過，建議您更新 Windows 7 的自訂屬性，以提供更佳且更一致的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="a9358-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="a9358-148">以下是新的元素和屬性：</span><span class="sxs-lookup"><span data-stu-id="a9358-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="a9358-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) 和 [relatedProperty](./propdesc-schema-relatedproperty.md) 元素</span><span class="sxs-lookup"><span data-stu-id="a9358-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="a9358-150">[image](./propdesc-schema-image.md) 元素</span><span class="sxs-lookup"><span data-stu-id="a9358-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="a9358-151">[searchInfo](./propdesc-schema-searchinfo.md)元素的助憶鍵屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="a9358-152">[enum](./propdesc-schema-enum.md)元素的助憶鍵屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="a9358-153">[typeInfo](./propdesc-schema-typeinfo.md)元素的 searchRawValue 屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="a9358-154">下列元素和屬性已變更：</span><span class="sxs-lookup"><span data-stu-id="a9358-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="a9358-155">[enumeratedList](./propdesc-schema-enumeratedlist.md)、 [enum](./propdesc-schema-enum.md)和 [enumRange](./propdesc-schema-enumrange.md) 元素</span><span class="sxs-lookup"><span data-stu-id="a9358-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="a9358-156">[drawControl](./propdesc-schema-drawcontrol.md) 元素</span><span class="sxs-lookup"><span data-stu-id="a9358-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="a9358-157">[editControl](./propdesc-schema-editcontrol.md) 元素</span><span class="sxs-lookup"><span data-stu-id="a9358-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="a9358-158">[propertyDescription](./propdesc-schema-propertydescription.md)元素的 propID 屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="a9358-159">[searchInfo](./propdesc-schema-searchinfo.md)元素的 columnIndexType 屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="a9358-160">已移除下列元素和屬性：</span><span class="sxs-lookup"><span data-stu-id="a9358-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="a9358-161">[queryControl](./propdesc-schema-querycontrol.md) 元素</span><span class="sxs-lookup"><span data-stu-id="a9358-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="a9358-162">[typeInfo](./propdesc-schema-typeinfo.md)元素的 isQueryable 屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="a9358-163">[typeInfo](./propdesc-schema-typeinfo.md)元素的 includeInFullTextQuery 屬性</span><span class="sxs-lookup"><span data-stu-id="a9358-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9358-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9358-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9358-165">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a9358-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a9358-166">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a9358-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a9358-167">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a9358-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a9358-168">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a9358-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a9358-169">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a9358-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a9358-170">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a9358-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a9358-171">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a9358-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a9358-172">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="a9358-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a9358-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a9358-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a9358-174">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a9358-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a9358-175">drawControl</span><span class="sxs-lookup"><span data-stu-id="a9358-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a9358-176">editControl</span><span class="sxs-lookup"><span data-stu-id="a9358-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a9358-177">filterControl</span><span class="sxs-lookup"><span data-stu-id="a9358-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a9358-178">queryControl</span><span class="sxs-lookup"><span data-stu-id="a9358-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="a9358-179">image</span><span class="sxs-lookup"><span data-stu-id="a9358-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
