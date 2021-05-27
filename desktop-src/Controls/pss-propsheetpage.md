---
title: 'PROPSHEETPAGE 結構 (Prsht.idl .h) '
description: 定義屬性工作表中的頁面。
keywords:
- PROPSHEETPAGE 結構 Windows 控制項
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 78e1d1e4e6b4b2067083443bdb5dc4db5df59558
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550343"
---
# <a name="propsheetpage-structure"></a>PROPSHEETPAGE 結構

定義屬性工作表中的頁面。

## <a name="syntax"></a>語法

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a>成員

*dwSize* 

類型： [DWORD](../winprog/windows-data-types.md)

此結構的大小（以位元組為單位）。

*dwFlags* 

類型： [DWORD](../winprog/windows-data-types.md)

旗標，指出建立屬性工作表頁面時要使用的選項。 這個成員可以是下列值的組合。

| 值 | 意義 |
|-------|---------|
| PSP_DEFAULT | 使用所有結構成員的預設意義。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |
| PSP_DLGINDIRECT | 從 *pResource* 成員所指向之記憶體中的對話方塊範本建立頁面。 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta)函式會假設記憶體中的範本未寫入保護。 唯讀範本會在某些版本的 Windows 中造成例外狀況。 |
| PSP_HASHELP | 當頁面為使用中狀態時，啟用 **屬性工作表說明** 按鈕。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |
| PSP_HIDEHEADER | [5.80 版](common-control-versions.md) 和更新版本。 當選取頁面時，讓 wizard 屬性工作表隱藏頁首區域。 如果已提供浮水印，則會在頁面的左側繪製。 此旗標應針對 [歡迎使用] 和 [完成] 頁面設定，並針對內部頁面省略。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |
| PSP_PREMATURE | [4.71 版](common-control-versions.md) 或更新版本。 當建立屬性工作表時，會建立頁面。 如果未指定此旗標，則在第一次選取該頁面之前，將不會建立該頁面。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |
| PSP_RTLREADING | 反轉顯示 *pszTitle* 的方向。 一般視窗會顯示所有文字，包括 *pszTitle*、由左至右 (LTR) 。 針對從右至左 (RTL) 的希伯來文或阿拉伯文等語言，可以將視窗鏡像，所有文字都會以 RTL 顯示。 如果設定了 PSP_RTLREADING， *pszTitle* 會改為在一般父視窗中讀取 RTL，並在鏡像父視窗中 LTR。 |
| PSP_USECALLBACK | 當建立或終結此結構所定義的屬性工作表頁面時，呼叫 *pfnCallback* 成員所指定的函式。 |
| PSP_USEFUSIONCONTEXT | [6.0 版](common-control-versions.md) 和更新版本。 使用啟用內容。 若要使用啟用內容，您必須設定這個旗標，並將啟用內容控制碼指派給 *hActCtx*。 請參閱備註。 |
| PSP_USEHEADERSUBTITLE | [5.80 版](common-control-versions.md) 或更新版本。 顯示 *pszHeaderSubTitle* 成員指向的字串，做為 Wizard97 頁面標頭區域的子標題。 若要使用此旗標，您也必須在相關聯的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。 如果已設定 PSP_HIDEHEADER，則會忽略 PSP_USEHEADERSUBTITLE 旗標。 在 Aero 樣式的嚮導中，標題會出現在工作區頂端附近。 |
| PSP_USEHEADERTITLE | [5.80 版](common-control-versions.md) 或更新版本。 顯示 *pszHeaderTitle* 成員所指向的字串，做為 Wizard97 內部頁面標頭中的標題。 您也必須在相關聯的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。 如果已設定 PSP_HIDEHEADER，則會忽略 PSP_USEHEADERTITLE 旗標。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |
| PSP_USEHICON | 使用 *hIcon* 做為頁面索引標籤上的小圖示。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。  |
| PSP_USEICONID | 使用 *pszIcon* 做為要載入的圖示資源名稱，並作為頁面索引標籤上的小圖示使用。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |
| PSP_USEREFPARENT | 針對從此結構建立的屬性工作表頁面存留期，維護 *pcRefParent* 成員所指定的參考計數。 |
| PSP_USETITLE | 使用 *pszTitle* 成員做為屬性工作表對話方塊的標題，而不是儲存在對話方塊範本中的標題。 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。 |

*hInstance* 

類型： [HINSTANCE](../winprog/windows-data-types.md)

要從其中載入圖示或字串資源的實例控制碼。 如果 *pszIcon*、 *pszTitle*、 *pszHeaderTitle* 或 *pszHeaderSubTitle* 成員識別要載入的資源，則必須指定 *hInstance* 。

*pszTemplate* 

類型： [LPCSTR](../winprog/windows-data-types.md)

用來建立頁面的對話方塊範本。 這個成員可以指定範本的資源識別碼，或指定範本名稱的字串位址。 如果已設定 *dwFlags* 成員中的 PSP_DLGINDIRECT 旗標，則會忽略 *pszTemplate* 。 這個成員會宣告為具有 *pResource* 的聯集。

*pResource* 

類型： **LPCDLGTEMPLATE**

