---
description: 'MBNProfileExt \/ ... \/AccessString (v4) '
MS-HAID: WWAN\_profile\_v4.element\_AccessString
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AccessString
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3216ac7b-e799-4734-8655-64e32b888d1c
api_name:
- AccessString
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dec0b54f4e6539fb12ab2f2150f13a8c2046f58a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112916"
---
# <a name="span-idwwan_profile_v4element_accessstringspanmbnprofileextaccessstring-v4"></a><span data-ttu-id="ff4fd-103"><span id="WWAN_profile_v4.element_AccessString"></span>MBNProfileExt \/ ... \/AccessString (v4) </span><span class="sxs-lookup"><span data-stu-id="ff4fd-103"><span id="WWAN_profile_v4.element_AccessString"></span>MBNProfileExt\/...\/AccessString (v4)</span></span>

<span data-ttu-id="ff4fd-104">識別要用來建立資料連線的 APN 或撥號字串。</span><span class="sxs-lookup"><span data-stu-id="ff4fd-104">Identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="ff4fd-105">如需詳細資訊，請參閱 v1 [**AccessString**](./schema-accessstring-contexttype-element.md) 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="ff4fd-105">For more information, see the documentation for the v1 [**AccessString**](./schema-accessstring-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="ff4fd-106">元素階層</span><span class="sxs-lookup"><span data-stu-id="ff4fd-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AccessString\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AccessString\>**

## <a name="syntax"></a><span data-ttu-id="ff4fd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff4fd-107">Syntax</span></span>

``` syntax
<AccessString>

  [TBD (missing description)]

</AccessString>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="ff4fd-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="ff4fd-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="ff4fd-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="ff4fd-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="ff4fd-110">無。</span><span class="sxs-lookup"><span data-stu-id="ff4fd-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="ff4fd-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="ff4fd-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="ff4fd-112">無。</span><span class="sxs-lookup"><span data-stu-id="ff4fd-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="ff4fd-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="ff4fd-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff4fd-114">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="ff4fd-114">Parent Element</span></span></th>
<th><span data-ttu-id="ff4fd-115">描述</span><span class="sxs-lookup"><span data-stu-id="ff4fd-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff4fd-116"><a href="element-context.md">內容</a></span><span class="sxs-lookup"><span data-stu-id="ff4fd-116"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="ff4fd-117">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="ff4fd-117">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="ff4fd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff4fd-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff4fd-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="ff4fd-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
