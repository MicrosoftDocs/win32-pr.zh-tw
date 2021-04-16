---
description: 列舉，描述設定檔適用的網路連接種類。
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: iwlanApplicabilityType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511737"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="ebca7-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="ebca7-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="ebca7-104">列舉，描述設定檔適用的網路連接種類。</span><span class="sxs-lookup"><span data-stu-id="ebca7-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

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

## <a name="enumeration-values"></a><span data-ttu-id="ebca7-105">列舉值</span><span class="sxs-lookup"><span data-stu-id="ebca7-105">Enumeration values</span></span>

<span data-ttu-id="ebca7-106">**IwlanApplicabilityType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="ebca7-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebca7-107">值</span><span class="sxs-lookup"><span data-stu-id="ebca7-107">Value</span></span></th>
<th><span data-ttu-id="ebca7-108">描述</span><span class="sxs-lookup"><span data-stu-id="ebca7-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebca7-109">CellularOnly</span><span class="sxs-lookup"><span data-stu-id="ebca7-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="ebca7-110">設定檔僅適用于行動電話通訊網路。</span><span class="sxs-lookup"><span data-stu-id="ebca7-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebca7-111">CellularAndIwlan</span><span class="sxs-lookup"><span data-stu-id="ebca7-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="ebca7-112">設定檔適用于行動電話或 Wi-Fi 卸載連接。</span><span class="sxs-lookup"><span data-stu-id="ebca7-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebca7-113">IwlanOnly</span><span class="sxs-lookup"><span data-stu-id="ebca7-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="ebca7-114">設定檔僅適用于 Wi-Fi 卸載連接。</span><span class="sxs-lookup"><span data-stu-id="ebca7-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



