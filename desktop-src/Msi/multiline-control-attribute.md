---
description: 如果此位設定在編輯控制項上，安裝程式會使用垂直捲動條來建立多行編輯控制項。
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: 多行控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192221"
---
# <a name="multiline-control-attribute"></a>多行控制項屬性

如果此位設定在 [編輯控制項](edit-control.md)上，安裝程式會使用垂直捲動條來建立多行編輯控制項。

如果未設定此位，則會指定顯示一般編輯控制項。

## <a name="valid-controls"></a>有效的控制項

[編輯控制項](edit-control.md)。



| Decimal | 十六進位 | 常數                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制 [資料表](control-table.md)中，于控制項記錄的 [屬性] 資料行中包含多行位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



