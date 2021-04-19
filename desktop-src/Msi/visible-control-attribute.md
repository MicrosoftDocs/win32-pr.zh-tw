---
description: 如果已設定可見的控制項位，則會在對話方塊中顯示控制項。 如果未設定此位，則會在對話方塊中隱藏控制項。 Visible 控制項屬性的可見或隱藏狀態可以稍後由控制項事件變更。
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Visible 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970156"
---
# <a name="visible-control-attribute"></a>Visible 控制項屬性

如果已設定可見的控制項位，則會在對話方塊中顯示控制項。 如果未設定此位，則會在對話方塊中隱藏控制項。 Visible 控制項屬性的可見或隱藏狀態可以稍後由 [控制項事件](control-events.md)變更。

## <a name="valid-controls"></a>有效的控制項

所有控制項。

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>備註

您可以使用 [ControlCondition 資料表](controlcondition-table.md) ，根據屬性或條件陳述式的值來顯示或隱藏控制項。 您也可以藉由將控制項訂閱至 [ControlEvent](control-events.md)來顯示或隱藏控制項。 在 [屬性] 資料行中輸入屬性的識別碼，並在 [EventMapping 資料表](eventmapping-table.md)的事件資料行中輸入事件的識別碼。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



