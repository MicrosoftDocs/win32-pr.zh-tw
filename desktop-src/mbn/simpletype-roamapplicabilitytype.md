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
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType 簡單類型

RoamApplicabilityType 描述漫遊設定檔適用的漫遊條件。

這是比 [**roamControlType**](simpletype-roamcontroltype.md)更具表達性的屬性，而且設定檔應該使用 **roamControlType** 或 **roamApplicabilityType**，但不能同時使用兩者。  (如果設定檔同時使用，則會套用這兩者。 結果會是兩個的交集。 ) 

您可以使用這個屬性來區別多個具有相鄰漫遊條件的設定檔，以指定不同的配置檔案屬性，例如，home 與漫遊。

有三種可能的家用/漫遊註冊狀態：

-   首頁：在家用網路上註冊
-   夥伴：已在與家用網路緊密關聯的網路上註冊
-   非夥伴：在未與家用網路緊密關聯的網路上註冊

「夥伴」的精確意義取決於網路，但它代表比非合作夥伴更有利的更好的關係。 如果以地區為基礎的運算子在其主區域以外使用另一個操作員的無線電存取網路，就可能會發生這種情況。 它也可以代表區域內漫遊之間的差異 (例如，EU) 和外部。

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

## <a name="enumeration-values"></a>列舉值

**RoamApplicabilityType** 簡單類型會定義下列值。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>NonPartnerOnly</td>
<td><p>此設定檔僅適用于在非夥伴網路漫遊時</p></td>
</tr>
<tr class="even">
<td>PartnerOnly</td>
<td><p>此設定檔只會在合作夥伴網路上進行漫遊時使用</p></td>
</tr>
<tr class="odd">
<td>HomeOnly</td>
<td><p>只有在家用網路上才會使用此設定檔</p></td>
</tr>
<tr class="even">
<td>HomeAndPartner</td>
<td><p>此設定檔僅適用于在家或合作夥伴網路時</p></td>
</tr>
<tr class="odd">
<td>PartnerAndNonpartner</td>
<td><p>此設定檔是在任何網路上沒有家用 (漫遊時使用) </p></td>
</tr>
<tr class="even">
<td>AllRoaming</td>
<td><p>此設定檔用於所有網路</p></td>
</tr>
</tbody>
</table>

 

 



