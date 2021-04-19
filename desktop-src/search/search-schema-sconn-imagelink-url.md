---
description: <url>元素指定此搜尋連接器的縮圖 URL。 如果 <imageLink> 存在，則需要這個元素。 它沒有任何子項目，而且沒有任何屬性。
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: 'imageLink url 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986309"
---
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="05bb5-105">imageLink url 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="05bb5-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="05bb5-106"><url>元素指定此搜尋連接器的縮圖 URL。</span><span class="sxs-lookup"><span data-stu-id="05bb5-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="05bb5-107">如果 <imageLink> 存在，則需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="05bb5-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="05bb5-108">它沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="05bb5-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="05bb5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="05bb5-109">Syntax</span></span>


```
<!-- url -->
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



## <a name="element-information"></a><span data-ttu-id="05bb5-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="05bb5-110">Element Information</span></span>



| <span data-ttu-id="05bb5-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="05bb5-111">Parent Element</span></span>                                                                   | <span data-ttu-id="05bb5-112">子元素</span><span class="sxs-lookup"><span data-stu-id="05bb5-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="05bb5-113">imageLink 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="05bb5-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="05bb5-114">備註</span><span class="sxs-lookup"><span data-stu-id="05bb5-114">Remarks</span></span>

<span data-ttu-id="05bb5-115">值可以是本機檔案系統路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="05bb5-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="05bb5-116">影像檔案可以是 Windows 7 (PNG、BMP、JPG、GIF) 所支援的任何基本映射類型。</span><span class="sxs-lookup"><span data-stu-id="05bb5-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="05bb5-117">ImageLinkurl 元素範例</span><span class="sxs-lookup"><span data-stu-id="05bb5-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



