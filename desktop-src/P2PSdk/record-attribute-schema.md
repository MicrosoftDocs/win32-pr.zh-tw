---
description: 記錄可能會有應用程式專屬的屬性，這些屬性是一系列的名稱或值組，以對等記錄結構之 pszAttributes 成員中的 XML 字串表示 \_ 。
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: 記錄屬性架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997901"
---
# <a name="record-attribute-schema"></a><span data-ttu-id="b31be-103">記錄屬性架構</span><span class="sxs-lookup"><span data-stu-id="b31be-103">Record Attribute Schema</span></span>

<span data-ttu-id="b31be-104">記錄可能會有應用程式專屬的屬性，這些屬性是一系列的名稱或值組，以 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)結構之 **PSZATTRIBUTES** 成員中的 XML 字串表示。</span><span class="sxs-lookup"><span data-stu-id="b31be-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="b31be-105">屬性是用來篩選 [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)呼叫所起始的記錄搜尋，這會採用 [記錄搜尋查詢格式](record-search-query-format.md) 所指定的 XML 搜尋篩選作為參數。</span><span class="sxs-lookup"><span data-stu-id="b31be-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="b31be-106">記錄屬性可以是下列三種類型的其中一種：</span><span class="sxs-lookup"><span data-stu-id="b31be-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="b31be-107">**int** 是整數值。</span><span class="sxs-lookup"><span data-stu-id="b31be-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="b31be-108">**date** 是表示為其中一種標準格式的日期時間值 [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) 。</span><span class="sxs-lookup"><span data-stu-id="b31be-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="b31be-109">**字串** 是 Unicode 字串值。</span><span class="sxs-lookup"><span data-stu-id="b31be-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="b31be-110">下列清單會識別對等基礎結構所保留的特定屬性名稱：</span><span class="sxs-lookup"><span data-stu-id="b31be-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="b31be-111">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="b31be-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="b31be-112">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="b31be-112">**peercreatorid**</span></span>
-   <span data-ttu-id="b31be-113">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="b31be-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="b31be-114">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="b31be-114">**peerrecordid**</span></span>
-   <span data-ttu-id="b31be-115">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="b31be-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="b31be-116">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="b31be-116">**peercreationtime**</span></span>
-   <span data-ttu-id="b31be-117">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="b31be-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="b31be-118">定義記錄屬性的範例</span><span class="sxs-lookup"><span data-stu-id="b31be-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="b31be-119">下列架構範例說明如何定義記錄屬性：</span><span class="sxs-lookup"><span data-stu-id="b31be-119">The following schema example shows you how to define record attributes:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> <span data-ttu-id="b31be-120">屬性名稱必須是英數位元的序列。</span><span class="sxs-lookup"><span data-stu-id="b31be-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="b31be-121">屬性名稱中不允許特殊字元，例如連字號 ( "-" ) 和底線 ( " \_ " ) 。</span><span class="sxs-lookup"><span data-stu-id="b31be-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="b31be-122">下列 XML 屬性序列範例包含自訂的 **AuthenticationType** 和 **AuthExpires** 屬性，這些屬性會出現在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)的 **pszAttributes** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b31be-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



