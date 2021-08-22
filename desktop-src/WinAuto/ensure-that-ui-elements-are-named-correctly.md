---
title: 確定 UI 元素的命名正確
description: 本主題說明在 Microsoft Win32 應用程式中指定 UI 元素名稱的正確方式，讓 Microsoft Active Accessibility 可以透過 IAccessible \ 32，準確地將名稱公開給用戶端應用程式。Name 屬性。
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c047228159e011ffa9a0842f1748ee07e6af4a49ff296ae8ed65b494b8c53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052758"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>確定 UI 元素的命名正確

本主題說明在 Microsoft Win32 應用程式中指定 UI 元素名稱的正確方式，讓 Microsoft Active Accessibility 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name 屬性](name-property.md)，準確地將名稱公開給用戶端應用程式。

本節中的資訊僅適用于 Microsoft Active Accessibility。 它並不適用于使用 Microsoft 消費者介面自動化的應用程式，或是以標記語言（例如 HTML、動態 HTML (DHTML) 或 XML）為基礎的應用程式。

-   [概觀](#overview)
-   [錯誤命名如何造成問題](#how-incorrect-naming-causes-problems)
-   [MSAA 如何取得 Name 屬性](#how-msaa-gets-the-name-property)
-   [如何尋找和修正命名問題](#how-to-find-and-correct-naming-problems)
-   [如何正確命名的簡介](#how-to-correctly-name-a-trackbar)
-   [如何使用隱藏的標籤來命名控制項](#how-to-use-invisible-labels-to-name-controls)
-   [如何使用直接注釋來指定名稱屬性](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [批註名稱屬性的步驟](#steps-for-annotating-the-name-property)
    -   [批註名稱屬性的範例](#example-of-annotating-the-name-property)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

在 Microsoft Active Accessibility 中，應用程式中的每個 UI 元素都會以公開 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的物件來表示。 用戶端應用程式會使用 **IAccessible** 介面的屬性和方法來與 UI 元素互動，以及取得其相關資訊。 **IAccessible** 介面所公開的其中一個最重要的屬性是 [Name 屬性](name-property.md)。 用戶端應用程式依賴 Name 屬性來尋找、識別或向使用者宣告 UI 元素。 如果 Microsoft Active Accessibility 無法正確地公開特定 UI 元素的 Name 屬性，用戶端應用程式將無法向使用者顯示該 UI 專案，而且殘障使用者將無法存取 UI 元素。

## <a name="how-incorrect-naming-causes-problems"></a>錯誤命名如何造成問題

為了說明 UI 元素命名不正確所造成的問題，請考慮下圖所示的名稱輸入表單。

![輸入姓氏和姓氏的簡單表單圖例](images/incorrect-form.png)

雖然表單中的 UI 元素看起來沒問題，但程式設計的執行是不正確的。 若為 Microsoft Active Accessibility 的用戶端，例如螢幕讀取器，則頂端編輯控制項的 [ [名稱] 屬性](name-property.md) 是 [姓氏：]，而底部編輯控制項的 [名稱] 屬性是空字串 ( "" ) 。 螢幕閱讀程式會將最上層的編輯控制項讀取為「姓氏」，雖然使用者預期會輸入名字。 螢幕閱讀程式會將第二個編輯控制項讀取為「沒有名稱」，因此使用者將不知道要在第二個編輯控制項中輸入的內容。 螢幕讀取器無法協助使用者將資料輸入這個簡單的表單。

表單的另一個問題是，沒有任何快捷方式按鍵指派給任何編輯控制項。 使用者會強制使用 tab 鍵移至控制項或使用滑鼠。

下列各節說明這些問題的來源，並提供修正這些問題的指導方針。

## <a name="how-msaa-gets-the-name-property"></a>MSAA 如何取得 Name 屬性

根據 UI 元素的類型而定，Microsoft Active Accessibility 會從不同的位置取得 [名稱屬性](name-property.md) 字串。 對於具有相關聯視窗文字的大部分 UI 元素，Microsoft Active Accessibility 使用視窗文字做為名稱屬性字串。 這種類型的 UI 元素範例包括按鈕、功能表項目和工具提示等控制項。

針對下列控制項，Microsoft Active Accessibility 會忽略視窗文字，而改為在定位順序中的控制項上方尋找靜態文字標籤 (或群組框標籤) 。

-   下拉式方塊
-   日期和時間選擇器
-   編輯和 Rich Edit 控制項
-   IP 位址控制項
-   清單方塊
-   列出視圖
-   進度列
-   杆
-   具有 SS \_ 圖示或 ss 點陣圖樣式的靜態 \_ 控制項
-   Trackbars
-   樹狀檢視

如果上述控制項未伴隨著靜態文字標籤，或標籤未正確地執行，Microsoft Active Accessibility 無法提供正確的 [名稱屬性](name-property.md) 給用戶端應用程式。

上述的大部分控制項實際上都有相關聯的視窗文字。 資源編輯器會自動產生視窗文字，其中包含泛型字串，例如 "edit1" 或 "listbox3"。 雖然開發人員可以使用更有意義的文字來取代產生的視窗文字，但大部分的情況都是如此。 因為產生的視窗文字對使用者沒有任何意義，Microsoft Active Accessibility 會忽略它，並改為使用隨附的靜態文字標籤。

## <a name="how-to-find-and-correct-naming-problems"></a>如何尋找和修正命名問題

在名稱輸入表單中所顯示的命名錯誤如何造成問題，問題的原因是控制項的定位順序不正確。 使用 [檢查](inspect-objects.md) 之類的測試控管來檢查 UI 會顯示物件階層的問題。 下列螢幕擷取畫面顯示 [檢查] 中所顯示之名稱輸入表單的中斷物件階層。

![[檢查] 工具的螢幕擷取畫面，其中顯示名稱輸入表單的不正確物件階層](images/incorrect-object-hierarchy.png)

在上一個螢幕擷取畫面中，請注意，物件階層不符合控制項在名稱輸入表單的使用者介面中顯示的結構。 另請注意， [檢查](inspect-objects.md) 已將不正確的名稱指派給下一個專案 (它是輸入名字的編輯控制項，而且應該是名為 "first name：" 的名稱。 最後，請注意，檢查找不到最後一個專案的名稱 (它是輸入姓氏的編輯控制項，名稱應為 "Last Name："。

下列範例會顯示名稱輸入表單的資源檔內容。 請注意，索引標籤順序與控制項出現在使用者介面中的邏輯結構不一致。 也請注意，這兩個編輯控制項未指定快速鍵。

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

若要更正名稱輸入表單的問題，應編輯資源 ( .rc) 檔案以指定鍵盤快速鍵，並以下列順序放置控制項：

1.  "&First Name：" 靜態文字標籤。
2.  用來輸入名字 (IDC EDIT1) 的編輯控制項 \_ 。
3.  "&Last Name：" 靜態文字標籤。
4.   (IDC EDIT2) 輸入姓氏的編輯控制項 \_ 。
5.  [確定] 預設推送按鈕。

下列範例會顯示名稱輸入表單的已更正資源檔：

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

若要更正資源檔，您可以直接編輯檔案，也可以使用 Microsoft Visual Studio 中的定位順序工具。 您可以按下 CTRL + D，或從 [**格式**] 功能表中選取 [定位 **順序]** ，以存取 Visual Studio 中的定位順序工具。

修正和重建應用程式之後，名稱輸入表單的 UI 看起來會與之前相同。 不過，Microsoft Active Accessibility 現在會提供正確的名稱屬性給用戶端應用程式，並在使用者按下 ALT + F 或 ALT + L 鍵盤快速鍵時，正確地設定焦點。 此外， [檢查](inspect-objects.md) 將會顯示正確的物件階層，如下列螢幕擷取畫面所示。

![可存取的瀏覽器工具的螢幕擷取畫面，其中顯示名稱輸入表單的正確物件階層](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>如何正確命名的簡介

當 (或滑杆) 定義標題時，請確定字幕的主要靜態文字標籤會出現在標題之前，而且最小和最大範圍的靜態文字標籤會出現在標題之後。 請記住，Microsoft Active Accessibility 會使用緊接在控制項前面的靜態文字標籤，作為控制項的 [ [名稱] 屬性](name-property.md) 。 將主要靜態文字標籤放在貼文之前，並在其後面加上其他標籤，可確保 Microsoft Active Accessibility 提供正確的名稱屬性給用戶端。

下圖顯示具有主要靜態文字標籤的一般字幕（稱為「速度」），以及最小 ( 「最小」 ) 的靜態文字標籤，以及最大 ( 「最大值」 ) 範圍。

![具有最小和最大範圍之主要標籤和標籤的 [標題] 控制項圖例](images/speed-trackbar.png)

下列範例顯示在資源檔中定義標題和其靜態文字標籤的正確方式：

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a>如何使用隱藏的標籤來命名控制項

每個控制項都不一定要有可見的標籤。 例如，有時新增標籤可能會在 UI 的外觀中造成不必要的變更。 在此情況下，您可以使用不可見的標籤。 Microsoft Active Accessibility 仍會挑選與隱藏標籤相關聯的文字，但標籤不會出現在視覺效果 UI 中，也不會干擾。

如同可見標籤，隱藏的標籤必須緊接在定位順序中的控制項前面。 若要在資源檔中將標籤隱藏 ( .rc) ，請將 `NOT WS_VISIBLE` 或加入 `|~WS_VISIBLE` 靜態文字控制項的樣式部分。 如果您在 Visual Studio 中使用資源編輯器，則可以將 Visible 屬性設為 False。

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>如何使用直接注釋來指定名稱屬性

Microsoft Active Accessibility 執行時間元件中包含的預設 proxy Oleacc.dll，會自動為所有標準 Windows 控制項提供 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件。 如果您自訂標準 Windows 控制項，則預設 proxy 會盡可能精確地提供自訂控制項的所有 **IAccessible** 屬性。 您應徹底測試自訂控制項，以確保預設 proxy 會提供精確且完整的屬性值。 如果測試顯示不正確或不完整的屬性值，您可以使用稱為直接注釋的動態注釋技術來提供正確的屬性值，並新增遺漏的屬性值。

請注意，動態注釋不只是 Microsoft Active Accessibility proxy 所支援的控制項。 您也可以使用它來修改或提供任何提供自身 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行的控制項屬性。

本節著重于使用直接注釋，為控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 [Name 屬性](name-property.md)提供正確的值。 您也可以使用直接注釋來提供其他屬性值。 此外，直接注釋旁的其他動態注釋技巧也可供使用，而動態批註 API 的特性和功能則延伸到本章節所述的範圍之外。 如需動態注釋的詳細資訊，請參閱 [動態批註 API](dynamic-annotation-api.md)。

### <a name="steps-for-annotating-the-name-property"></a>批註名稱屬性的步驟

使用直接注釋來變更控制項的 [ [名稱] 屬性](name-property.md) 牽涉到下列步驟。

1.  包含下列標頭檔：
    -   Initguid。h
    -   Oleacc。h

    > [!Note]  
    > 若要定義 Guid，您必須在相同的檔案中包含 Initguid 之前的 Oleacc。

     

2.  藉由呼叫 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函式（通常是在應用程式初始化過程中），初始化元件物件模型 (COM) 程式庫。
3.  建立目標控制項之後 (通常會在 [WM \_ INITDIALOG](../dlgbox/wm-initdialog.md) 訊息) 期間，建立注釋管理員的實例，並取得其 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 指標的指標。
4.  使用 [**IAccPropServices：： SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)方法，標注目標控制項的 [[名稱] 屬性](name-property.md)。

5.  釋放 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 指標。
6.  在終結目標控制項之前 (通常會在處理) 的 WM 終結訊息時，建立注釋管理員的實例，並取得其 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)介面的指標。 [ \_](../winmsg/wm-destroy.md)
7.  您可以使用 [**IAccPropServices：： ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) 方法，從目標控制項清除 [名稱屬性](name-property.md) 批註。
8.  釋放 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 指標。
9.  在您的應用程式結束之前 (通常會在處理 [WM 損 \_ 毀](../winmsg/wm-destroy.md) 訊息) 時，呼叫 [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式來釋放 COM 程式庫。

[**IAccPropServices：： SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)函數接受五個參數。 前三個（*hwnd*、 *idObject* 和 *idChild*）結合以識別控制項。 第四個參數 *idProp* 指定要變更之屬性的識別碼。 若要變更 [Name 屬性](name-property.md)，請將 *IdProp* 設定為 **PROPID \_ ACC \_ Name**。  (如需您可以透過直接注釋設定之其他屬性的清單，請參閱 [使用直接注釋](using-direct-annotation.md)。 ) **SetHwndPropStr** 的最後一個參數（ *str*）是要做為 Name 屬性的新字串。

### <a name="example-of-annotating-the-name-property"></a>批註名稱屬性的範例

下列範例程式碼示範如何使用直接注釋來變更控制項之 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 [Name 屬性](name-property.md)。 為了簡單起見，此範例會使用硬式編碼的字串 ( 「新的控制項名稱」 ) 來設定 Name 屬性。 在應用程式的最終版本中，不應使用硬式編碼的字串，因為它們無法進行當地語系化。 相反地，一律從資源檔載入字串。 此外，此範例不會顯示對 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函數的呼叫。


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[動態注釋 API](dynamic-annotation-api.md)
</dt> <dt>

[提供 Name 屬性](providing-the-name-property.md)
</dt> <dt>

[測試控管](testing-tools.md)
</dt> </dl>

 

 