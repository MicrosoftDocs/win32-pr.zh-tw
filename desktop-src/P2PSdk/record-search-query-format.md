---
description: 呼叫 PeerGroupSearchRecords 函式時，需要用來判斷搜尋基本準則的 XML 查詢字串參數。
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: 記錄搜尋查詢格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850891"
---
# <a name="record-search-query-format"></a><span data-ttu-id="b9bf1-103">記錄搜尋查詢格式</span><span class="sxs-lookup"><span data-stu-id="b9bf1-103">Record Search Query Format</span></span>

<span data-ttu-id="b9bf1-104">呼叫 [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) 函式時，需要用來判斷搜尋基本準則的 XML 查詢字串參數。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="b9bf1-105">使用下列架構來制訂 XML 字串：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-105">Use the following schema to formulate an XML string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="b9bf1-106">用於記錄搜尋的元素</span><span class="sxs-lookup"><span data-stu-id="b9bf1-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="b9bf1-107">記錄搜尋中的主要元素是 **peersearch**，其中包含 **xmlns** 屬性中相關聯架構 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="b9bf1-108">使用 **peersearch** 做為子專案時，您可以使用 **and**、 **子句** 和 **或** 做為子項目。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="b9bf1-109">**和** - **和** 元素會對開頭和結束記號所包含的一或多個子句執行邏輯 and 運算。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="b9bf1-110">其他 **和** 和 **或** 標記可以是子系，而且其子子句的遞迴結果會包含在作業中。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="b9bf1-111">例如，如果您想要取得的記錄中包含的名稱等於 James Peters、最後一個更新大於2/28/2003，或是小於1/31/2003 的建立日期，請使用下列 XML 查詢字串：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   <span data-ttu-id="b9bf1-112">**子句** - **子句** 元素會指定基本的比較規則，將特定記錄屬性的值與開頭和結束記號之間的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="b9bf1-113">[ **類型** ] 和 [ **比較** ] 屬性必須提供 [ **比較** ] 表示要執行的比較作業。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="b9bf1-114">例如，表示所有相符記錄的簡單搜尋必須具有等於 James Peters 的 **peercreatorid** 值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="b9bf1-115">一般 **類型** 屬性包括 **int**、 **string** 和 **date**。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="b9bf1-116">**Date** 屬性可以是中所述的其中一種標準日期格式 [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) 。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="b9bf1-117">**Compare** 屬性的值是 **相等**、 **notequal**、 **less**、**大於**、 **lessorequal** 和 **greaterorequal**。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="b9bf1-118">**或** - **或** 專案會對開頭和結束記號所包含的一或多個子句執行邏輯 or 運算。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="b9bf1-119">其他 **或** 和 **和** 元素可以是子系，而子子句的遞迴結果則包含在作業中。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="b9bf1-120">例如，如果您想要取得的記錄中包含的名稱等於 James Peters，或者是1/31/2003 到2/28/2003 之間的最後一個更新，請使用下列 XML 查詢字串：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="b9bf1-121">記錄搜尋的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="b9bf1-121">More Information About a Record Search</span></span>

<span data-ttu-id="b9bf1-122">**Peersearch** 之後的第一個節點層級只能有一個元素。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="b9bf1-123">不過，該元素的後續子系可以有許多相同層級的元素。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="b9bf1-124">下列搜尋查詢不正確：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-124">The following search query is incorrect:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

<span data-ttu-id="b9bf1-125">查詢失敗的原因是，針對比對傳回兩個值，但未將其解析為一個 true/false 值，這表示一個子句查詢的記錄名稱等於 James Peters，而 AND 運算則符合兩個元件子句。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="b9bf1-126">結果會是兩個邏輯 true/false 值互相矛盾。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="b9bf1-127">若要取得名稱等於 James Peters 的所有記錄，以及介於1/31/2003 到2/28/2003 之間的最後一個更新，請將 **子句** 和 **和** 標記放在開頭和結尾 **和** 標記之間的相同層級。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="b9bf1-128">下列範例會顯示成功的查詢：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-128">The following example shows you the successful query:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

