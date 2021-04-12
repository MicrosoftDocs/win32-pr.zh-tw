---
description: 專案 <simpleLocation> 會指定以檔案系統為基礎或依通訊協定處理常式為基礎之搜尋連接器的位置。 此元素有兩個子項目，而且沒有任何屬性。
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: 'simpleLocation 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318136"
---
# <a name="simplelocation-element-search-connector-schema"></a><span data-ttu-id="93176-104">simpleLocation 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="93176-104">simpleLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="93176-105">專案 <simpleLocation> 會指定以檔案系統為基礎或依通訊協定處理常式為基礎之搜尋連接器的位置。</span><span class="sxs-lookup"><span data-stu-id="93176-105">The <simpleLocation> element specifies the location for search connectors that are file-system based or protocol-handler based.</span></span> <span data-ttu-id="93176-106">此元素有兩個子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="93176-106">This element has two child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="93176-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="93176-107">Syntax</span></span>


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="93176-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="93176-108">Element Information</span></span>



| <span data-ttu-id="93176-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="93176-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="93176-110">子元素</span><span class="sxs-lookup"><span data-stu-id="93176-110">Child Elements</span></span>                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93176-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="93176-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="93176-112">simpleLocation url 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="93176-112">simpleLocation url Element (Search Connector Schema)</span></span>](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | <span data-ttu-id="93176-113">已序列化：此元素包含指向專案中定義之位置的 base64 編碼 ShellLink <url> 。</span><span class="sxs-lookup"><span data-stu-id="93176-113">serialized: This element contains the base64-encoded ShellLink pointing to the location defined in the <url> element.</span></span> <span data-ttu-id="93176-114">Windows 7 會從專案的值建立 ShellLink <url> ，並在此程式庫的第一次載入時適當地更新此欄位，作者應將其保留空白。</span><span class="sxs-lookup"><span data-stu-id="93176-114">Windows 7 creates the ShellLink from the value of the <url> element and properly updates this field on the first load of this library, so it should be left empty by the author.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="93176-115">備註</span><span class="sxs-lookup"><span data-stu-id="93176-115">Remarks</span></span>

<span data-ttu-id="93176-116">您可以使用這個元素，而不是在 <locationProvider> 檔案系統上的位置，或連接器是已知的通訊協定處理常式 (例如 mapi： ) 。</span><span class="sxs-lookup"><span data-stu-id="93176-116">This element can be used instead of <locationProvider> when the location is on the file system or the connector is a known protocol handler (like mapi:).</span></span> <span data-ttu-id="93176-117">如果 <simpleLocation> 存在，就不能有 <locationProvider> 元素。</span><span class="sxs-lookup"><span data-stu-id="93176-117">If <simpleLocation> is present, there MUST NOT be a <locationProvider> element.</span></span> <span data-ttu-id="93176-118">若為 web 服務提供者搜尋連接器，請改用 [<locationProvider>](search-schema-sconn-locationprovider.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="93176-118">For web service provider search connectors, use the [<locationProvider>](search-schema-sconn-locationprovider.md) element instead.</span></span>

## <a name="examples"></a><span data-ttu-id="93176-119">範例</span><span class="sxs-lookup"><span data-stu-id="93176-119">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



