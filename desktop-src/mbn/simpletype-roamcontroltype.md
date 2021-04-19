---
description: 描述設定檔如何控制漫遊。
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamControlType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972647"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="39fe9-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="39fe9-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="39fe9-104">描述設定檔如何控制漫遊。</span><span class="sxs-lookup"><span data-stu-id="39fe9-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="39fe9-105">有兩種可能的漫遊註冊狀態：</span><span class="sxs-lookup"><span data-stu-id="39fe9-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="39fe9-106">夥伴：已在與家用網路緊密關聯的網路上註冊</span><span class="sxs-lookup"><span data-stu-id="39fe9-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="39fe9-107">非夥伴：在未與家用網路緊密關聯的網路上註冊</span><span class="sxs-lookup"><span data-stu-id="39fe9-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="39fe9-108">「夥伴」的精確意義取決於網路，但它代表比非合作夥伴更有利的更好的關係。</span><span class="sxs-lookup"><span data-stu-id="39fe9-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="39fe9-109">如果以地區為基礎的運算子在其主區域以外使用另一個操作員的無線電存取網路，就可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="39fe9-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="39fe9-110">它也可以代表區域內漫遊之間的差異 (例如，EU) 和外部。</span><span class="sxs-lookup"><span data-stu-id="39fe9-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="39fe9-111">請注意， [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) 是比 **roamControlType** 更具表達性的屬性，而且設定檔應該使用 **roamControlType** 或 **roamApplicabilityType**，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="39fe9-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="39fe9-112"> (如果設定檔同時使用，則會套用這兩者。</span><span class="sxs-lookup"><span data-stu-id="39fe9-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="39fe9-113">結果會是兩個的交集。 ) </span><span class="sxs-lookup"><span data-stu-id="39fe9-113">The result is the intersection of the two.)</span></span>

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="39fe9-114">列舉值</span><span class="sxs-lookup"><span data-stu-id="39fe9-114">Enumeration values</span></span>

<span data-ttu-id="39fe9-115">**RoamControlType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="39fe9-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39fe9-116">值</span><span class="sxs-lookup"><span data-stu-id="39fe9-116">Value</span></span></th>
<th><span data-ttu-id="39fe9-117">描述</span><span class="sxs-lookup"><span data-stu-id="39fe9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39fe9-118">AllRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="39fe9-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="39fe9-119">合作夥伴和非合作夥伴網路上允許漫遊。</span><span class="sxs-lookup"><span data-stu-id="39fe9-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fe9-120">PartnerRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="39fe9-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="39fe9-121">只有合作夥伴網路才能進行漫遊。</span><span class="sxs-lookup"><span data-stu-id="39fe9-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fe9-122">NoRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="39fe9-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="39fe9-123">不允許漫遊。</span><span class="sxs-lookup"><span data-stu-id="39fe9-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



