---
description: 列舉，描述設定檔適用的網路連接種類。
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: iwlanApplicabilityType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529ae39c2b0e137825e7a80d41c43203b0a27de7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478954"
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


| 值 | 描述 | 
|-------|-------------|
| CellularOnly | <p>設定檔僅適用于行動電話通訊網路。</p> | 
| CellularAndIwlan | <p>設定檔適用于行動電話或 Wi-Fi 卸載連接。</p> | 
| IwlanOnly | <p>設定檔僅適用于 Wi-Fi 卸載連接。</p> | 


 

 



