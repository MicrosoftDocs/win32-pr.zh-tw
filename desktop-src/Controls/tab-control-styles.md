---
title: '索引標籤控制項樣式 (CommCtrl .h) '
description: 本節列出支援的索引標籤控制項樣式。
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352864fe71b5efc39529109bafb3bdc49cee68e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000776"
---
# <a name="tab-control-styles"></a>索引標籤控制項樣式

本節列出支援的索引標籤控制項樣式。



| 常數                                                                                                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TCS \_ 底部**</dt> </dl>                                  | [版本 4.70](common-control-versions.md)。 索引標籤會出現在控制項底部。 此值等於 TCS \_ RIGHT。 如果您使用 ComCtl32.dll 第6版，就不支援這個樣式。<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**TCS \_ 按鈕**</dt> </dl>                               | 索引標籤會顯示為按鈕，不會在顯示區域周圍繪製框線。<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TCS \_ FIXEDWIDTH**</dt> </dl>                      | 所有索引標籤都具有相同的寬度。 此樣式無法與 TCS \_ RIGHTJUSTIFY 樣式結合。<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**TCS \_ FLATBUTTONS**</dt> </dl>                   | [版本 4.71](common-control-versions.md)。 選取的索引標籤會顯示為縮排到背景，而其他索引標籤會顯示為與背景相同的平面。 這個樣式只會影響具有 [TCS] 按鈕樣式的索引標籤控制項 \_ 。<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**TCS \_ FOCUSNEVER**</dt> </dl>                      | 按一下時，索引標籤控制項不會收到輸入焦點。<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**TCS \_ FOCUSONBUTTONDOWN**</dt> </dl> | 按一下時，索引標籤控制項會接收輸入焦點。<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**TCS \_ FORCEICONLEFT**</dt> </dl>             | 圖示會與每個固定寬度索引標籤的左邊緣對齊。此樣式只能與 TCS FIXEDWIDTH 樣式搭配使用 \_ 。<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**TCS \_ FORCELABELLEFT**</dt> </dl>          | 標籤與每個固定寬度索引標籤的左邊緣對齊;也就是說，標籤會立即顯示在圖示的右側，而不是置中。 此樣式只能搭配 TCS \_ FIXEDWIDTH 樣式使用，並隱含 TCS \_ FORCEICONLEFT 樣式。<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**TCS \_ HOTTRACK**</dt> </dl>                            | [版本 4.70](common-control-versions.md)。 指標底下的專案會自動反白顯示。 您可以藉由呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)來檢查是否啟用熱追蹤。 <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**TCS \_ 多行**</dt> </dl>                         | 如有必要，會顯示多個索引標籤列，以便一次顯示所有索引標籤。<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS \_ 多重複選**</dt> </dl>                   | [版本 4.70](common-control-versions.md)。 按一下時按住 CTRL 鍵即可選取多個索引標籤。 此樣式必須與 TCS \_ 按鈕樣式搭配使用。<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**TCS \_ OWNERDRAWFIXED**</dt> </dl>          | 父視窗負責繪製索引標籤。<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**TCS \_ RAGGEDRIGHT**</dt> </dl>                   | 索引標籤的資料列將不會伸展以填滿整個控制項的寬度。 這是預設樣式。<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS \_ RIGHT**</dt> </dl>                                     | [版本 4.70](common-control-versions.md)。 索引標籤會以垂直方式出現在使用 TCS 垂直樣式的控制項右邊 \_ 。 此值等於 TCS \_ 底端。 如果您使用視覺化樣式，則不支援這個樣式。<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**TCS \_ RIGHTJUSTIFY**</dt> </dl>                | 必要時，會增加每個索引標籤的寬度，讓每個索引標籤的資料列填滿整個索引標籤控制項的寬度。 除非 \_ 同時指定了 TCS 多行樣式，否則會忽略此視窗樣式。<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**TCS \_ SCROLLOPPOSITE**</dt> </dl>          | [版本 4.70](common-control-versions.md)。 選取索引標籤時，不需要的索引標籤會滾動至控制項的相反邊。<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**TCS \_ 單行**</dt> </dl>                      | 只會顯示一個索引標籤的資料列。 必要時，使用者可以視需要滾動查看更多索引標籤。 這是預設樣式。<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**TCS 索引標籤 \_**</dt> </dl>                                        | 索引標籤會顯示為索引標籤，並在顯示區域周圍繪製框線。 這是預設樣式。<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**TCS \_ 工具提示**</dt> </dl>                            | 索引標籤控制項有相關聯的工具提示控制項。 <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**\_垂直 TCS**</dt> </dl>                            | [版本 4.70](common-control-versions.md)。 索引標籤會出現在控制項的左邊，並以垂直方式顯示定位字元文字。 只有搭配 TCS 多行樣式使用時，此樣式才有效 \_ 。 若要讓索引標籤顯示在控制項的右側，也可以使用 [TCS] \_ 許可權樣式。 如果您使用 ComCtl32.dll 第6版，就不支援這個樣式。<br/> |



## <a name="remarks"></a>備註

您可以在建立控制項之後修改下列樣式。

-   TCS \_ 底部
-   TCS \_ 按鈕
-   TCS \_ FIXEDWIDTH
-   TCS \_ FLATBUTTONS
-   TCS \_ FORCEICONLEFT
-   TCS \_ FORCELABELLEFT
-   TCS \_ 多行
-   TCS \_ OWNERDRAWFIXED
-   TCS \_ RAGGEDRIGHT
-   TCS \_ RIGHT
-   \_垂直 TCS

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

