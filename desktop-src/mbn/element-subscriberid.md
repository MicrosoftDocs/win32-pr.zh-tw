---
description: SubscriberID
MS-HAID: WWAN\_profile\_v4.element\_SubscriberID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SubscriberID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525cd75dbf1ab752ab17ea32d566e57977ab74a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972402"
---
# <a name="span-idwwan_profile_v4element_subscriberidspansubscriberid"></a><span data-ttu-id="aa50f-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span><span class="sxs-lookup"><span data-stu-id="aa50f-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span></span>

<span data-ttu-id="aa50f-104">識別設定檔的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa50f-104">Identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="aa50f-105">若為 GSM 網路，這應該包含 SIM 的 IMSI (國際行動使用者身分識別) ，而針對 CDMA 裝置，則應該包含裝置的最小 (行動電話識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="aa50f-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="aa50f-106">如需詳細資訊，請參閱 v1 [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="aa50f-106">For more information, see the documentation for the v1 [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="aa50f-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="aa50f-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<SubscriberID>**

## <a name="syntax"></a><span data-ttu-id="aa50f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa50f-108">Syntax</span></span>

``` syntax
<SubscriberID>

  subscriberIdType

</SubscriberID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="aa50f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="aa50f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="aa50f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="aa50f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="aa50f-111">無。</span><span class="sxs-lookup"><span data-stu-id="aa50f-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="aa50f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="aa50f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="aa50f-113">無。</span><span class="sxs-lookup"><span data-stu-id="aa50f-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="aa50f-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="aa50f-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa50f-115">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="aa50f-115">Parent Element</span></span></th>
<th><span data-ttu-id="aa50f-116">Description</span><span class="sxs-lookup"><span data-stu-id="aa50f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa50f-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="aa50f-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="aa50f-118"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="aa50f-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="aa50f-119">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa50f-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="aa50f-120">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="aa50f-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="aa50f-121">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa50f-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="aa50f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa50f-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa50f-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa50f-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
