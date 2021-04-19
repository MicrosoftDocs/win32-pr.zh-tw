---
description: 如果設定此位，則控制項中的文字會顯示在同一行上。 如果文字延伸超過控制項的邊界，則會被截斷，而且省略號 (&\# 0034; ... &\# 0034; ) 插入結尾以表示截斷。 如果未設定此位，則文字會換行。
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979198"
---
# <a name="nowrap-control-attribute"></a>NoWrap 控制項屬性

如果設定此位，則控制項中的文字會顯示在同一行上。 如果文字延伸超過控制項的邊界，則會截斷，並在結尾插入省略號 ( "... ) "，以表示截斷。 如果未設定此位，則文字會換行。

## <a name="valid-controls"></a>有效的控制項

[Text](text-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 NoWrap 位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



