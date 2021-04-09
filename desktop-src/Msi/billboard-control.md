---
description: 佈告欄控制項顯示常用的控制項，這些控制項是透過控制項來加入和移除對話方塊中。
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: 佈告欄控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848956"
---
# <a name="billboard-control"></a>佈告欄控制項

佈告欄控制項顯示常用的控制項，這些控制項是透過控制項來加入和移除對話方塊中。 只有未與屬性相關聯的控制項（例如 [文字](text-control.md)、 [點陣圖](bitmap-control.md)或 [圖示](icon-control.md)）或自訂控制項才能放置在佈告欄上。 佈告欄控制項通常會顯示進度訊息。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與佈告欄控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                 | 十六進位位                  | Description                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BillboardName](billboardname-control-attribute.md) |                                  | 目前佈告欄的名稱。 在 [BBControl 資料表](bbcontrol-table.md)的 [佈告欄] 資料行中輸入佈告欄的識別碼。<br/>                                                                                                                                                                            |
| [位置](position-control-attribute.md)           |                                  | 對話方塊中的控制項位置。 將控制項左上角的控制項寬度、高度和座標，輸入至 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [BBControl 資料表](bbcontrol-table.md) 的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。<br/> 使用 [ControlCondition 資料表](controlcondition-table.md)隱藏或顯示控制項。<br/> |
| [沉沒](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體、外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                               |



 

## <a name="remarks"></a>備註

此控制項沒有自己的視窗。

出現在完整使用者介面中的佈告欄控制項會列在 [佈告欄資料表](billboard-table.md)中。

位於佈告欄的控制項必須列在 [BBControl 資料表](bbcontrol-table.md) 中，而不是 [控制資料表](control-table.md)中。

 

 




