---
description: 這個屬性會指定是否啟用或停用指定的控制項。 停用時，大部分的控制項會顯示為灰色。
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: 啟用的控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977814"
---
# <a name="enabled-control-attribute"></a>啟用的控制項屬性

這個屬性會指定是否啟用或停用指定的控制項。 停用時，大部分的控制項會顯示為灰色。

如果設定此位，則會建立啟用的控制項。

如果未設定此位，則會將控制項建立為停用。

## <a name="valid-controls"></a>有效的控制項

所有控制項。 某些與屬性沒有關聯的控制項（例如點陣圖和圖示）的外觀不受設定這個屬性的影響。

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>備註

您也可以使用 [ControlCondition 資料表](controlcondition-table.md) ，根據屬性或條件陳述式的值來停用或啟用控制項。

您也可以藉由將控制項訂閱至 [ControlEvent](control-events.md)來啟用或停用控制項。 在 [屬性] 資料行中輸入屬性的識別碼，並在 [EventMapping 資料表](eventmapping-table.md)的事件資料行中輸入事件的識別碼。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



