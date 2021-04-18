---
description: 'ModemDMConfigProfile \/ ... \/IPType (v4) '
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPType (v4) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec57fbe0bbcb4c633ddb8485f048ce4230e0ca5
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106976310"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span data-ttu-id="16bcb-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile \/ ... \/IPType (v4) </span><span class="sxs-lookup"><span data-stu-id="16bcb-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile\/...\/IPType (v4)</span></span>

<span data-ttu-id="16bcb-104">指定要用於此資料連線的 IP 類型。</span><span class="sxs-lookup"><span data-stu-id="16bcb-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="16bcb-105">此元素是架構 v4 中的新專案。</span><span class="sxs-lookup"><span data-stu-id="16bcb-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="16bcb-106">元素可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="16bcb-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="16bcb-107">值</span><span class="sxs-lookup"><span data-stu-id="16bcb-107">Value</span></span>   | <span data-ttu-id="16bcb-108">意義</span><span class="sxs-lookup"><span data-stu-id="16bcb-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="16bcb-109">預設</span><span class="sxs-lookup"><span data-stu-id="16bcb-109">Default</span></span> | <span data-ttu-id="16bcb-110">IP 類型是由較低層 () 所挑選</span><span class="sxs-lookup"><span data-stu-id="16bcb-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="16bcb-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="16bcb-111">IPv4</span></span>    | <span data-ttu-id="16bcb-112">使用 IPv4</span><span class="sxs-lookup"><span data-stu-id="16bcb-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="16bcb-113">IPv6</span><span class="sxs-lookup"><span data-stu-id="16bcb-113">IPv6</span></span>    | <span data-ttu-id="16bcb-114">使用 IPv6</span><span class="sxs-lookup"><span data-stu-id="16bcb-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="16bcb-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="16bcb-115">IPv4v6</span></span>  | <span data-ttu-id="16bcb-116">使用 IPv4 和（或） IPv6 （如有提供）。</span><span class="sxs-lookup"><span data-stu-id="16bcb-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="16bcb-117">XLAT</span><span class="sxs-lookup"><span data-stu-id="16bcb-117">XLAT</span></span>    | <span data-ttu-id="16bcb-118">使用464XLAT 透過 IPv6 網路將 IPv4 通道</span><span class="sxs-lookup"><span data-stu-id="16bcb-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="16bcb-119">元素階層</span><span class="sxs-lookup"><span data-stu-id="16bcb-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="16bcb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="16bcb-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="16bcb-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="16bcb-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="16bcb-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="16bcb-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="16bcb-123">無。</span><span class="sxs-lookup"><span data-stu-id="16bcb-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="16bcb-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="16bcb-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="16bcb-125">無。</span><span class="sxs-lookup"><span data-stu-id="16bcb-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="16bcb-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="16bcb-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16bcb-127">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="16bcb-127">Parent Element</span></span></th>
<th><span data-ttu-id="16bcb-128">描述</span><span class="sxs-lookup"><span data-stu-id="16bcb-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16bcb-129"><a href="element-1-context.md">內容</a></span><span class="sxs-lookup"><span data-stu-id="16bcb-129"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="16bcb-130">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="16bcb-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="16bcb-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="16bcb-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16bcb-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="16bcb-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