記憶體中對話方塊範本的指標。 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta)函式會假設範本未受寫入保護。 唯讀範本會在某些版本的 Windows 中造成例外狀況。 若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_DLGINDIRECT 旗標。 這個成員會宣告為具有 *pszTemplate* 的聯集。

*hIcon* 

類型： [HICON](../winprog/windows-data-types.md)

圖示的控制碼，用來做為頁面索引標籤中的圖示。 如果 *dwFlags* 成員不包含 PSP_USEHICON，則會忽略這個成員。 這個成員會宣告為具有 *pszIcon* 的聯集。

*pszIcon* 

類型： [LPCSTR](../winprog/windows-data-types.md)

圖示資源，用來做為頁面索引標籤中的圖示。 這個成員可以指定圖示資源的識別碼，或指定圖示資源名稱的字串位址。 若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USEICONID 旗標。 這個成員會宣告為具有 *hIcon* 的聯集。

*pszTitle* 

類型： [LPCSTR](../winprog/windows-data-types.md)

[屬性工作表] 對話方塊的標題。 此標題會覆寫對話方塊範本中指定的標題。 這個成員可以指定字串資源的識別碼或指定標題之字串的位址。 若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USETITLE 旗標。

*pfnDlgProc* 

類型： **DLGPROC**

頁面的對話方塊程式指標。 因為頁面是建立為非強制回應對話方塊，所以對話方塊程式不能呼叫 [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) 函數。

*lParam* 

類型： [LPARAM](../winprog/windows-data-types.md)

當建立頁面時，會將頁面的 **PROPSHEETPAGE** 結構複本傳遞至對話方塊程式，並提供 [WM_INITDIALOG](../dlgbox/wm-initdialog.md) 訊息。 系統會提供 *lParam* 成員，讓您將應用程式特定的資訊傳遞給對話方塊程式。 它不會對頁面本身產生任何影響。

*pfnCallback* 

類型： **LPFNPSPCALLBACK**

應用程式定義回呼函式的指標，該函式會在頁面建立時以及即將終結時呼叫。 如需回呼函數的詳細資訊，請參閱 [LPFNPSPCALLBACKA 回呼函數](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)。 若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USECALLBACK 旗標。

*pcRefParent* 

類型： [UINT *](../winprog/windows-data-types.md)

參考計數值的指標。 若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USEREFPARENT 旗標。

> [!NOTE]
> 建立屬性工作表頁面時， *pcRefParent* 所指向的值會遞增。 您可以在 [PROPSHEETHEADER](pss-propsheetheader.md)的 *dwFlags* 成員中設定 PSH_PROPSHEETPAGE 旗標，並呼叫 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta)函式，以隱含方式建立屬性工作表頁面。 您可以使用 [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函式來明確地進行。 當屬性工作表頁面損毀時， *pcRefParent* 成員指向的值會遞減。 當屬性工作表損毀時，就會自動發生這種情況。 您可以使用 [DestroyPropertySheetPage](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) 函式來明確終結屬性工作表頁面。

*pszHeaderTitle* 

類型： [LPCTSTR](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 標題區域的標題。 若要在 Wizard97 樣式的 wizard 下使用這個成員，您也必須執行下列動作：

* 在 *dwFlags* 成員中設定 PSP_USEHEADERTITLE 旗標。
* 在頁面的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。
* 請確定未設定 *dwFlags* 成員中的 PSP_HIDEHEADER 旗標。

*pszHeaderSubTitle* 

類型： [LPCTSTR](../winprog/windows-data-types.md)

[5.80 版](common-control-versions.md) 或更新版本。 標題區域的子標題。 若要使用這個成員，您必須執行下列動作：

* 在 *dwFlags* 成員中設定 PSP_USEHEADERSUBTITLE 旗標。
* 在頁面的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。
* 請確定未設定 *dwFlags* 成員中的 PSP_HIDEHEADER 旗標。

> [!NOTE]
> 使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md) 時，會忽略這個成員) 

*hActCtx* 

類型： [控制碼](../winprog/windows-data-types.md)

[6.0 版](common-control-versions.md) 或更新版本。 啟用內容控制碼。 將這個成員設定為當您使用 [CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa)建立啟用內容時所傳回的控制碼。 系統會先啟動此內容，再建立對話方塊。 如果您使用全域資訊清單，就不需要使用這個成員。

*hbmHeader* 

類型： [HBITMAP](../winprog/windows-data-types.md)

這個成員會宣告為具有 *pszbmHeader* 的聯集。

*pszbmHeader*

類型： [LPCSTR](../winprog/windows-data-types.md)

這個成員會宣告為具有 *hbmHeader* 的聯集。

## <a name="remarks"></a>備註

Comctl32.dll 版6和更新版本不能轉散發。 若要使用 Comctl32.dll 6 版或更新版本，請在資訊清單中指定 .dll 檔案。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | \[僅限 Windows Vista 桌面應用程式\]                                    |
| 最低支援的伺服器 | 僅限 Windows Server 2003 \[ desktop 應用程式\]                              |
| 標頭                   | Prsht.idl。h |
| Unicode 與 ANSI 名稱                   | **PROPSHEETHEADERW** (Unicode) 和 **PROPSHEETHEADERA** (ANSI)  |