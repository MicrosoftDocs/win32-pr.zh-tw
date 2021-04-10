---
description: DisplayProviderName
MS-HAID: WWAN\_profile\_v2.element\_DisplayProviderName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DisplayProviderName
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 906f844d483789decb88a9d97fca083ef10f5550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026197"
---
# <a name="span-idwwan_profile_v2element_displayprovidernamespandisplayprovidername"></a><span data-ttu-id="dcd03-103"><span id="WWAN_profile_v2.element_DisplayProviderName"></span>DisplayProviderName</span><span class="sxs-lookup"><span data-stu-id="dcd03-103"><span id="WWAN_profile_v2.element_DisplayProviderName"></span>DisplayProviderName</span></span>

<span data-ttu-id="dcd03-104">[**DisplayProviderName**](element-displayprovidername.md)元素是選擇性的 [**providerNameType**](./schema-providernametype-simpletype.md) ，其中包含要顯示在 Windows 連線管理員中的網路連線名稱。</span><span class="sxs-lookup"><span data-stu-id="dcd03-104">The [**DisplayProviderName**](element-displayprovidername.md) element is an optional [**providerNameType**](./schema-providernametype-simpletype.md) that contains the network connection name to display in the Windows Connection Manager.</span></span> <span data-ttu-id="dcd03-105">只有當訂閱者位於家用網路而不是漫遊時，才會顯示此名稱。</span><span class="sxs-lookup"><span data-stu-id="dcd03-105">This name will only be displayed if the subscriber is on a home network and not roaming.</span></span> <span data-ttu-id="dcd03-106">漫遊網路名稱會根據行動寬頻裝置的資訊顯示。</span><span class="sxs-lookup"><span data-stu-id="dcd03-106">The roaming network name is displayed based on information from the mobile broadband device.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="dcd03-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="dcd03-107">Element hierarchy</span></span>

**<DisplayProviderName>**

## <a name="syntax"></a><span data-ttu-id="dcd03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcd03-108">Syntax</span></span>

``` syntax
<DisplayProviderName>

  providerNameType

</DisplayProviderName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="dcd03-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="dcd03-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="dcd03-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="dcd03-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="dcd03-111">無。</span><span class="sxs-lookup"><span data-stu-id="dcd03-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="dcd03-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="dcd03-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="dcd03-113">無。</span><span class="sxs-lookup"><span data-stu-id="dcd03-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="dcd03-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="dcd03-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="dcd03-115">這個最外層的 (檔) 元素可能不會包含在任何其他專案中。</span><span class="sxs-lookup"><span data-stu-id="dcd03-115">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd03-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcd03-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcd03-117">命名空間</span><span class="sxs-lookup"><span data-stu-id="dcd03-117">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v2</p></td>
</tr>
</tbody>
</table>

 

 
