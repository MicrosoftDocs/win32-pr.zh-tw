---
description: 點陣圖控制項會顯示點陣圖或 JPEG 靜態圖片檔案。 Windows Installer 會自動判斷二進位資料的格式，並顯示圖片。 控制項不支援動畫。
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: 點陣圖控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058b67d52266906735719976bf7311b4f562b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977287"
---
# <a name="bitmap-control"></a>點陣圖控制項

點陣圖控制項會顯示點陣圖或 JPEG 靜態圖片檔案。 Windows Installer 會自動判斷二進位資料的格式，並顯示圖片。 控制項不支援動畫。

**Windows 8 和 Windows Server 2012：** 影像檔案可以是 Windows 影像處理元件 (WIC) 所支援的任何標準格式，包括 TIFF、JPEG、PNG、GIF、BMP 和 HDPhoto。 控制項不支援動畫。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                 | 十六進位位                  | Description                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [位置](position-control-attribute.md)           |                                  | 對話方塊中控制項的位置。 將控制項左上角的寬度、高度和 Y 座標，輸入控制項 [資料表](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | 包含 [二進位資料表](binary-table.md)中所儲存之點陣圖的名稱。 若要顯示二進位資料表中所儲存的點陣圖，請執行下列動作。 輸入在二進位資料表的 [名稱] 資料行中顯示之點陣圖影像的名稱，放在此控制項的 [ [控制資料表](control-table.md) 記錄] 的 [文字] 資料行中。 <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制項資料表](control-table.md) 或 [BBControl 表](bbcontrol-table.md)的 [屬性] 資料行的位字中包含此位。在建立控制項時，讓控制項成為可見或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/> |
| [沉沒](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                   |
| [FixedSize 控制項](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | 伸展點陣圖影像以容納控制項。 裁剪或置入控制項中的點陣圖影像。<br/> 在 [BBControl 資料表](bbcontrol-table.md) 或 [控制資料表](control-table.md)的 [屬性] 資料行的位字組中包含此位。<br/>                                                                                                       |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從靜態類別建立這個控制項。 它有 **ss \_ BITMAP**、 **ss \_ CENTERIMAGE**、 **ws \_ CHILD** 和 **ws \_ GROUP** 樣式。

 

