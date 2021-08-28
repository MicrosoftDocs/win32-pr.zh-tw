---
description: 超連結控制項會顯示位址的 HTML 連結，此連結會在電腦的預設瀏覽器中開啟。
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: 超連結控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce515b64a518012ea187eb2c3a933e653b1ea5cf99b316028f9cfe3b397c5f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129458"
---
# <a name="hyperlink-control"></a>超連結控制項

超連結控制項會顯示位址的 HTML 連結，此連結會在電腦的預設瀏覽器中開啟。 HTML 以外的通訊協定不支援連結。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個控制項。

超連結控制項的文字值會使用錨點 <a> 標記和 HREF 屬性值來指定連結的 URL 和顯示的文字。

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與 Hyperlink 控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                             | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [位置](position-control-attribute.md)       |                                  | 對話方塊中的控制項位置。 將控制項左上角的寬度、高度和 Y 座標，輸入控制項 [資料表](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | 控制項所顯示的文字。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&style}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。 此文字值也會將 \[ 屬性解析 \] 為參考的屬性。 <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制項資料表](control-table.md) 或 [BBControl 表](bbcontrol-table.md)的 [屬性] 資料行的位字中包含此位。在建立控制項時，讓控制項成為可見或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                                                                                                           |
| [Enabled](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md) 的 [屬性] 資料行中的位字組中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>                                                                                                                        |
| [沉沒](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體、外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                                                                                                                                            |
| [透明](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | 不透明的控制項。 透過控制項顯示背景。 控制項具有 WS \_ EX \_ 透明樣式。<br/> 在 [控制項](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 [屬性] 資料行中包含此位。<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>備註

您可以使用 CreateWindowEx 函數，從 WC \_ 連結類別建立這個控制項[](/windows/win32/api/winuser/nf-winuser-createwindowexa) 。 它具有 WS \_ 子系、ws \_ TABSTOP 和 ws \_ GROUP 樣式。

請勿將透明 [文字控制項](text-control.md) 放在彩色點陣圖上方。 如果使用者變更顯示色彩配置，可能看不到文字。 例如，如果使用者針對協助工具原因設定高對比參數，文字可能會變成隱藏。

如果控制項中的文字長度超過控制項寬度，則文字會換行或截斷，取決於高度是否足以容納換行文字。

 

 
