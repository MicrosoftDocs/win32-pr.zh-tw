---
description: 描述設定檔如何控制漫遊。
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamControlType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b88d3d024c7fe4340c3e1ee54492e947f2443a5112c807dde2d494d57175c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065650"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType 簡單類型

描述設定檔如何控制漫遊。

有兩種可能的漫遊註冊狀態：

-   夥伴：已在與家用網路緊密關聯的網路上註冊
-   非夥伴：在未與家用網路緊密關聯的網路上註冊

「夥伴」的精確意義取決於網路，但它代表比非合作夥伴更有利的更好的關係。 如果以地區為基礎的運算子在其主區域以外使用另一個操作員的無線電存取網路，就可能會發生這種情況。 它也可以代表區域內漫遊之間的差異 (例如，EU) 和外部。

請注意， [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) 是比 **roamControlType** 更具表達性的屬性，而且設定檔應該使用 **roamControlType** 或 **roamApplicabilityType**，但不能同時使用兩者。  (如果設定檔同時使用，則會套用這兩者。 結果會是兩個的交集。 ) 

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

## <a name="enumeration-values"></a>列舉值

**RoamControlType** 簡單類型會定義下列值。

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
<td>AllRoamAllowed</td>
<td><p>合作夥伴和非合作夥伴網路上允許漫遊。</p></td>
</tr>
<tr class="even">
<td>PartnerRoamAllowed</td>
<td><p>只有合作夥伴網路才能進行漫遊。</p></td>
</tr>
<tr class="odd">
<td>NoRoamAllowed</td>
<td><p>不允許漫遊。</p></td>
</tr>
</tbody>
</table>

 

 



