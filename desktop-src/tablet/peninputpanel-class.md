---
description: PenInputPanel 物件可讓您輕鬆地將就地畫筆輸入新增至您的應用程式。
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: 'PenInputPanel 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975329"
---
# <a name="peninputpanel-class"></a>PenInputPanel 類別

\[廢棄。 **PenInputPanel** 已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。\]

**PenInputPanel** 物件可讓您輕鬆地將就地畫筆輸入新增至您的應用程式。

**PenInputPanel** 物件是以可附加的物件形式提供，可讓您將 Tablet PC 輸入面板功能新增至現有的控制項。 使用者介面大多是由目前的輸入語言所規定。 您可以選擇 **PenInputPanel** 物件的預設輸入方法，也就是手寫或鍵盤。 終端使用者可以使用使用者介面上的按鈕，在輸入方法之間切換。

**PenInputPanel** 具有下列類型的成員：

-   [列舉](#enumerations)
-   [事件](#events)
-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="enumerations"></a>列舉

**PenInputPanel** 類別具有這些列舉。



| 列舉型別                    | 描述                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | 定義 **PenInputPanel** 物件中目前可用的輸入類型。<br/> |



 

### <a name="events"></a>事件

**PenInputPanel** 類別具有這些事件。



| 事件                                                  | 描述                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | 在 **PenInputPanel** 物件能夠將使用者輸入插入附加控制項之前變更輸入焦點時發生。<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | 在 **PenInputPanel** 物件于配置之間變更時發生。<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | 在 **PenInputPanel** 物件移動時發生。<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | 在 **PenInputPanel** 物件顯示或隱藏本身時發生。<br/>                                                         |



 

### <a name="interfaces"></a>介面

**PenInputPanel** 類別會定義這些介面。



| 介面          | 描述                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | 這個物件會實 **IPenInputPanel** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**PenInputPanel** 類別有這些方法。



| 方法                                                         | 描述                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | 將收集的筆墨傳送至辨識器，並張貼辨識結果。<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | 當傳遞 **TRUE** 時， **PenInputPanel** 會嘗試透過文字服務架構 (TSF) ，將文字傳送至附加的控制項，並允許使用更正使用者介面。<br/>    |
| [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | 將 **PenInputPanel** 物件的位置設定為靜態螢幕位置。<br/>                                                                                                               |
| [**重新整理**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | 根據 Tablet PC 輸入面板設定來更新和還原 **PenInputPanel** 內容、自動放置畫筆輸入面板，以及將使用者介面設定為預設面板。<br/> |



 

### <a name="properties"></a>屬性

**PenInputPanel** 類別具有這些屬性。



| 屬性                                                                  | 存取類型           | Description                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | 讀取/寫入<br/> | 取得或設定 **PenInputPanel** 物件所附加之控制項的視窗控制碼。<br/>                                                                     |
| [**自動**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | 讀取/寫入<br/> | 取得或設定布林值，這個值會指定當使用畫筆設定焦點時，是否要顯示 **PenInputPanel** 物件。<br/>                                           |
| [**忙**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | 唯讀<br/>  | 取得布林值，這個值會指定 **PenInputPanel** 物件目前是否正在處理筆墨。<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | 讀取/寫入<br/> | 取得或設定目前在 **PenInputPanel** 物件內用於輸入的面板類型。<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | 讀取/寫入<br/> | 取得或設定哪一個面板類型是在 **PenInputPanel** 物件內用於輸入的預設面板類型。<br/>                                                         |
| [**標記**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | 讀取/寫入<br/> | 取得或設定用於辨識的模擬程式字串名稱。<br/>                                                                                                    |
| [**高度**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | 唯讀<br/>  | 取得 **PenInputPanel** 物件在用戶端座標中的高度。<br/>                                                                                              |
| [**System.windows.controls.primitives.popup.horizontaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | 讀取/寫入<br/> | 取得或設定 **PenInputPanel** 物件的左邊緣與其附加之控制項的左邊緣之間的位移。<br/>                             |
| [**離開**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | 唯讀<br/>  | 取得 **PenInputPanel** 物件左邊緣的水準或 X 軸位置（以螢幕座標為單位）。<br/>                                                   |
| [**返回頁首**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | 唯讀<br/>  | 取得 **PenInputPanel** 物件上邊緣的垂直軸（或 y 軸）位置（以螢幕座標為單位）。<br/>                                                      |
| [**System.windows.controls.primitives.popup.verticaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | 讀取/寫入<br/> | 取得或設定 **PenInputPanel** 物件的最接近水準邊緣與其附加之控制項最接近水準邊緣之間的位移。<br/> |
| [**可見**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | 讀取/寫入<br/> | 取得或設定值，這個值會指出是否可以看到 **PenInputPanel** 物件。<br/>                                                                                |
| [**寬度**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | 唯讀<br/>  | 取得用戶端座標中 **PenInputPanel** 物件的寬度。<br/>                                                                                               |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PenInputPanel 類別來設計輸入面板](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
