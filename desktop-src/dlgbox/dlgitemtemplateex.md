---
title: DLGITEMTEMPLATEEX 結構
description: 延伸對話方塊範本用來描述延伸對話方塊的文字區塊。 如需延伸對話方塊範本格式的描述，請參閱 DLGTEMPLATEEX。
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- DLGITEMTEMPLATEEX 結構對話方塊
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad2bf1795f5059ec1fdda00ddb6a93cfe396dae5b4119d392eff42382fa978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785864"
---
# <a name="dlgitemtemplateex-structure"></a>DLGITEMTEMPLATEEX 結構

延伸對話方塊範本用來描述延伸對話方塊的文字區塊。 如需延伸對話方塊範本格式的描述，請參閱 [**DLGTEMPLATEEX**](dlgtemplateex.md)。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a>成員

<dl> <dt>

**h**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

控制項的說明內容識別碼。 當系統傳送 WM 說明 [**\_**](../shell/wm-help.md)訊息時，它會在 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的 **dwCoNtextId** 成員中傳遞 **h** 值。

</dd> <dt>

**exStyle**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

視窗的延伸樣式。 此成員不會用來在對話方塊中建立控制項，但使用對話方塊範本的應用程式可以使用它來建立其他類型的視窗。 如需值清單，請參閱 [**擴充的視窗樣式**](/windows/desktop/winmsg/extended-window-styles)。

</dd> <dt>

**style**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

控制項的樣式。 這個成員可以是 [視窗樣式值](/windows/desktop/winmsg/window-styles) 的組合 (例如 **WS \_ 框線**) ，以及一或多個 [控制項樣式值](/windows/desktop/Controls/common-control-styles) (例如 **BS \_ 按鈕** 和 **ES \_ 左方**) 。

</dd> <dt>

**x**
</dt> <dd>

類型： **short**

</dd> <dd>

控制項左上角的 x 座標（以對話方塊單位為單位）。 此座標一律相對於對話方塊工作區的左上角。

</dd> <dt>

**y**
</dt> <dd>

類型： **short**

</dd> <dd>

控制項左上角的 y 座標（以對話方塊單位為單位）。 此座標一律相對於對話方塊工作區的左上角。

</dd> <dt>

**殘雪**
</dt> <dd>

類型： **short**

</dd> <dd>

控制項的寬度（以對話方塊單位）。

</dd> <dt>

**cy**
</dt> <dd>

類型： **short**

</dd> <dd>

控制項之對話方塊單位中的高度。

</dd> <dt>

**id**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

控制項識別碼。

</dd> <dt>

**windowClass**
</dt> <dd>

類型： **sz \_ 或 \_ Ord**

</dd> <dd>

變數長度的16位元素陣列，指定控制項的視窗類別。 如果這個陣列的第一個元素是0xFFFF 以外的任何值，系統會將陣列視為以 null 終止的 Unicode 字串，以指定已註冊視窗類別的名稱。

如果第一個元素是0xFFFF，陣列有一個額外的元素，可指定預先定義之系統類別的序數值。 序數可以是下列其中一個 atom 值。



| 值                                                                             | 意義               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Button<br/>     |
| <dl> <dt>0x0081</dt> </dl> | 編輯<br/>       |
| <dl> <dt>0x0082</dt> </dl> | 靜態<br/>     |
| <dl> <dt>0x0083</dt> </dl> | 清單方塊<br/>   |
| <dl> <dt>0x0084</dt> </dl> | 捲軸<br/> |
| <dl> <dt>0x0085</dt> </dl> | 下拉式方塊<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

類型： **sz \_ 或 \_ Ord**

</dd> <dd>

16位元素的可變長度陣列，包含控制項的初始文字或資源識別碼。 如果這個陣列的第一個元素是0xFFFF，則陣列有一個額外的元素，可在可執行檔中指定資源的序數值（例如圖示）。 您可以針對控制項（例如靜態圖示控制項）使用資源識別碼來載入和顯示圖示或其他資源，而不是文字。 如果第一個元素是0xFFFF 以外的任何值，系統會將陣列視為以 null 終止的 Unicode 字串，以指定初始文字。

</dd> <dt>

**extraCount**
</dt> <dd>

類型： **WORD**

</dd> <dd>

遵循這個成員的建立資料位元組數目。 如果這個值大於零，則建立的資料會從下一個 **字** 邊界開始。 此建立資料可以是任何大小和格式。 控制項的視窗程式必須能夠解讀資料。 當系統建立控制項時，它會在傳送至控制項之 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息的 *lParam* 參數中，傳遞此資料的指標。

</dd> </dl>

## <a name="remarks"></a>備註

對話方塊的延伸範本包含 [**DLGTEMPLATEEX**](dlgtemplateex.md) 標頭，後面接著對話方塊中每個控制項的 **DLGITEMTEMPLATEEX** 結構。

每個 **DLGITEMTEMPLATEEX** 結構都必須對齊 **DWORD** 界限。 可變長度的 **windowClass** 和 **標題** 陣列必須對齊 **字** 組邊界。 建立資料陣列（如果有的話）必須對齊 **字** 邊界。

如果您在 **windowClass** 和 **標題** 陣列中指定字元字串，就必須使用 Unicode 字串。 您可以使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函數，從 ANSI 字串產生 Unicode 字串。

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

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ 建立**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**WM \_ 說明**](../shell/wm-help.md)
</dt> </dl>

 

