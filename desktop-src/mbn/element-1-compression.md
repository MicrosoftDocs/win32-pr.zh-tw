---
description: 'ModemDMConfigProfile \/ ... \/壓縮 (v4) '
MS-HAID: WWAN\_profile\_v4.element\_1\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: '壓縮 (v4) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8dc3acd6-5997-47a5-bd30-899569b9aad9
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5796afb061bdc758bba020384501699fe3627e16
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106999768"
---
# <a name="span-idwwan_profile_v4element_1_compressionspanmodemdmconfigprofilecompression-v4"></a><span data-ttu-id="d8da0-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile \/ ... \/壓縮 (v4) </span><span class="sxs-lookup"><span data-stu-id="d8da0-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile\/...\/Compression (v4)</span></span>

<span data-ttu-id="d8da0-104">指定是否要在資料連結上使用壓縮來進行標頭和資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="d8da0-104">Specifies whether compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="d8da0-105">如需詳細資訊，請參閱 v1 [**壓縮**](./schema-compression-contexttype-element.md) 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="d8da0-105">For more information, see the documentation for the v1 [**Compression**](./schema-compression-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d8da0-106">元素階層</span><span class="sxs-lookup"><span data-stu-id="d8da0-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a><span data-ttu-id="d8da0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8da0-107">Syntax</span></span>

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d8da0-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="d8da0-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d8da0-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="d8da0-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d8da0-110">無。</span><span class="sxs-lookup"><span data-stu-id="d8da0-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d8da0-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="d8da0-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d8da0-112">無。</span><span class="sxs-lookup"><span data-stu-id="d8da0-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d8da0-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="d8da0-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8da0-114">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="d8da0-114">Parent Element</span></span></th>
<th><span data-ttu-id="d8da0-115">描述</span><span class="sxs-lookup"><span data-stu-id="d8da0-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8da0-116"><a href="element-1-context.md">內容</a></span><span class="sxs-lookup"><span data-stu-id="d8da0-116"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="d8da0-117">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="d8da0-117">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d8da0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8da0-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8da0-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8da0-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
