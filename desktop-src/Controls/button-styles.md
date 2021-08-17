---
title: '按鈕樣式 (Winuser .h) '
description: 指定按鈕樣式的組合。 如果您使用 BUTTON 類別和 CreateWindow 或 CreateWindowEx 函式來建立按鈕，則可以指定下列任何按鈕樣式。
ms.assetid: 30254cb5-43cd-407f-8ad6-bd7f9ec3edc7
topic_type:
- apiref
api_name:
- BS_3STATE
- BS_AUTO3STATE
- BS_AUTOCHECKBOX
- BS_AUTORADIOBUTTON
- BS_BITMAP
- BS_BOTTOM
- BS_CENTER
- BS_CHECKBOX
- BS_COMMANDLINK
- BS_DEFCOMMANDLINK
- BS_DEFPUSHBUTTON
- BS_DEFSPLITBUTTON
- BS_GROUPBOX
- BS_ICON
- BS_FLAT
- BS_LEFT
- BS_LEFTTEXT
- BS_MULTILINE
- BS_NOTIFY
- BS_OWNERDRAW
- BS_PUSHBUTTON
- BS_PUSHLIKE
- BS_RADIOBUTTON
- BS_RIGHT
- BS_RIGHTBUTTON
- BS_SPLITBUTTON
- BS_TEXT
- BS_TOP
- BS_TYPEMASK
- BS_USERBUTTON
- BS_VCENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 60419d947036516e093d481f3fc0d8caa097671c13bd4fe3fc8e95d21cc3cb83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832478"
---
# <a name="button-styles"></a>按鈕樣式

指定按鈕樣式的組合。 如果您使用 BUTTON 類別和 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立按鈕，則可以指定下列任何按鈕樣式。

## <a name="example"></a>範例

```cpp
HRESULT Button::CreateText(HWND hParent, const TCHAR *szCaption, int nID, 
                               const Rect& rcBound)
{
    CREATESTRUCT create;
    ZeroMemory(&create, sizeof(CREATESTRUCT));

    create.x = rcBound.left;
    create.y = rcBound.top;
    create.cx = rcBound.right - create.x;
    create.cy = rcBound.bottom - create.y;

    create.hwndParent = hParent;
    create.lpszName = szCaption;
    create.hMenu = (HMENU)(INT_PTR)nID;
    create.lpszClass = TEXT("BUTTON");
    create.style = BS_PUSHBUTTON | BS_FLAT;
    return Control::Create(create);
}
```
GitHub 上[Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp)的範例。


