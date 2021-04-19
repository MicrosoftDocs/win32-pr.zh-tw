---
description: 指定如何顯示內容的標籤。
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974384"
---
# <a name="labelinfo"></a><span data-ttu-id="f3212-103">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f3212-103">labelInfo</span></span>

<span data-ttu-id="f3212-104">指定如何顯示內容的標籤。</span><span class="sxs-lookup"><span data-stu-id="f3212-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="f3212-105">每個[propertyDescription](./propdesc-schema-propertydescription.md)專案都只能有一個[labelInfo]()元素。</span><span class="sxs-lookup"><span data-stu-id="f3212-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="f3212-106">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="f3212-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="f3212-107">如果未提供任何 [labelInfo]() 元素，則不會顯示內容的標籤;不過，這通常是一個瑕疵。</span><span class="sxs-lookup"><span data-stu-id="f3212-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3212-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3212-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f3212-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f3212-109">Element Information</span></span>



| <span data-ttu-id="f3212-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="f3212-110">Parent Element</span></span>                                                   | <span data-ttu-id="f3212-111">子元素</span><span class="sxs-lookup"><span data-stu-id="f3212-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f3212-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f3212-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="f3212-113">無</span><span class="sxs-lookup"><span data-stu-id="f3212-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f3212-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f3212-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3212-115">屬性</span><span class="sxs-lookup"><span data-stu-id="f3212-115">Attribute</span></span></th>
<th><span data-ttu-id="f3212-116">描述</span><span class="sxs-lookup"><span data-stu-id="f3212-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3212-117">label</span><span class="sxs-lookup"><span data-stu-id="f3212-117">label</span></span></td>
<td><span data-ttu-id="f3212-118">公用。</span><span class="sxs-lookup"><span data-stu-id="f3212-118">Public.</span></span> <span data-ttu-id="f3212-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f3212-119">Optional.</span></span> <span data-ttu-id="f3212-120">顯示在 UI 中的標籤 (例如，[詳細資料] 資料行標籤或 [預覽] 窗格) 。</span><span class="sxs-lookup"><span data-stu-id="f3212-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="f3212-121">語法允許直接顯示字串或間接顯示字串參考。</span><span class="sxs-lookup"><span data-stu-id="f3212-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="f3212-122">使用間接顯示字串，因為它可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="f3212-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="f3212-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription：： GetDisplayName</strong></a> 會傳回已解析的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f3212-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3212-124">sortDescription</span><span class="sxs-lookup"><span data-stu-id="f3212-124">sortDescription</span></span></td>
<td><span data-ttu-id="f3212-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f3212-125">Optional.</span></span> <span data-ttu-id="f3212-126">指定以排序選項提供的字串。</span><span class="sxs-lookup"><span data-stu-id="f3212-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="f3212-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription：： GetSortDescription</strong></a> 會傳回此排序描述。</span><span class="sxs-lookup"><span data-stu-id="f3212-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="f3212-128">下列值提供對應的 UI 字串。</span><span class="sxs-lookup"><span data-stu-id="f3212-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="f3212-129">一般： &quot; 排序向上 &quot;  /  &quot; 排序下移&quot;</span><span class="sxs-lookup"><span data-stu-id="f3212-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="f3212-130">AToZ：頂端 &quot; &quot;  /  &quot; Z 頂端的&quot;</span><span class="sxs-lookup"><span data-stu-id="f3212-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="f3212-131">LowestHighest：頂端 &quot; &quot;  /  &quot; 最高的最高&quot;</span><span class="sxs-lookup"><span data-stu-id="f3212-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="f3212-132">OldestNewest：最舊的最 &quot; &quot;  /  &quot; 新頂端&quot;</span><span class="sxs-lookup"><span data-stu-id="f3212-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="f3212-133">SmallestLargest：頂端最 &quot; &quot;  /  &quot; 大的最小值&quot;</span><span class="sxs-lookup"><span data-stu-id="f3212-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3212-134">invitationText</span><span class="sxs-lookup"><span data-stu-id="f3212-134">invitationText</span></span></td>
<td><span data-ttu-id="f3212-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f3212-135">Optional.</span></span> <span data-ttu-id="f3212-136">顯示為控制項或工具提示 (使用者之指示的說明字串文字，請 &quot; 輸入作者名稱。 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="f3212-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="f3212-137">語法允許直接顯示字串或間接顯示字串參考。</span><span class="sxs-lookup"><span data-stu-id="f3212-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="f3212-138">使用間接顯示字串，因為它可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="f3212-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="f3212-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription：： GetEditInvitation</strong></a> 會傳回已解析的邀請文字。</span><span class="sxs-lookup"><span data-stu-id="f3212-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3212-140">hideLabel</span><span class="sxs-lookup"><span data-stu-id="f3212-140">hideLabel</span></span></td>
<td><span data-ttu-id="f3212-141">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f3212-141">Optional.</span></span> <span data-ttu-id="f3212-142">預設值為 &quot;false&quot;。</span><span class="sxs-lookup"><span data-stu-id="f3212-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="f3212-143">指出標籤是否隱藏。</span><span class="sxs-lookup"><span data-stu-id="f3212-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
