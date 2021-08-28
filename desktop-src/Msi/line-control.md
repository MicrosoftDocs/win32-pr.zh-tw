---
description: 線條控制項是水平線條。
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: 線條控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4dc02db9c701c0c5156a0e3f3e15a039893bae290fc7e8bee7dfce64f2eb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763488"
---
# <a name="line-control"></a>線條控制項

線條控制項是水平線條。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                       | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [位置](position-control-attribute.md) |                                  | 對話方塊中控制項的位置。 將控制項左上角的寬度、高度和 Y 座標，輸入控制項 [資料表](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                         |
| [Visible](visible-control-attribute.md)   | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 請在 [control table](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md) 中的 Attributes 資料行的位字組中包含這個位，讓控制項在建立時可見或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/> |
| [沉沒](sunken-control-attribute.md)     | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從靜態類別建立這個控制項。 它有 **ss \_ ETCHEDHORZ** 和 **ss 的 \_ 凹陷** 樣式。

 

 