## <a name="constants"></a>常數
| 常數                                                                                                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**BS \_ 3STATE**</dt> </dl>                            | 建立與核取方塊相同的按鈕，不同之處在于方塊可以變成灰色，也可以選取或清除。 使用灰色狀態，顯示未判斷核取方塊的狀態。<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**BS \_ AUTO3STATE**</dt> </dl>                | 建立按鈕，此按鈕與三個狀態的核取方塊相同，不同之處在于方塊會在使用者選取時變更其狀態。 狀態迴圈會透過 checked、不定和清除。<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**BS \_ AUTOCHECKBOX**</dt> </dl>          | 建立與核取方塊相同的按鈕，不同之處在于檢查狀態會在每次使用者選取核取方塊時，自動在每次選取和清除之間切換。<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**BS \_ AUTORADIOBUTTON**</dt> </dl> | 建立的按鈕與選項按鈕相同，不同之處在于當使用者選取它時，系統會自動將按鈕的檢查狀態設定為 [已選取]，並自動將相同群組中所有其他按鈕的檢查狀態設定為 [已清除]。<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**BS \_ 點陣圖**</dt> </dl>                            | 指定按鈕顯示點陣圖。 請參閱「備註」一節，以瞭解其與 BS 的互動 \_ 圖示。<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS \_ 底部**</dt> </dl>                            | 將文字放在按鈕矩形的底部。<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**BS \_ 中心**</dt> </dl>                            | 將文字水準置中按鈕矩形。<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**BS \_ 核取方塊**</dt> </dl>                      | 建立含有文字的小型空白核取方塊。 根據預設，文字會顯示于核取方塊的右邊。 若要顯示覆選框左邊的文字，請將此旗標與 BS \_ LEFTTEXT 樣式結合 (，或使用對等的 BS \_ RIGHTBUTTON 樣式) 。<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**BS \_ COMMANDLINK**</dt> </dl>             | 建立行為類似 BS 按鍵樣式按鈕的命令連結按鈕 \_ ，但 [命令連結] 按鈕的左邊會有綠色箭號，指向按鈕文字。 您可以藉由將 BCM SETNOTE 訊息傳送至按鈕，來設定按鈕文字的標題 \_ 。<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**BS \_ DEFCOMMANDLINK**</dt> </dl>    | 建立行為類似 BS 按鈕樣式按鈕的命令連結按鈕 \_ 。 如果按鈕在對話方塊中，使用者可以按 ENTER 鍵來選取命令連結按鈕，即使命令連結按鈕沒有輸入焦點也一樣。 這種樣式適用于讓使用者快速選取最有可能的 (預設) 選項。<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**BS \_ DEFPUSHBUTTON**</dt> </dl>       | 建立行為類似 BS 按鈕樣式按鈕的按鈕 \_ ，但有不同的外觀。 如果按鈕在對話方塊中，使用者可以按 ENTER 鍵來選取按鈕，即使按鈕沒有輸入焦點也一樣。 這種樣式適用于讓使用者快速選取最有可能的 (預設) 選項。<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**BS \_ DEFSPLITBUTTON**</dt> </dl>    | 建立行為類似 BS 按鈕樣式按鈕的分割按鈕 \_ ，但也有獨特的外觀。 如果 [分割] 按鈕在對話方塊中，即使分割按鈕沒有輸入焦點，使用者也可以按 ENTER 鍵來選取分割按鈕。 這種樣式適用于讓使用者快速選取最有可能的 (預設) 選項。<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**BS \_ 群組方塊**</dt> </dl>                      | 建立可將其他控制項分組的矩形。 與此樣式相關聯的任何文字都會顯示在矩形的左上角。<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**BS \_ 圖示**</dt> </dl>                                  | 指定按鈕顯示圖示。 請參閱「備註」一節，以瞭解其與 BS 點陣圖的互動 \_ 。<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ 平面**</dt> </dl>                                  | 指定按鈕為二維;它不會使用預設的陰影來建立立體影像。 <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**\_左 BS**</dt> </dl>                                  | 將按鈕矩形中的文字靠左對齊。 但是，如果按鈕是沒有 BS RIGHTBUTTON 樣式的核取方塊或選項按鈕 \_ ，則文字會靠在核取方塊或選項按鈕的右邊對齊。<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**BS \_ LEFTTEXT**</dt> </dl>                      | 將文字放在選項按鈕的左邊，或與選項按鈕或核取方塊樣式結合時的核取方塊。 與 BS \_ RIGHTBUTTON 樣式相同。<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ 多行**</dt> </dl>                   | 如果文字字串太長而無法放入按鈕矩形中的單一行，則會將按鈕文字包裝成多行。<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**BS \_ 通知**</dt> </dl>                            | 啟用按鈕以將 [BN \_ KILLFOCUS](bn-killfocus.md) 和 [BN \_ SETFOCUS](bn-setfocus.md) 通知碼傳送至其父視窗。 <br/> 請注意，按鈕會 [傳送 \_ BN](bn-clicked.md) 的已按下通知程式碼，不論它是否有此樣式。 若要取得 [BN \_ DBLCLK](bn-dblclk.md) 通知碼，按鈕必須具有 BS \_ 選項按鈕或 BS \_ OWNERDRAW 樣式。<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**BS \_ OWNERDRAW**</dt> </dl>                   | 建立擁有者繪製按鈕。 當按鈕的視覺外觀變更時，擁有者視窗會收到 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 請勿結合 BS \_ OWNERDRAW 樣式與任何其他按鈕樣式。<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**BS \_ 按鍵**</dt> </dl>                | 建立推播按鈕，此按鈕會在使用者選取按鈕時，將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息張貼至擁有者視窗。<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**BS \_ PUSHLIKE**</dt> </dl>                      | 讓按鈕 (例如核取方塊、三個狀態核取方塊或選項按鈕，) 外觀] 和 [按下] 按鈕動作。 按鈕會在未推送或未核取時引發，並在推送或核取時顯示凹陷。<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**BS \_ 選項按鈕**</dt> </dl>             | 建立含有文字的小圓圈。 根據預設，文字會顯示在圓形右邊。 若要顯示圓圈左邊的文字，請將此旗標與 BS \_ LEFTTEXT 樣式結合 (，或使用對等的 BS \_ RIGHTBUTTON 樣式) 。 針對相關但互斥選擇的群組，使用選項按鈕。<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ RIGHT**</dt> </dl>                               | 靠右對齊按鈕矩形中的文字。 但是，如果按鈕是沒有 BS RIGHTBUTTON 樣式的核取方塊或選項按鈕 \_ ，則文字會靠右對齊在核取方塊或選項按鈕的右邊。<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**BS \_ RIGHTBUTTON**</dt> </dl>             | 將選項按鈕的圓形或核取方塊的正方形放置在按鈕矩形的右邊。 與 BS \_ LEFTTEXT 樣式相同。<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_ SPLITBUTTON**</dt> </dl>             | 建立分割按鈕。 分割按鈕具有下拉式箭號。<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**BS \_ 文字**</dt> </dl>                                  | 指定按鈕會顯示文字。<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS \_ TOP**</dt> </dl>                                     | 將文字放在按鈕矩形的上方。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**BS \_ TYPEMASK**</dt> </dl>                      | 請勿使用這個樣式。 在 BS 樣式位上使用 OR 運算子所產生的複合樣式位 \_ \* 。 可以用來將 \_ \* 指定的位元遮罩中的有效 BS 位遮罩出來。 請注意，這已過期，且未正確包含所有有效的樣式。 因此，您不應該使用這個樣式。<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**BS \_ USERBUTTON**</dt> </dl>                | 已淘汰，但為了與16位版本的 Windows 的相容性而提供。 應用程式應該改為使用 BS \_ OWNERDRAW。<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ VCENTER**</dt> </dl>                         | 將文字放在按鈕矩形的中間 (垂直) 。<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>備註

如需主要按鈕樣式（例如 BS \_ 核取方塊和 BS 群組方塊）的圖例 \_ ，請參閱 [按鈕類型](button-types-and-styles.md)。

文字或圖示的外觀或按鈕控制項上的兩者都取決於 BS \_ 圖示和 BS \_ 點陣圖樣式，以及是否傳送 [**BM \_ SETIMAGE**](bm-setimage.md) 訊息。 可能的結果如下所示。



| BS \_ 圖示或 BS \_ 點陣圖集合？ | \_呼叫 BM SETIMAGE？ | 結果              |
|-----------------------------|----------------------|---------------------|
| 是                         | 是                  | 僅顯示圖示。     |
| 否                          | 是                  | 顯示圖示和文字。 |
| 是                         | 否                   | 只顯示文字。     |
| 否                          | 否                   | 只顯示文字      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winuser。h</dt> </dl> |



 

