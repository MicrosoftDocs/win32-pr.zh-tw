---
title: 'PROPSHEETHEADER 結構 (Prsht.idl .h) '
description: 定義屬性工作表的框架和頁面。
keywords:
- PROPSHEETHEADER 結構 Windows 控制項
topic_type:
- apiref
api_name:
- PROPSHEETHEADER
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 719982c1e17ab74dc5c624352625d226f8f4bef90ae84dce4f2b85d5dc2713f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085118"
---
# <a name="propsheetheader--structure"></a>PROPSHEETHEADER 結構

定義屬性工作表的框架和頁面。

## <a name="syntax"></a>語法

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HWND       hwndParent;
    HINSTANCE  hInstance;
    union {
        HICON   hIcon;
        LPCTSTR pszIcon;
    };
    LPCTSTR  pszCaption;
    UINT     nPages;
    union {
        UINT    nStartPage;
        LPCTSTR pStartPage;
    };
    union {
        LPCPROPSHEETPAGE ppsp;
        HPROPSHEETPAGE   *phpage;
    };
    PFNPROPSHEETCALLBACK pfnCallback;
    union {
        HBITMAP hbmWatermark;
        LPCTSTR pszbmWatermark;
    };
    HPALETTE  hplWatermark;
    union {
        HBITMAP hbmHeader;
        LPCSTR  pszbmHeader;
    };
} PROPSHEETHEADER, *LPPROPSHEETHEADER;
```

## <a name="members"></a>成員

*dwSize* 

類型： [DWORD](../winprog/windows-data-types.md)

此結構的大小（以位元組為單位）。 屬性工作表管理員會使用這個成員來判斷您所使用的 **PROPSHEETHEADER** 結構版本。 如需詳細資訊，請參閱＜備註＞一節。

*dwFlags* 

類型： [DWORD](../winprog/windows-data-types.md)

旗標，指出建立屬性工作表頁面時要使用的選項。 這個成員可以是下列值的組合。

| 值 | 意義 |
|-------|---------|
| PSH_DEFAULT (0x00000000)  | 使用所有結構成員的預設意義，並建立一般屬性工作表。 此旗標的值為零，且不會與其他旗標合併。 |
| PSH_AEROWIZARD (0x00004000)  | [6.00 版](common-control-versions.md) 和更新版本。 建立使用 Aero 樣式的 wizard 屬性工作表。 您也必須設定 PSH_WIZARD 旗標。 必須使用單一執行緒的單元 (STA) 模型。 |
| PSH_HASHELP (0x00000200)  | 允許 [屬性工作表] 頁面顯示 [說明 **] 按鈕。** 建立頁面時，您也必須在頁面的 [PROPSHEETPAGE](pss-propsheetpage.md) 結構中設定 PSP_HASHELP 旗標。 如果有任何初始屬性工作表頁面啟用 [說明 **] 按鈕，** 就會自動設定 PSH_HASHELP。 如果任何初始頁面都沒有啟用 [說明] 按鈕，您必須明確地設定 PSH_HASHELP 如果您想要在稍後可能加入的任何頁面上有 [說明 **] 按鈕。** 此旗標不支援搭配 PSH_AEROWIZARD 使用。|
| PSH_HEADER (0x00080000)  | [5.80 版](common-control-versions.md) 和更新版本。 指出將使用 Wizard97 wizard 的標頭點陣圖。 您也必須設定 PSH_WIZARD97 旗標。 如果設定了 PSH_USEHBMHEADER 旗標，則會從 *hbmHeader* 成員取得標頭點陣圖。 否則，就會從 *pszbmHeader* 成員取得標頭點陣圖。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_HEADERBITMAP (0x08000000)  | [6.00 版](common-control-versions.md) 和更新版本。 *PszbmHeader* 成員會指定標頭區域中顯示的點陣圖。 必須搭配 PSH_AEROWIZARD 一起使用。 |
| PSH_MODELESS (0x00000400)  | 使 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) 函式將屬性工作表建立為非強制回應對話方塊，而非強制回應對話方塊。 當設定這個旗標時， [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) 會在建立對話方塊之後立即傳回，而 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) 的傳回值是 [屬性工作表] 對話方塊的視窗控制碼。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_NOAPPLYNOW (0x00000080)  | 移除 [ **套用** ] 按鈕。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_NOCONTEXTHELP (0x02000000)  | [5.80 版](common-control-versions.md) 和更新版本。 移除即時線上說明按鈕 ( "？") ，通常會出現在屬性工作表的標題列上。 此旗標對嚮導無效。 如需有關如何移除舊版通用控制項 **標題列說明** 按鈕的討論，請參閱 [屬性工作表](property-sheets.md)。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_NOMARGIN (0x10000000)  | [6.00 版](common-control-versions.md) 或更新版本。 指定在頁面和框架之間沒有插入邊界。 必須搭配 PSH_AEROWIZARD 一起使用。 |
| PSH_PROPSHEETPAGE (0x00000008)  | 當建立屬性工作表的頁面時，會使用 *ppsp* 成員並忽略 *phpage* 成員。 |
| PSH_PROPTITLE (0x00000001)  | 表示 *pszCaption* 是要顯示其屬性之內容的名稱。 Windows 會對標題進行版本和語言相依的調整。 例如，在英文中，"Properties for" 的片語會加在非空白 *pszCaption* (，如果 *pszCaption* 產生空白的標題，則標題只是 "Properties" ) 。 如果省略此旗標，則會原封不動地使用 pszCaption。  |
| PSH_RESIZABLE (0x04000000)  | 允許使用者調整嚮導的大小。 [最大化] 和 [最小化] 按鈕會出現在嚮導的畫面格中，而畫面格則會調整 若要使用此旗標，您也必須設定 PSH_AEROWIZARD。 |
| PSH_RTLREADING (0x00000800)  | 將 [屬性工作表] 或 [wizard] 視窗設定為由右至左 (RTL) 讀取順序，適用于希伯來文和阿拉伯文等語言。 如果未指定此旗標，屬性工作表視窗預設為從左至右 (LTR) 讀取順序，而 wizard 視窗符合目前頁面的讀取順序。 |
| PSH_STRETCHWATERMARK (0x00040000)  | 在 Wizard97 樣式的 [嚮導] 中伸展水位線。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 此樣式旗標只包含在為特定應用程式提供回溯相容性。 不建議使用它，只有通用控制項版本4.0 和4.01 才支援此功能。 使用通用控制項5.80 版和更新版本時，會忽略此旗標。 |
| PSH_USECALLBACK (0x00000100)  | 當特定事件發生時，呼叫 *pfnCallback* 參數所指定的函式。 如需詳細資訊，請參閱 [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) 回呼函數的描述。 |
| PSH_USEHBMHEADER (0x00100000)  | [版本 5.80](common-control-versions.md)。 從 *hbmHeader* 成員（而不是 *pszbmHeader* 成員）取得標頭點陣圖。 您也必須將 PSH_AEROWIZARD 旗標或 PSH_WIZARD97 旗標與 PSH_HEADER 旗標一起設定。 |
| PSH_USEHBMWATERMARK (0x00010000)  | [版本 5.80](common-control-versions.md)。 從 *hbmWatermark* 成員（而不是 *pszbmWatermark* 成員）取得浮水印點陣圖。 您也必須設定 PSH_WIZARD97 和 PSH_WATERMARK。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_USEHICON (0x00000002)  | 在 [屬性工作表] 對話方塊的標題列中，使用 *hIcon* 做為小圖示。 |
| PSH_USEHPLWATERMARK (0x00020000)  | [版本 5.80](common-control-versions.md)。 使用 *hplWatermark* 成員所指向的 **HPALETTE** 結構，而不是預設的調色板，以繪製 Wizard97 wizard 的浮水印點陣圖和/或標頭點陣圖。 您也必須設定 PSH_WIZARD97，並 PSH_WATERMARK 或 PSH_HEADER。 此旗標不支援搭配 PSH_AEROWIZARD 使用。  |
| PSH_USEICONID (0x00000004)  | 使用 *pszIcon* 做為要載入之圖示資源的名稱，並在 [屬性工作表] 對話方塊的標題列中，用來做為小圖示。 |
| PSH_USEPAGELANG (0x00200000)  | [版本 5.80](common-control-versions.md)。 指定將會從第一頁的資源取得屬性工作表的語言。 該頁面必須由資源識別碼指定。 |
| PSH_USEPSTARTPAGE (0x00000040)  | 顯示內容表的初始頁面時，會使用 *pStartPage* 成員，而不是 *nStartPage* 成員。 |
| PSH_WATERMARK (0x00008000)  | [版本 5.80](common-control-versions.md)。 指定在具有 PSP_HIDEHEADER 樣式的頁面上，將浮水印點陣圖與 Wizard97 wizard 一起使用。 您也必須設定 PSH_WIZARD97 旗標。 除非設定 PSH_USEHBMWATERMARK，否則會從 *pszbmWatermark* 成員取得浮水印點陣圖。 在此情況下，會從 *hbmWatermark* 成員取得標頭點陣圖。 此旗標不支援搭配 PSH_AEROWIZARD 使用。  |
| PSH_WIZARD (0x00000020)  | 建立 wizard 屬性工作表。 使用 PSH_AEROWIZARD 時，您也必須設定此旗標。 |
| PSH_WIZARD97 (0x01000000)  | [版本 5.80](common-control-versions.md)。 建立 Wizard97 樣式的屬性工作表，它支援內部頁面標頭中的點陣圖以及外部頁面的左側。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_WIZARDCONTEXTHELP (0x00001000)  | 新增上下文相關 **説明** 按鈕 ( "？") ，通常會從 wizard 的標題列中消失。 此旗標對一般屬性工作表而言是不正確。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |
| PSH_WIZARDHASFINISH (0x00000010)   | 一律在嚮導上顯示 [ **完成]** 按鈕。 您也必須設定 PSH_WIZARD、PSH_WIZARD97 或 PSH_AEROWIZARD。 |
| PSH_WIZARD_LITE (0x00400000)  | [版本 5.80](common-control-versions.md)。 使用 Wizard lite 樣式。 這種樣式與 PSH_WIZARD97 的外觀相似，但它的執行方式非常類似 PSH_WIZARD。 頁面的格式化方式有一些限制。 比方說，沒有任何強制的框線，而且 PSH_WIZARD_LITE 的樣式不會以 Wizard97 的方式繪製浮水印和標頭點陣圖。 此旗標不支援搭配 PSH_AEROWIZARD 使用。 |

*hwndParent* 

類型： [HWND](../winprog/windows-data-types.md)

屬性工作表的擁有者視窗控制碼。

*hInstance* 

類型： [HINSTANCE](../winprog/windows-data-types.md)

要從其中載入圖示、標題字串資源、起始頁名稱、標頭點陣圖或浮水印的實例控制碼。 如果 *pszIcon*、 *pszCaption*、 *pStartPage*、 *pszbmHeader* 或 *pszbmWatermark* 成員識別要載入的資源，則必須指定這個成員。

*hIcon* 

類型： [HICON](../winprog/windows-data-types.md)

在 [屬性工作表] 對話方塊的標題列中，用來做為小圖示的圖示控制碼。 如果 *dwFlags* 成員包含 PSH_USEHICON，則會使用這個成員。 這個成員會宣告為具有 *pszIcon* 的聯集。

*pszIcon* 

類型： [LPCTSTR](../winprog/windows-data-types.md)

圖示資源，用來作為 [屬性工作表] 對話方塊的標題列中的小圖示。 如果 *dwFlags* 成員包含 PSH_USEICONID，則會使用這個成員。 這個成員可以指定圖示資源的識別碼，或指定圖示資源名稱的字串位址。 在這兩種情況下，都會從 *hInstance* 成員所提供的實例載入圖示。 這個成員會宣告為具有 *hIcon* 的聯集。

*pszCaption* 

類型： [LPCTSTR](../winprog/windows-data-types.md)

[屬性工作表] 對話方塊的標題。 這個成員可以指定字串資源的識別碼 (從 *hInstance* 成員所指定的實例載入) 或指定標題之字串的位址。 如果 *dwFlags* 成員包含 PSH_PROPTITLE，就會在標題的開頭插入的字串 **屬性** 。 Wizard97 的嚮導會忽略此欄位。 針對 Aero 的嚮導，無論是否已設定 PSH_PROPTITLE 旗標，都會將字串單獨用於標題。

*nPages* 

類型： [UINT](../winprog/windows-data-types.md)

*Ppsp* 或 *phpage* 陣列中提供的屬性工作表頁面數目。

*nStartPage* 

類型： [UINT](../winprog/windows-data-types.md)

當建立屬性工作表對話方塊時，所顯示之初始頁面的以零為基底的索引。 如果 *dwFlags* 成員不包含 PSH_USEPSTARTPAGE 旗標，則會使用這個成員。 這個成員會宣告為具有 *pStartPage* 的聯集。

*pStartPage* 

類型： [LPCTSTR](../winprog/windows-data-types.md)

建立屬性工作表對話方塊時所出現的初始頁面名稱。 如果 *dwFlags* 成員包含 PSH_USESTARTPAGE 旗標，則會使用這個成員。 這個成員可以指定字串資源的識別碼 (從 *hInstance* 成員所指定的實例載入) 或指定名稱之字串的位址。 起始頁名稱會與頁面的標題相符。 這個成員會宣告為具有 *nStartPage* 的聯集。

*ppsp* 

類型： **LPCPROPSHEETPAGE**

[PROPSHEETPAGE](pss-propsheetpage.md)結構陣列的指標，此陣列會定義屬性工作表中的頁面。 如果 *dwFlags* 成員不包含 PSH_PROPSHEETPAGE，則會忽略這個成員。 請注意， **PROPSHEETPAGE** 結構的大小是可變的。 剖析 *ppsp* 所指向陣列的應用程式，必須將每個頁面的大小納入考慮。 這個成員會宣告為具有 *phpage* 的聯集。

*phpage* 

類型： **HPROPSHEETPAGE \***

指向屬性工作表頁面之控制碼陣列的指標。 如果 *dwFlags* 成員不包含 PSH_PROPSHEETPAGE，則會使用這個成員。 每個控制碼都必須由先前對 [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函式的呼叫所建立。 當 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) 函式傳回時， *phpage* 陣列中的任何 HPROPSHEETPAGE 控制碼都將被終結。 這個成員會宣告為具有 *ppsp* 的聯集。

*pfnCallback* 

類型： **PFNPROPSHEETCALLBACK**

特定事件發生時所呼叫之應用程式定義回呼函數的指標。 如需回呼函數的詳細資訊，請參閱 [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) 回呼函式的描述。 如果 *dwFlags* 成員不包含 PSH_USECALLBACK，則會忽略這個成員。

*hbmWatermark* 

類型： [HBITMAP](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 水位線點陣圖的控制碼。 如果 *dwFlags* 成員不包含 PSH_USEHBMWATERMARK，則會忽略這個成員。

*pszbmWatermark* 

類型： [LPCTSTR](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 用來作為浮水印的點陣圖資源。 這個成員可以指定點陣圖資源的識別碼，或指定點陣圖資源名稱的字串位址。 如果 *dwFlags* 成員包含 PSH_USEHBMWATERMARK，則會忽略這個成員。

*hplWatermark*

類型： [HPALETTE](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 用來繪製浮水印點陣圖和/或標頭點陣圖的 **HPALETTE** 結構。 如果 *dwFlags* 成員不包含 PSH_USEHPLWATERMARK，則會忽略這個成員。

*hbmHeader*

類型： [HBITMAP](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 標頭點陣圖的控制碼。 如果 *dwFlags* 成員不包含 PSH_USEHBMHEADER，則會忽略這個成員。

*pszbmHeader*

類型： [LPCSTR](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 要做為標頭使用的點陣圖資源。 這個成員可以指定點陣圖資源的識別碼，或指定點陣圖資源名稱的字串位址。 如果 *dwFlags* 成員包含 PSH_USEHBMHEADER，則會忽略這個成員。

## <a name="remarks"></a>備註

如果使用者選擇的是放大對話方塊的大型字型等設定，則在 [開始] 和 [完成] 頁面上繪製的浮水印也會放大。 原始點陣圖的大小和位置會維持不變。 其他區域將會填滿點陣圖左上角的圖元色彩。

PSH_WIZARD、PSH_WIZARD97 和 PSH_WIZARD_LITE 樣式互相不相容。 只應設定其中一個樣式旗標。 PSH_AEROWIZARD 應與 PSH_WIZARD 結合。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows\[僅限 Vista desktop 應用程式\]                                    |
| 最低支援的伺服器 | Windows\[僅限 Server 2003 desktop 應用程式\]                              |
| 標頭                   | Prsht.idl。h |
| Unicode 與 ANSI 名稱                   | **PROPSHEETHEADERW** (Unicode) 和 **PROPSHEETHEADERA** (ANSI)  |
