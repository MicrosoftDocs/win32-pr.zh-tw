---
title: '工具列按鈕狀態 (CommCtrl .h) '
description: 此區段會列出工具列按鈕可以有的狀態。
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998796"
---
# <a name="toolbar-button-states"></a>工具列按鈕狀態

此區段會列出工具列按鈕可以有的狀態。



| 常數                                                                                                                                                                              | 描述                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ 已核取**</dt> </dl>                   | 此按鈕具有 [**TBSTYLE \_ 檢查**](toolbar-control-and-button-styles.md) 樣式，且正在按一下。<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**TBSTATE \_ 橢圓形**</dt> </dl>                | [版本 4.70](common-control-versions.md)。 按鈕的文字會被剪下，並顯示省略號。<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ 已啟用**</dt> </dl>                   | 按鈕接受使用者輸入。 沒有此狀態的按鈕會呈現灰色。<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**\_隱藏 TBSTATE**</dt> </dl>                      | 按鈕不會顯示，且無法接收使用者輸入。<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ 不定**</dt> </dl> | 按鈕會呈現灰色。<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ 標示**</dt> </dl>                      | [版本 4.71](common-control-versions.md)。 按鈕會標示為。 標示專案的解讀取決於應用程式。 <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**已 \_ 按下 TBSTATE**</dt> </dl>                   | 正在按一下按鈕。<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**TBSTATE \_ WRAP**</dt> </dl>                            | 按鈕後面接著分行符號。 此按鈕也必須具有 TBSTATE \_ 啟用狀態。<br/>                                              |



## <a name="remarks"></a>備註

工具列可能會有狀態的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





