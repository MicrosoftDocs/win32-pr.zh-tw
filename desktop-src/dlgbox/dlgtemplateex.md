---
title: DLGTEMPLATEEX 結構
description: 擴充的對話方塊範本以描述對話方塊的 DLGTEMPLATEEX 標頭開頭，並在對話方塊中指定控制項數目。
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- DLGTEMPLATEEX 結構對話方塊
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab23b93a72edb2da6784797dd47bdfb4a839e2e9ce662adfc6ffbe09e468ac17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503449"
---
# <a name="dlgtemplateex-structure"></a>DLGTEMPLATEEX 結構

擴充的對話方塊範本以描述對話方塊的 **DLGTEMPLATEEX** 標頭開頭，並在對話方塊中指定控制項數目。 針對對話方塊中的每個控制項，擴充的對話方塊範本都有一個使用 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 格式來描述控制項的資料區塊。

**DLGTEMPLATEEX** 結構未定義于任何標準標頭檔中。 此處提供結構定義，以說明對話方塊的延伸範本格式。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a>成員

<dl> <dt>

**dlgVer**
</dt> <dd>

類型： **WORD**

</dd> <dd>

延伸對話方塊範本的版本號碼。 此成員必須設定為1。

</dd> <dt>

**簽章**
</dt> <dd>

類型： **WORD**

</dd> <dd>

指出範本是否為擴充的對話方塊範本。 如果 **signature** 是0xffff，這就是延伸的對話方塊範本。 在此情況下， **dlgVer** 成員會指定範本版本號碼。 如果 **signature** 是0xffff 以外的任何值，則這是使用 [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) 和 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構的標準對話方塊範本。

</dd> <dt>

**h**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

對話方塊視窗的說明內容識別碼。 當系統傳送 WM 說明 [**訊息 \_**](../shell/wm-help.md)時，它會在 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的 **wCoNtextId** 成員中傳遞此值。

</dd> <dt>

**exStyle**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

擴充的 windows 樣式。 建立對話方塊時不會使用這個成員，但是使用對話方塊範本的應用程式可以使用它來建立其他類型的視窗。 如需值清單，請參閱 [**擴充的視窗樣式**](/windows/desktop/winmsg/extended-window-styles)。

</dd> <dt>

**style**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

對話方塊的樣式。 這個成員可以是 [視窗樣式值](/windows/desktop/winmsg/window-styles) 和 [對話方塊樣式值](dialog-box-styles.md)的組合。

如果 [ **樣式** ] 包含 [ **ds \_ SETFONT** ] 或 [ **ds \_ SHELLFONT** ] 對話方塊樣式，則延伸對話方塊範本的 **DLGTEMPLATEEX** 標頭會包含四個額外的成員 ( [ **dialog**]、[ **權數**]、[ **斜體**] 和 [ **字型** ]) ，其中描述要用於工作區中的文字和對話方塊控制項的字型。 可能的話，系統會根據這些成員中指定的值來建立字型。 然後系統會將 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息傳送至對話方塊，並傳送至每個控制項，以提供字型的控制碼。

如需詳細資訊，請參閱 [對話方塊](about-dialog-boxes.md)字型。

</dd> <dt>

**cDlgItems**
</dt> <dd>

類型： **WORD**

</dd> <dd>

對話方塊中的控制項數目。

</dd> <dt>

**x**
</dt> <dd>

類型： **short**

</dd> <dd>

對話方塊左上角的 x 座標（以對話方塊單位為單位）。

</dd> <dt>

**y**
</dt> <dd>

類型： **short**

</dd> <dd>

對話方塊左上角的 y 座標（以對話方塊單位為單位）。

</dd> <dt>

**殘雪**
</dt> <dd>

類型： **short**

</dd> <dd>

對話方塊的寬度（以對話方塊單位）。

</dd> <dt>

**cy**
</dt> <dd>

類型： **short**

