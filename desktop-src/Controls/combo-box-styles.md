---
title: CommCtrl) 的下拉式列示方塊樣式 (
description: 若要使用 CreateWindow 或 CreateWindowEx 函式來建立下拉式方塊，請指定 COMBOBOX 類別、適當的視窗樣式常數，以及下列下拉式列示方塊樣式的組合。
ms.assetid: 4dc347b2-7da7-4aa0-b61f-781acf652d84
topic_type:
- apiref
api_name:
- CBS_AUTOHSCROLL
- CBS_DISABLENOSCROLL
- CBS_DROPDOWN
- CBS_DROPDOWNLIST
- CBS_HASSTRINGS
- CBS_LOWERCASE
- CBS_NOINTEGRALHEIGHT
- CBS_OEMCONVERT
- CBS_OWNERDRAWFIXED
- CBS_OWNERDRAWVARIABLE
- CBS_SIMPLE
- CBS_SORT
- CBS_UPPERCASE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f531b93725f3aa92778a42bae3dd3fd972534e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998800"
---
# <a name="combo-box-styles"></a>下拉式列示方塊樣式

若要使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立下拉式方塊，請指定 COMBOBOX 類別、適當的視窗樣式常數，以及下列下拉式列示方塊樣式的組合。



| 常數                                                                                                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**CBS \_ AUTOHSCROLL**</dt> </dl>                   | 當使用者在行尾輸入字元時，會自動將編輯控制項中的文字向右滾動。 如果未設定此樣式，則只會允許符合矩形界限的文字。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**CBS \_ DISABLENOSCROLL**</dt> </dl>       | 當方塊沒有包含足夠的專案可滾動時，在清單方塊中顯示已停用的垂直捲動條。 若沒有這個樣式，在清單方塊中未包含足夠的項目時，捲軸會隱藏。<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**CBS \_ 下拉式清單**</dt> </dl>                            | 類似于 CBS \_ SIMPLE，不同之處在于除非使用者選取編輯控制項旁的圖示，否則不會顯示清單方塊。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**CBS \_ DROPDOWNLIST**</dt> </dl>                | 類似于 CBS \_ 下拉式清單，不同之處在于編輯控制項會由顯示清單方塊中目前選取範圍的靜態文字專案所取代。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**CBS \_ HASSTRINGS**</dt> </dl>                      | 指定主控描繪的下拉式列示方塊包含字串所組成的專案。 下拉式方塊會維護字串的記憶體和位址，讓應用程式可以使用 [**CB \_ GETLBTEXT**](cb-getlbtext.md) 訊息來取得特定專案的文字。<br/> 針對協助工具問題，請參閱 [公開 Owner-Drawn 下拉式方塊專案](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**CBS \_ 小寫**</dt> </dl>                         | 將選取欄位和清單中的所有文字轉換成小寫。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**CBS \_ NOINTEGRALHEIGHT**</dt> </dl>    | 指定下拉式方塊的大小與應用程式建立下拉式方塊時所指定的大小完全相同。 一般來說，系統會調整下拉式方塊的大小，使其不會顯示部分專案。<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**CBS \_ OEMCONVERT**</dt> </dl>                      | 將下拉式方塊編輯控制項中輸入的文字，從 Windows 字元集轉換為 OEM 字元集，然後再轉換回 Windows 字元集。 這可確保當應用程式呼叫 [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) 函式將下拉式方塊中的 Windows 字串轉換成 OEM 字元時，會進行適當的字元轉換。 這個樣式最適合用於包含檔案名的下拉式方塊，而且只適用于以 CBS \_ SIMPLE 或 CBS 下拉式樣式建立的下拉式方塊 \_ 。<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**CBS \_ OWNERDRAWFIXED**</dt> </dl>          | 指定清單方塊的擁有者會負責繪製其內容，而且清單方塊中的專案全都具有相同的高度。 當下拉式方塊建立時，擁有者視窗會收到 [**wm \_ MEASUREITEM**](wm-measureitem.md) 訊息，而下拉式方塊的視覺外觀已變更時，則為 [**wm \_ DRAWITEM**](wm-drawitem.md) 訊息。<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**CBS \_ OWNERDRAWVARIABLE**</dt> </dl> | 指定清單方塊的擁有者會負責繪製其內容，而且清單方塊中的專案會高度為變數。 當您在下拉式方塊的視覺外觀已變更時，當您建立下拉式方塊和 [**wm \_ DRAWITEM**](wm-drawitem.md)訊息時，擁有者視窗會針對下拉式方塊中的每個專案收到 [**wm \_ MEASUREITEM**](wm-measureitem.md)訊息。<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ 簡單**</dt> </dl>                                  | 隨時顯示清單方塊。 編輯控制項會顯示清單方塊中目前的選取範圍。<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**CBS \_ 排序**</dt> </dl>                                        | 自動排序新增至清單方塊的字串。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**CBS \_ 大寫**</dt> </dl>                         | 將選取欄位和清單中的所有文字轉換成大寫。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

