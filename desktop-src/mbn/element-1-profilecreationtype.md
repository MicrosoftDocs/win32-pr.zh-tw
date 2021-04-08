---
description: 'ModemDMConfigProfile 中的 ProfileCreationType () '
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ModemDMConfigProfile 中的 ProfileCreationType () '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b755840d0308ec2d7a7bba5896b0cf67b7b61198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847989"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span data-ttu-id="91ec6-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ModemDMConfigProfile 中的 ProfileCreationType () </span><span class="sxs-lookup"><span data-stu-id="91ec6-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)</span></span>

<span data-ttu-id="91ec6-104">指定此數據機 DM 設定檔的建立方式。</span><span class="sxs-lookup"><span data-stu-id="91ec6-104">Specifies how this modem DM profile was created.</span></span>

<span data-ttu-id="91ec6-105">這個值是用來決定使用者是否可以刪除設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ec6-105">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="91ec6-106">使用者只能刪除 **UserProvisioned** 設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ec6-106">Users can only delete **UserProvisioned** profiles.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="91ec6-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="91ec6-107">Element hierarchy</span></span>

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="91ec6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ec6-108">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="91ec6-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="91ec6-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="91ec6-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="91ec6-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="91ec6-111">無。</span><span class="sxs-lookup"><span data-stu-id="91ec6-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="91ec6-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="91ec6-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="91ec6-113">無。</span><span class="sxs-lookup"><span data-stu-id="91ec6-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="91ec6-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="91ec6-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91ec6-115">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="91ec6-115">Parent Element</span></span></th>
<th><span data-ttu-id="91ec6-116">Description</span><span class="sxs-lookup"><span data-stu-id="91ec6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91ec6-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="91ec6-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="91ec6-118">數據機 DM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ec6-118">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="91ec6-119">相關元素</span><span class="sxs-lookup"><span data-stu-id="91ec6-119">Related elements</span></span>

<span data-ttu-id="91ec6-120">下列專案的名稱與這個專案的名稱相同，但內容或屬性不同：</span><span class="sxs-lookup"><span data-stu-id="91ec6-120">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="91ec6-121">**[MBNProfileExt 中的 ProfileCreationType ()](element-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="91ec6-121">**[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="91ec6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="91ec6-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91ec6-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="91ec6-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