</dd> <dd>

對話方塊的高度（以對話方塊單位）。

</dd> <dt>

**功能表**
</dt> <dd>

類型： **sz \_ 或 \_ Ord**

</dd> <dd>

變數長度的16位元素陣列，識別對話方塊的功能表資源。 如果這個陣列的第一個元素是0x0000，則對話方塊沒有功能表，且陣列沒有其他元素。 如果第一個元素是0xFFFF，陣列有一個額外的元素，可在可執行檔中指定功能表資源的序數值。 如果第一個元素有任何其他值，系統會將陣列視為以 null 終止的 Unicode 字串，在可執行檔中指定功能表資源的名稱。

</dd> <dt>

**windowClass**
</dt> <dd>

類型： **sz \_ 或 \_ Ord**

</dd> <dd>

變數長度的16位元素陣列，識別對話方塊的視窗類別。 如果陣列的第一個元素是0x0000，系統就會使用對話方塊的預先定義對話方塊類別，而陣列沒有其他元素。 如果第一個元素是0xFFFF，陣列有一個額外的元素，可指定預先定義之系統視窗類別的序數值。 如果第一個元素有任何其他值，系統會將陣列視為以 null 終止的 Unicode 字串，以指定已註冊視窗類別的名稱。

</dd> <dt>

**title**
</dt> <dd>

類型： **WCHAR \[ titleLen \]**

</dd> <dd>

對話方塊的標題。 如果這個陣列的第一個元素是0x0000，則對話方塊沒有標題，而且陣列沒有其他元素。

</dd> <dt>

**dialog**
</dt> <dd>

類型： **WORD**

</dd> <dd>

要用於對話方塊和其控制項中文字的字型點大小。

只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。

</dd> <dt>

**weight**
</dt> <dd>

類型： **WORD**

</dd> <dd>

字型的粗細。 請注意，雖然這可以是 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfWeight** 成員所列出的任何值，但使用的任何值都會自動變更為 **FW \_ NORMAL**。

只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。

</dd> <dt>

**斜體**
</dt> <dd>

類型： **位元組**

</dd> <dd>

指出字型是否為斜體。 如果這個值為 **TRUE**，表示字型為斜體。

只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。

</dd> <dt>

**字元集**
</dt> <dd>

類型： **位元組**

</dd> <dd>

要使用的字元集。 如需詳細資訊，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)的 **lfcharset** 成員。

只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。

</dd> <dt>

**字體**
</dt> <dd>

類型： **WCHAR \[ stringLen \]**

</dd> <dd>

字型的字型名稱。

只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用擴充的對話方塊範本，而不是 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)、 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)、 [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)和 [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) 函數中的標準對話方塊範本。

在擴充對話方塊範本中的 **DLGTEMPLATEEX** 標頭之後，就是一或多個描述對話方塊控制項的 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 結構。 **DLGITEMTEMPLATEEX** 結構的 **cDlgItems** 成員會指定範本中遵循的 **DLGITEMTEMPLATEEX** 結構數目。

範本中的每個 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 結構都必須對齊 **DWORD** 界限。 如果 **樣式** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 樣式，則第一個 **DLGITEMTEMPLATEEX** 結構會在 **字型** 字串之後的第一個 **DWORD** 界限上開始。 如果未指定這些樣式，則第一個結構會在 **標題** 字串之後的第一個 **DWORD** 界限上開始。

**Menu**、 **windowClass**、 **title** 和 **字樣** 陣列必須對齊 **字** 組邊界。

如果您在 **功能表**、 **windowClass**、 **title** 和 **字樣** 陣列中指定字元字串，就必須使用 Unicode 字串。 您可以使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函數，從 ANSI 字串產生這些 Unicode 字串。

**X**、 **y**、 **cx** 和 **cy** 成員會在對話方塊單位中指定值。 您可以使用 [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) 函式，將這些值轉換為螢幕單位 (圖元) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

