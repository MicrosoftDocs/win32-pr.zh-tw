---
description: 這個屬性會指定是否要將回復備份檔案包含在 VolumeCostList 控制項所顯示的成本中。
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: ControlShowRollbackCost 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a888df328062a81637b36dc3fcfbe178d6e49bd4aee01c65b2d2e3524fb321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379923"
---
# <a name="controlshowrollbackcost-control-attribute"></a>ControlShowRollbackCost 控制項屬性

這個屬性會指定是否要將回復備份檔案包含在 [VolumeCostList 控制項](volumecostlist-control.md)所顯示的成本中。

如果設定此位，且 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) 屬性 = P，則會將回復備份檔案包含在 [VolumeCostList 控制項](volumecostlist-control.md)所顯示的成本中。

如果未設定此位且 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) 屬性 = P，則不會在 [VolumeCostList 控制項](volumecostlist-control.md)所顯示的成本中包含復原備份檔案。

## <a name="valid-controls"></a>有效的控制項

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>備註

如果 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D 或 F，則會忽略這個控制項屬性。

如果 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F，則會包含復原的成本、備份檔案。

如果 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D 或 [**DISABLEROLLBACK**](-disablerollback.md) 屬性 = 1，就不會包含復原的成本。

 

 



