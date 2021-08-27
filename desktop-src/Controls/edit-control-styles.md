---
title: '編輯控制項樣式 (Winuser .h) '
description: 若要使用 CreateWindow 或 CreateWindowEx 函數來建立編輯控制項，請指定編輯類別、適當的視窗樣式常數，以及下列編輯控制項樣式的組合。
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 5e1a62dba617f73efdec992f843856d80a5b39bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468585"
---
# <a name="edit-control-styles"></a>編輯控制項樣式

若要使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數來建立編輯控制項，請指定編輯類別、適當的視窗樣式常數，以及下列編輯控制項樣式的組合。 建立控制項之後，除非有注明，否則無法修改這些樣式。

## <a name="example"></a>範例

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

GitHub 上[Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c)的範例。

## <a name="constants"></a>常數


| 常數 | 描述 | 
|----------|-------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl><dt><strong>ES_AUTOHSCROLL</strong></dt></dl> | 當使用者在行尾輸入字元時，會自動將文字向右滾動10個字元。 當使用者按下 ENTER 鍵時，控制項會將所有文字滾動回零的位置。<br /> | 
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl><dt><strong>ES_AUTOVSCROLL</strong></dt></dl> | 當使用者按下最後一行的 ENTER 鍵時，自動將文字向上滾動一個頁面。<br /> | 
| <span id="ES_CENTER"></span><span id="es_center"></span><dl><dt><strong>ES_CENTER</strong></dt></dl> | 在單行或多行編輯控制項中將文字置中。<br /> | 
| <span id="ES_LEFT"></span><span id="es_left"></span><dl><dt><strong>ES_LEFT</strong></dt></dl> | 將文字對齊左邊界。<br /> | 
| <span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl><dt><strong>ES_LOWERCASE</strong></dt></dl> | 將所有字元轉換成小寫，因為它們是在編輯控制項中輸入的。<br /> 若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。<br /> | 
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl><dt><strong>ES_MULTILINE</strong></dt></dl> | 指定多行編輯控制項。 預設值為單行編輯控制項。 <br /> 當多行編輯控制項在對話方塊中，按下 ENTER 鍵的預設回應是啟用預設按鈕。 若要使用 ENTER 鍵作為回車，請使用 <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> 樣式。<br /> 當多行編輯控制項不在對話方塊中並指定 <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> 樣式時，編輯控制項會盡可能顯示最多行數，並在使用者按下 ENTER 鍵時垂直捲動。 如果您未指定 <strong>ES_AUTOVSCROLL</strong>，則編輯控制項會盡可能顯示最多行數，並在沒有其他行可顯示時，于使用者按下 ENTER 鍵時發出嗶聲。<br /> 如果您指定 <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> 樣式，當插入號超過控制項的右邊緣時，多行編輯控制項會自動水準滾動。 若要開始新的一行，使用者必須按 ENTER 鍵。 如果您未指定 <strong>ES_AUTOHSCROLL</strong>，控制項會在必要時自動將文字換行到下一行的開頭。 如果使用者按下 ENTER 鍵，也會啟動新的一行。 視窗大小會決定 Wordwrap 的位置。 如果視窗大小變更，Wordwrapping 位置會變更，並重新顯示文字。<br /> 多行編輯控制項可以有捲軸。 具有捲軸的編輯控制項會處理自己的捲軸訊息。 請注意，不含捲軸的編輯控制項會依照上一段所述的方式進行滾動，並處理父視窗所傳送的任何捲軸訊息。<br /> | 
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl><dt><strong>ES_NOHIDESEL</strong></dt></dl> | 對編輯控制項的預設行為否定。 當控制項失去輸入焦點時，預設行為會隱藏選取範圍，並在控制項收到輸入焦點時反轉選取範圍。 如果您指定 <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>，即使控制項沒有焦點，也會反轉選取的文字。<br /> | 
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl><dt><strong>ES_NUMBER</strong></dt></dl> | 只允許在編輯控制項中輸入數位。 請注意，即使使用這個集合，仍然可以在編輯控制項中貼上非數位。 <br /> 若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。<br /> 若要將輸入的文字轉譯為整數值，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> 函數。 若要將編輯控制項的文字設定為指定之整數的字串表示，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> 函數。<br /> | 
| <span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl><dt><strong>ES_OEMCONVERT</strong></dt></dl> | 轉換在編輯控制項中輸入的文字。 文字會從 Windows 字元集轉換成 OEM 字元集，然後再轉換回 Windows 字元集。 這可確保當應用程式呼叫<a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a>函式將編輯控制項中的 Windows 字串轉換為 OEM 字元時，會進行適當的字元轉換。 如果編輯控制項包含的檔案名將會用於不支援 Unicode 的檔案系統，此樣式最適合用。 <br /> 若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。 <br /> | 
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl><dt><strong>ES_PASSWORD</strong></dt></dl> | 針對輸入編輯控制項的每個字元，顯示星號 ( * ) 。 這個樣式只對單行編輯控制項有效。 <br /> 若要變更顯示的字元，或設定或清除此樣式，請使用 <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> 的訊息。 <br /><blockquote>[!Note]<br />若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</blockquote><br /> | 
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl><dt><strong>ES_READONLY</strong></dt></dl> | 防止使用者輸入或編輯編輯控制項中的文字。<br /> 若要在建立控制項之後變更這個樣式，請使用 <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> 訊息。 <br /> | 
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl><dt><strong>ES_RIGHT</strong></dt></dl> | 在單行或多行編輯控制項中靠右對齊文字。<br /> | 
| <span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl><dt><strong>ES_UPPERCASE</strong></dt></dl> | 將所有字元轉換成大寫，因為它們是在編輯控制項中輸入的。 <br /> 若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。<br /> | 
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl><dt><strong>ES_WANTRETURN</strong></dt></dl> | 指定當使用者在對話方塊中輸入文字至多行編輯控制項時按下 ENTER 鍵時，要插入的回車。 如果您未指定此樣式，按下 ENTER 鍵的效果與按下對話方塊的預設推送按鈕相同。 這個樣式不會影響單行編輯控制項。 <br /> 若要在建立控制項之後變更這個樣式，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>。<br /> | 




## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winuser。h</dt> </dl> |



