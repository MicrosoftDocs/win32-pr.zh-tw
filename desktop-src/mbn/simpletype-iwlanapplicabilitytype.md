---
description: 列舉，描述設定檔適用的網路連接種類。
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: iwlanApplicabilityType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ede1e4c360bfd88fa8ca0eb3494a9400f4dfc2a1eb70f7857156caabf7b469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035746"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType 簡單類型

列舉，描述設定檔適用的網路連接種類。

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**IwlanApplicabilityType** 簡單類型會定義下列值。

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
<td>CellularOnly</td>
<td><p>設定檔僅適用于行動電話通訊網路。</p></td>
</tr>
<tr class="even">
<td>CellularAndIwlan</td>
<td><p>設定檔適用于行動電話或 Wi-Fi 卸載連接。</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>設定檔僅適用于 Wi-Fi 卸載連接。</p></td>
</tr>
</tbody>
</table>

 

 



