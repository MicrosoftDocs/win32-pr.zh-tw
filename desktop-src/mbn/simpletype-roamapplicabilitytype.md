---
description: RoamApplicabilityType 描述漫遊設定檔適用的漫遊條件。
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamApplicabilityType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847984"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="3fb32-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="3fb32-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="3fb32-104">RoamApplicabilityType 描述漫遊設定檔適用的漫遊條件。</span><span class="sxs-lookup"><span data-stu-id="3fb32-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="3fb32-105">這是比 [**roamControlType**](simpletype-roamcontroltype.md)更具表達性的屬性，而且設定檔應該使用 **roamControlType** 或 **roamApplicabilityType**，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="3fb32-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="3fb32-106"> (如果設定檔同時使用，則會套用這兩者。</span><span class="sxs-lookup"><span data-stu-id="3fb32-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="3fb32-107">結果會是兩個的交集。 ) </span><span class="sxs-lookup"><span data-stu-id="3fb32-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="3fb32-108">您可以使用這個屬性來區別多個具有相鄰漫遊條件的設定檔，以指定不同的配置檔案屬性，例如，home 與漫遊。</span><span class="sxs-lookup"><span data-stu-id="3fb32-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="3fb32-109">有三種可能的家用/漫遊註冊狀態：</span><span class="sxs-lookup"><span data-stu-id="3fb32-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="3fb32-110">首頁：在家用網路上註冊</span><span class="sxs-lookup"><span data-stu-id="3fb32-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="3fb32-111">夥伴：已在與家用網路緊密關聯的網路上註冊</span><span class="sxs-lookup"><span data-stu-id="3fb32-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="3fb32-112">非夥伴：在未與家用網路緊密關聯的網路上註冊</span><span class="sxs-lookup"><span data-stu-id="3fb32-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="3fb32-113">「夥伴」的精確意義取決於網路，但它代表比非合作夥伴更有利的更好的關係。</span><span class="sxs-lookup"><span data-stu-id="3fb32-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="3fb32-114">如果以地區為基礎的運算子在其主區域以外使用另一個操作員的無線電存取網路，就可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="3fb32-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="3fb32-115">它也可以代表區域內漫遊之間的差異 (例如，EU) 和外部。</span><span class="sxs-lookup"><span data-stu-id="3fb32-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="3fb32-116">列舉值</span><span class="sxs-lookup"><span data-stu-id="3fb32-116">Enumeration values</span></span>

<span data-ttu-id="3fb32-117">**RoamApplicabilityType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="3fb32-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fb32-118">值</span><span class="sxs-lookup"><span data-stu-id="3fb32-118">Value</span></span></th>
<th><span data-ttu-id="3fb32-119">描述</span><span class="sxs-lookup"><span data-stu-id="3fb32-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3fb32-120">NonPartnerOnly</span><span class="sxs-lookup"><span data-stu-id="3fb32-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="3fb32-121">此設定檔僅適用于在非夥伴網路漫遊時</span><span class="sxs-lookup"><span data-stu-id="3fb32-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fb32-122">PartnerOnly</span><span class="sxs-lookup"><span data-stu-id="3fb32-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="3fb32-123">此設定檔只會在合作夥伴網路上進行漫遊時使用</span><span class="sxs-lookup"><span data-stu-id="3fb32-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fb32-124">HomeOnly</span><span class="sxs-lookup"><span data-stu-id="3fb32-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="3fb32-125">只有在家用網路上才會使用此設定檔</span><span class="sxs-lookup"><span data-stu-id="3fb32-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fb32-126">HomeAndPartner</span><span class="sxs-lookup"><span data-stu-id="3fb32-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="3fb32-127">此設定檔僅適用于在家或合作夥伴網路時</span><span class="sxs-lookup"><span data-stu-id="3fb32-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fb32-128">PartnerAndNonpartner</span><span class="sxs-lookup"><span data-stu-id="3fb32-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="3fb32-129">此設定檔是在任何網路上沒有家用 (漫遊時使用) </span><span class="sxs-lookup"><span data-stu-id="3fb32-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fb32-130">AllRoaming</span><span class="sxs-lookup"><span data-stu-id="3fb32-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="3fb32-131">此設定檔用於所有網路</span><span class="sxs-lookup"><span data-stu-id="3fb32-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



