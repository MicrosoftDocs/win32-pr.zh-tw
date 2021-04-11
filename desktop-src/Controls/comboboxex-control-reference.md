---
title: ComboBoxEx 控制項
description: 本章節包含與 ComboBoxEx 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d5a926ccf2f9f5b5bb68e040731d6b9d8e37ee8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945863"
---
# <a name="comboboxex-control"></a>ComboBoxEx 控制項

本章節包含與 ComboBoxEx 控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                                | 目錄                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [關於 ComboBoxEx 控制項](comboboxex-controls.md) | ComboBoxEx 控制項是下拉式方塊控制項，可提供專案影像的原生支援。<br/> |
| [使用 ComboBoxEx 控制項](using-comboboxex.md)    | 本章節包含範例程式碼，以及如何使用 ComboBoxEx 控制項的相關資訊。<br/> |



 

### <a name="messages"></a>訊息



| 主題                                                   | 目錄                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | 從 ComboBoxEx 控制項中移除專案。 <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | 取得子下拉式方塊控制項的控制碼。 <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | 取得 ComboBoxEx 控制項之編輯控制項部分的控制碼。 當 ComboBoxEx 控制項設定為 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式時，會使用編輯方塊。 <br/> |
| [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) | 取得用於 ComboBoxEx 控制項的延伸樣式。 <br/>                                                                                                                             |
| [**CBEM \_ GETIMAGELIST**](cbem-getimagelist.md)         | 取得指派給 ComboBoxEx 控制項之影像清單的控制碼。 <br/>                                                                                                                             |
| [**CBEM \_ GETITEM**](cbem-getitem.md)                   | 取得指定之 ComboBoxEx 專案的專案資訊。<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | 取得控制項的 UNICODE 字元格式旗標。 <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | 判斷使用者是否已變更 ComboBoxEx 編輯控制項的文字。<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | 在 ComboBoxEx 控制項中插入新專案。 <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | 此訊息不會執行。 <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | 此訊息不會執行。 <br/>                                                                                                                                                               |
| [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) | 設定 ComboBoxEx 控制項中的延伸樣式。 <br/>                                                                                                                                              |
| [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md)         | 設定 ComboBoxEx 控制項的影像清單。 <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | 設定 ComboBoxEx 控制項中專案的屬性。 <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | 設定控制項的 UNICODE 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | 設定 ComboBoxEx 控制項的視覺化樣式。<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>通知



| 主題                                                      | 目錄                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | 當使用者啟動下拉式清單，或按一下控制項的編輯方塊時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | 在刪除專案時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                     |
| [CBEN \_ DRAGBEGIN](cben-dragbegin.md)                      | 當使用者開始拖曳顯示在控制項編輯部分的專案影像時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | 當使用者在編輯方塊內結束作業，或已從控制項下拉式清單中選取專案時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                             |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md)                  | 傳送以取得回呼專案的顯示資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | 在控制項中插入新專案時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                  |
| [NM \_ SETCURSOR (ComboBoxEx) ](nm-setcursor-comboboxex-.md) | 通知 ComboBoxEx 控制項的父視窗，控制項正在設定資料指標以回應 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |



 

### <a name="structures"></a>結構



| 主題                                    | 目錄                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | 包含 ComboBoxEx 控制項中專案的相關資訊。<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | 包含與 [CBEN \_ DRAGBEGIN](cben-dragbegin.md) 通知程式碼搭配使用的資訊。 <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | 包含 ComboBoxEx 控制項內編輯作業結論的相關資訊。 此結構會與 [CBEN \_ ENDEDIT](cben-endedit.md) 通知程式碼搭配使用。 <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | 包含 ComboBoxEx 專案特定的資訊，以用於通知碼。 <br/>                                                                                               |



 

### <a name="constants"></a>常數



| 主題                                                                        | 目錄                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [ComboBoxEx 控制項擴充樣式](comboboxex-control-extended-styles.md) | 支援本節中所列的延伸樣式，以及大部分標準的下拉式方塊控制項樣式。<br/> |



 

 

