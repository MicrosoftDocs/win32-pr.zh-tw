---
description: 選擇性的布林值 <isDefaultSaveLocation> 元素會指定是否應該使用搜尋連接器中所述的位置做為預設的儲存位置。 這個元素沒有任何子項目，而且沒有任何屬性。
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: 'isDefaultSaveLocation 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318140"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="d29fd-104">isDefaultSaveLocation 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="d29fd-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="d29fd-105">選擇性的布林值 <isDefaultSaveLocation> 元素會指定是否應該使用搜尋連接器中所述的位置做為預設的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="d29fd-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="d29fd-106">這個元素沒有任何子項目，而且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="d29fd-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29fd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d29fd-107">Syntax</span></span>


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="d29fd-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d29fd-108">Element Information</span></span>



| <span data-ttu-id="d29fd-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="d29fd-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="d29fd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d29fd-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="d29fd-111">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="d29fd-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="d29fd-112">備註</span><span class="sxs-lookup"><span data-stu-id="d29fd-112">Remarks</span></span>

<span data-ttu-id="d29fd-113">當使用者選擇儲存專案時，Windows 檔案總管會將專案儲存至元素中指定的位置 <simpleLocation> 。</span><span class="sxs-lookup"><span data-stu-id="d29fd-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="d29fd-114">使用者可以使用搜尋連接器的 [屬性] 對話方塊來變更此設定。</span><span class="sxs-lookup"><span data-stu-id="d29fd-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="d29fd-115">範例</span><span class="sxs-lookup"><span data-stu-id="d29fd-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



