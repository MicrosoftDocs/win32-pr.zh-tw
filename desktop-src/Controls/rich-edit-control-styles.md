---
title: 'Rich Edit 控制項樣式 (Winuser .h) '
description: 下列視窗樣式對 rich edit 控制項而言是唯一的。
ms.assetid: 0f1b3e01-01cb-4b3e-b959-6f32498f0394
topic_type:
- apiref
api_name:
- ES_DISABLENOSCROLL
- ES_EX_NOCALLOLEINIT
- ES_NOIME
- ES_NOOLEDRAGDROP
- ES_SAVESEL
- ES_SELECTIONBAR
- ES_SELFIME
- ES_SUNKEN
- ES_VERTICAL
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc88ea2c3c5d32dff9920b2699474a810f29b14dcf50d9b4c2401863c875778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169088"
---
# <a name="rich-edit-control-styles"></a>Rich Edit 控制項樣式

下列視窗樣式對 rich edit 控制項而言是唯一的。



| 常數                                                                                                                                                                         | 描述                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**ES \_ DISABLENOSCROLL**</dt> </dl>     | 停用捲軸，而不是在不需要時隱藏捲軸。<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ EX \_ NOCALLOLEINIT**</dt> </dl> | 防止控制項在建立時呼叫 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) 函數。 這個視窗樣式只適用于對話方塊範本，因為 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 不接受這個樣式。<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**ES \_NOIME**</dt> </dl>                                | 停用 IME 運算。 此樣式僅適用于亞洲語言支援。<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**ES \_ NOOLEDRAGDROP**</dt> </dl>           | 停用拖放 OLE 物件的支援。<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**ES \_ SAVESEL**</dt> </dl>                             | 當控制項失去焦點時，保留選取專案。 根據預設，當重新獲得焦點時，會選取控制項的整個內容。<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**ES \_ SELECTIONBAR**</dt> </dl>              | 將空格加入左邊界，其中游標會變成向右箭號，讓使用者可以選取整行文字。 <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**ES \_SELFIME**</dt> </dl>                          | 指示 rich edit 控制項，以允許應用程式處理所有的 IME 作業。 此樣式僅適用于亞洲語言支援。<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES \_ 凹陷**</dt> </dl>                                | 顯示具有凹陷框線樣式的控制項，讓 rich edit 控制項以凹陷顯示于其父視窗中。 <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**ES \_ 垂直**</dt> </dl>                          | 以垂直方向繪製文字和物件。 此樣式僅適用于亞洲語言支援。<br/>                                                                                                                                 |



Rich edit 控制項也支援下列編輯控制項樣式。



| 常數                                                                                                                                                         | 描述                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**ES \_ AUTOHSCROLL**</dt> </dl> | 當使用者在行尾輸入字元時，會自動將文字向右滾動10個字元。 當使用者按下 ENTER 鍵時，控制項會將所有文字滾動回零的位置。<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**ES \_ AUTOVSCROLL**</dt> </dl> | 當使用者按下最後一行的 ENTER 鍵時，自動將文字向上滾動一個頁面。<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**ES \_ 中心**</dt> </dl>                | 在單行或多行編輯控制項中將文字置中。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**剩餘的 ES \_**</dt> </dl>                      | 靠左對齊文字。<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ 多行**</dt> </dl>       | 指定多行編輯控制項。 預設值為單行編輯控制項。<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**ES \_ NOHIDESEL**</dt> </dl>       | 對編輯控制項的預設行為否定。 當控制項失去輸入焦點時，預設行為會隱藏選取範圍，並在控制項收到輸入焦點時反轉選取範圍。 如果您指定 [**ES \_ NOHIDESEL**](edit-control-styles.md)，則即使控制項沒有焦點，也會反轉選取的文字。<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**ES \_ 號碼**</dt> </dl>                | 只允許在編輯控制項中輸入數位。<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**ES \_ 密碼**</dt> </dl>          | \*針對輸入編輯控制項的每個字元，顯示星號 () 。 這個樣式只對單行編輯控制項有效。<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ READONLY**</dt> </dl>          | 防止使用者輸入或編輯編輯控制項中的文字。<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ RIGHT**</dt> </dl>                   | 靠右對齊單行或多行編輯控制項中的文字。<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**ES \_ WANTRETURN**</dt> </dl>    | 指定當使用者在對話方塊中輸入文字至多行編輯控制項時按下 ENTER 鍵時，要插入的回車。 如果您未指定此樣式，按下 ENTER 鍵的效果與按下對話方塊的預設推送按鈕相同。 這個樣式不會影響單行編輯控制項。<br/>                   |



Rich edit 控制項不支援下列編輯控制項樣式。

-   [**ES \_ 小寫**](edit-control-styles.md)
-   [**ES \_ OEMCONVERT**](edit-control-styles.md)
-   [**ES \_ 大寫**](edit-control-styles.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winuser。h</dt> </dl> |



 

