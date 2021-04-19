---
description: 指定如何根據指定的屬性定義來設定 Windows 搜尋引擎。
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984190"
---
# <a name="searchinfo"></a><span data-ttu-id="17dac-103">searchInfo</span><span class="sxs-lookup"><span data-stu-id="17dac-103">searchInfo</span></span>

<span data-ttu-id="17dac-104">指定如何根據指定的屬性定義來設定 Windows 搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="17dac-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="17dac-105">如果未提供任何 [searchInfo]() 元素，則不會將屬性包含在 Windows 搜尋引擎中。</span><span class="sxs-lookup"><span data-stu-id="17dac-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="17dac-106">此元素已針對 Windows 7 變更。</span><span class="sxs-lookup"><span data-stu-id="17dac-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="17dac-107">Windows 7 的語法</span><span class="sxs-lookup"><span data-stu-id="17dac-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="17dac-108">Windows Vista 的語法</span><span class="sxs-lookup"><span data-stu-id="17dac-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="17dac-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="17dac-109">Element Information</span></span>



| <span data-ttu-id="17dac-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="17dac-110">Parent Element</span></span>                                                   | <span data-ttu-id="17dac-111">子元素</span><span class="sxs-lookup"><span data-stu-id="17dac-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="17dac-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="17dac-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="17dac-113">無</span><span class="sxs-lookup"><span data-stu-id="17dac-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="17dac-114">屬性</span><span class="sxs-lookup"><span data-stu-id="17dac-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17dac-115">屬性</span><span class="sxs-lookup"><span data-stu-id="17dac-115">Attribute</span></span></th>
<th><span data-ttu-id="17dac-116">描述</span><span class="sxs-lookup"><span data-stu-id="17dac-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17dac-117">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="17dac-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="17dac-118">公用。</span><span class="sxs-lookup"><span data-stu-id="17dac-118">Public.</span></span> <span data-ttu-id="17dac-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="17dac-119">Optional.</span></span> <span data-ttu-id="17dac-120">指出屬性值是否應該儲存在反向索引中。</span><span class="sxs-lookup"><span data-stu-id="17dac-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="17dac-121">這可讓終端使用者對這個屬性的值執行全文檢索查詢。</span><span class="sxs-lookup"><span data-stu-id="17dac-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="17dac-122">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="17dac-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17dac-123">isColumn</span><span class="sxs-lookup"><span data-stu-id="17dac-123">isColumn</span></span></td>
<td><span data-ttu-id="17dac-124">公用。</span><span class="sxs-lookup"><span data-stu-id="17dac-124">Public.</span></span> <span data-ttu-id="17dac-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="17dac-125">Optional.</span></span> <span data-ttu-id="17dac-126">指出屬性是否也應該以資料行的形式儲存在 Windows 搜尋資料庫中，讓獨立軟體廠商 (Isv) 可以建立以述詞為基礎的查詢 (例如 &quot; Select \* Where system.string &quot; &quot; = ' qqq ' &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="17dac-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="17dac-127">如果架構建立者想要讓使用者 (或開發人員) 在屬性上建立以述詞為基礎的查詢，則必須將此設定為 &quot; true &quot; 。</span><span class="sxs-lookup"><span data-stu-id="17dac-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="17dac-128">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="17dac-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17dac-129">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="17dac-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="17dac-130">公用。</span><span class="sxs-lookup"><span data-stu-id="17dac-130">Public.</span></span> <span data-ttu-id="17dac-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="17dac-131">Optional.</span></span> <span data-ttu-id="17dac-132">預設值為 &quot;True&quot;。</span><span class="sxs-lookup"><span data-stu-id="17dac-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="17dac-133">如果屬性是多重值，則這個屬性一律 &quot; 為 true &quot; 。</span><span class="sxs-lookup"><span data-stu-id="17dac-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17dac-134">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="17dac-134">columnIndexType</span></span></td>
<td><span data-ttu-id="17dac-135">公用。</span><span class="sxs-lookup"><span data-stu-id="17dac-135">Public.</span></span> <span data-ttu-id="17dac-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="17dac-136">Optional.</span></span> <span data-ttu-id="17dac-137">為了優化排序和分組，Windows 搜尋引擎可以針對具有 isColumn = true 的屬性建立次要索引 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="17dac-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="17dac-138">只有當 Windows Vista 中的 inInvertedIndex 為 &quot; true， &quot; 或 &quot; &quot; Windows 7 中的 isColumn 為 true 時，這個屬性才有用。</span><span class="sxs-lookup"><span data-stu-id="17dac-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="17dac-139">如果屬性通常會依使用者排序，則應該指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="17dac-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="17dac-140">Windows Vista 中的預設值為 &quot; NotIndexed &quot; 。</span><span class="sxs-lookup"><span data-stu-id="17dac-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="17dac-141">Windows 7 中的預設值為 &quot; OnDemand &quot; 。</span><span class="sxs-lookup"><span data-stu-id="17dac-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="17dac-142">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="17dac-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="17dac-143"><strong>NotIndexed</strong>：永不建立值索引。</span><span class="sxs-lookup"><span data-stu-id="17dac-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="17dac-144"><strong>OnDisk</strong>：建立這個屬性的預設值索引。</span><span class="sxs-lookup"><span data-stu-id="17dac-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="17dac-145"><strong>OnDiskAll</strong> (Windows 7 及更新版本僅限) ：建立這個屬性的預設值索引，如果它是向量屬性，則也是所有串連向量值的值索引。</span><span class="sxs-lookup"><span data-stu-id="17dac-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="17dac-146"><strong>OnDiskVector</strong> (Windows 7 及更新版本僅) ：為串連向量值建立預設值索引。</span><span class="sxs-lookup"><span data-stu-id="17dac-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="17dac-147"><strong>OnDemand</strong> (Windows 7 及更新版本僅限) ：僅依需求建立值索引，也就是只在第一次用於查詢時。</span><span class="sxs-lookup"><span data-stu-id="17dac-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17dac-148">maxSize</span><span class="sxs-lookup"><span data-stu-id="17dac-148">maxSize</span></span></td>
<td><span data-ttu-id="17dac-149">公用。</span><span class="sxs-lookup"><span data-stu-id="17dac-149">Public.</span></span> <span data-ttu-id="17dac-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="17dac-150">Optional.</span></span> <span data-ttu-id="17dac-151">儲存在 Windows 搜尋資料庫中的特定屬性所允許的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="17dac-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="17dac-152">預設值為：</span><span class="sxs-lookup"><span data-stu-id="17dac-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="17dac-153"><strong>Windows Vista</strong>：128位元組</span><span class="sxs-lookup"><span data-stu-id="17dac-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="17dac-154"><strong>Windows 7 和更新版本</strong>：512位元組</span><span class="sxs-lookup"><span data-stu-id="17dac-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="17dac-155">請注意，這個大小上限是以位元組為單位，而不是字元。</span><span class="sxs-lookup"><span data-stu-id="17dac-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="17dac-156">字元數目上限取決於其編碼方式。</span><span class="sxs-lookup"><span data-stu-id="17dac-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17dac-157">助憶鍵</span><span class="sxs-lookup"><span data-stu-id="17dac-157">mnemonics</span></span></td>
<td><span data-ttu-id="17dac-158"><strong>Windows 7 和更新版本。</strong></span><span class="sxs-lookup"><span data-stu-id="17dac-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="17dac-159">公用。</span><span class="sxs-lookup"><span data-stu-id="17dac-159">Public.</span></span> <span data-ttu-id="17dac-160">選擇性。</span><span class="sxs-lookup"><span data-stu-id="17dac-160">Optional.</span></span> <span data-ttu-id="17dac-161">助憶鍵值的清單，可用來參考搜尋查詢中的屬性。</span><span class="sxs-lookup"><span data-stu-id="17dac-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="17dac-162">此清單會以 ' | ' 字元分隔。</span><span class="sxs-lookup"><span data-stu-id="17dac-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