<span data-ttu-id="b9bf1-129">下列清單指出您必須知道才能撰寫成功查詢的其他特定資訊：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="b9bf1-130">在開頭和結尾 **子句** 標記之間找不到 **and** 和 **or** 標記，因為在該設定中，它們會被解釋為要比對的值的一部分，而這會導致錯誤或失敗的相符。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="b9bf1-131">每一組 **和** 和 **或** 開頭和結束記號都必須包含至少一個或多個子節點。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="b9bf1-132">此架構中不允許零個元素集合。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="b9bf1-133">記錄屬性</span><span class="sxs-lookup"><span data-stu-id="b9bf1-133">Record Attributes</span></span>

<span data-ttu-id="b9bf1-134">使用者可以使用 [記錄屬性架構](record-attribute-schema.md)，建立子句專案中的 **attrib** XML 屬性所指定的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="b9bf1-135">您可以使用架構中指定的格式，將 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)的 **PSZATTRIBUTES** 成員設定為 XML 字串，藉以加入新記錄的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="b9bf1-136">對等基礎結構會保留下列屬性名稱：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="b9bf1-137">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="b9bf1-138">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-138">**peercreatorid**</span></span>
-   <span data-ttu-id="b9bf1-139">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="b9bf1-140">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-140">**peerrecordid**</span></span>
-   <span data-ttu-id="b9bf1-141">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="b9bf1-142">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-142">**peercreationtime**</span></span>
-   <span data-ttu-id="b9bf1-143">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="b9bf1-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="b9bf1-144">特殊字元</span><span class="sxs-lookup"><span data-stu-id="b9bf1-144">Special Characters</span></span>

<span data-ttu-id="b9bf1-145">某些字元可以用來表示比對模式，或換用其他特殊字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="b9bf1-146">下表將說明這些字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="b9bf1-147">字元模式</span><span class="sxs-lookup"><span data-stu-id="b9bf1-147">Character pattern</span></span> | <span data-ttu-id="b9bf1-148">Description</span><span class="sxs-lookup"><span data-stu-id="b9bf1-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="b9bf1-149">萬用字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-149">The wildcard character.</span></span> <span data-ttu-id="b9bf1-150">當子句值中遇到此字元時，它會比對任何值的 0-n 字元，包括空白字元和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="b9bf1-151">例如：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-151">For example:</span></span><br/> <span data-ttu-id="b9bf1-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"</span><span class="sxs-lookup"><span data-stu-id="b9bf1-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="b9bf1-153">這個子句會比對名字為 "James" 和姓氏開頭為 "P" 的所有 **peercreatorid** 值。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="b9bf1-154">轉義的星號。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-154">An escaped asterisk.</span></span> <span data-ttu-id="b9bf1-155">此序列符合星號字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b9bf1-156">?</span><span class="sxs-lookup"><span data-stu-id="b9bf1-156">?</span></span>                 | <span data-ttu-id="b9bf1-157">單一字元的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-157">The single-character wildcard character.</span></span> <span data-ttu-id="b9bf1-158">當子句值中遇到此字元時，它會比對任何單一字元，包括空白字元和英數位元。例如：</span><span class="sxs-lookup"><span data-stu-id="b9bf1-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="b9bf1-159">「<clause attrib="filename" type="string" compare="equal">data-0？」。xml</clause>"</span><span class="sxs-lookup"><span data-stu-id="b9bf1-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="b9bf1-160">這個子句會比對 **檔案名** 值，例如 "data-01.xml" 和 "data-0B.xml"。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="b9bf1-161">\\?</span><span class="sxs-lookup"><span data-stu-id="b9bf1-161">\\?</span></span>               | <span data-ttu-id="b9bf1-162">已標記的問號。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-162">An escaped question mark.</span></span> <span data-ttu-id="b9bf1-163">此序列符合問號字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="b9bf1-164">已轉義的反斜線。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-164">An escaped backslash.</span></span> <span data-ttu-id="b9bf1-165">此序列符合單一反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="b9bf1-166">如果字元序列無效， [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) 函數就會傳回錯誤 **E \_ INVALIDARG**。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="b9bf1-167">不正確序列是包含 " \\ " (反斜線) 字元後面不緊接 " \* " (星號) 字元、"？" (問號) 字元或另一個 " \\ " (反斜線) 字元的序列。</span><span class="sxs-lookup"><span data-stu-id="b9bf1-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




