---
description: IsAdditionalPdpCoNtextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpCoNtextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318319"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="aa1f5-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpCoNtextProfile</span><span class="sxs-lookup"><span data-stu-id="aa1f5-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="aa1f5-104">**IsAdditionalPdpCoNtextProfile** 元素包含 **布林值**，如果這是「額外的 PDP (封包資料通訊協定) 內容」設定檔，則為 **true** ，否則為 **false**。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="aa1f5-105">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-105">Default is **false**.</span></span>

<span data-ttu-id="aa1f5-106">「額外的 PDP 內容」設定檔是不會透過實體介面卡預設埠啟動的設定檔，並將此元素設定為 true，可確保此設定檔不會在使用者介面中不當顯示。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="aa1f5-107">請注意，如果此元素設定為 true，則下列專案也必須為 true。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="aa1f5-108">必須指定 [**IsDefault**](./schema-isdefault-mbnprofile-element.md) 元素或將其設為 **false** ，設定檔才會是有效的。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="aa1f5-109">[**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md)元素必須未指定或設為 **manual** ，設定檔才會生效。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="aa1f5-110">元素階層</span><span class="sxs-lookup"><span data-stu-id="aa1f5-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="aa1f5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa1f5-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="aa1f5-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="aa1f5-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="aa1f5-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="aa1f5-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="aa1f5-114">無。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="aa1f5-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="aa1f5-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="aa1f5-116">無。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="aa1f5-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="aa1f5-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="aa1f5-118">這個最外層的 (檔) 元素可能不會包含在任何其他專案中。</span><span class="sxs-lookup"><span data-stu-id="aa1f5-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1f5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa1f5-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa1f5-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa1f5-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
