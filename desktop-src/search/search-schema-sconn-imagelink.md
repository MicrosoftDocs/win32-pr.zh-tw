---
description: 選擇性 <imageLink> 元素會指定此搜尋連接器的縮圖。 這個元素有一個必要的子項目，而且沒有任何屬性。
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: 'imageLink 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970141"
---
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="3e231-104">imageLink 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="3e231-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="3e231-105">選擇性 <imageLink> 元素會指定此搜尋連接器的縮圖。</span><span class="sxs-lookup"><span data-stu-id="3e231-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="3e231-106">這個元素有一個必要的子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="3e231-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e231-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e231-107">Syntax</span></span>


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="3e231-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3e231-108">Element Information</span></span>



| <span data-ttu-id="3e231-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="3e231-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="3e231-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3e231-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e231-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="3e231-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="3e231-112">imageLink url 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="3e231-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="3e231-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e231-113">Remarks</span></span>

<span data-ttu-id="3e231-114">ImageLink 值可以是本機檔案系統路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="3e231-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="3e231-115">影像檔案可以是 Windows 7 (PNG、BMP、JPG、GIF) 所支援的任何基本映射類型。</span><span class="sxs-lookup"><span data-stu-id="3e231-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="3e231-116">ImageLink 元素範例</span><span class="sxs-lookup"><span data-stu-id="3e231-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



