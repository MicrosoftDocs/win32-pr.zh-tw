---
title: 版面設定對話方塊
description: 顯示模式對話方塊，可讓使用者選擇包含紙張類型、紙張來源、頁面方向和頁面邊界寬度的設定。
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面、通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- 版面設定對話方塊
- 自訂版面設定對話方塊
- 頁面設定對話方塊、掛勾
- 預先定義的對話方塊
- 對話方塊，頁面設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b9a8f7f30a8313017dc3a124cdccb7d00c872b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093259"
---
# <a name="page-setup-dialog-box"></a>版面設定對話方塊

顯示模式對話方塊，讓使用者可以設定列印頁面的下列屬性：

-   紙張類型 (信封、法律、信件等等) 
-   紙張來源 (手動摘要、車紙、紙器紙、紙器等等) 
-   頁面方向 (縱向或橫向) 
-   頁面邊界的寬度

您可以藉由初始化 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構並將結構傳遞至 [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))函式，來建立和顯示 [版面 **設定**] 對話方塊。 不過，根據印表機的功能而定，對話方塊中顯示的屬性會有所不同。 下圖顯示一般的 [版面 **設定** ] 對話方塊。

![版面設定對話方塊](images/pagesetupdialogboxxp.png)

如果使用者按一下 [**確定]** 按鈕， [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))會在 [**PageSetupDlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構中設定各種成員以指定使用者的選取專案之後傳回 **TRUE** 。 **PtPaperSize** 和 **rtMargin** 成員包含使用者指定的值。 **HDevMode** 和 **HDevNames** 成員包含 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)和 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)結構的全域記憶體控制碼。 這些結構包含其他頁面資訊，以及印表機的相關資訊。 您可以使用這份資訊來準備要傳送到所選印表機的輸出。

如果使用者取消 [版面 **設定** ] 對話方塊或發生錯誤， [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 會傳回 **FALSE**。 若要判斷錯誤的原因，請呼叫 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值。

本節將討論下列主題。

-   [初始化頁面設定對話方塊](#initializing-the-page-setup-dialog-box)
-   [自訂版面設定對話方塊](#customizing-the-page-setup-dialog-box)
-   [自訂範例頁面](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>初始化頁面設定對話方塊

依預設，[版面 **設定** ] 對話方塊會顯示目前預設印表機的相關資訊。 若要指示對話方塊顯示特定印表機的相關資訊，請設定 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 或 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的成員，並將這些結構的全域記憶體控制碼指派給 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)中的對應成員。 如果您指定目前未安裝之印表機的名稱，對話方塊會顯示錯誤訊息。 若要避免對話方塊顯示錯誤訊息，請使用 **PSD \_ NOWARNING** 值。 若要在不顯示 [版面 **設定** ] 對話方塊的情況下取出預設印表機的相關資訊，請使用 [ **PSD \_ RETURNDEFAULT** ] 值。

如果預設測量系統為英寸，則對話方塊會使用萬分之一作為預設測量單位。 如果預設測量系統為計量，此對話方塊會使用百分之一毫米作為預設測量單位。 若要覆寫預設的度量單位，請在 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構的 **旗標** 成員中設定 **psd \_ INHUNDREDTHSOFMILLIMETERS** 或 **psd \_ INTHOUSANDTHSOFINCHES** 旗標。

根據預設，邊界的初始值為1英寸。 如果您設定 [ **PSD \_ 邊界** ] 旗標，此對話方塊會顯示 **rtMargin** 成員中指定的初始邊界值。 使用者可以為邊界指定的預設最小值是印表機允許的最小邊界。 如果您設定了 **PSD \_ MINMARGINS** 旗標，此對話方塊會強制執行 **rtMinMargin** 成員中指定的最小邊界。

若要防止使用者選取特定選項，請設定下列旗標的任何組合，以停用對應的控制項。



| 旗標                        | 意義                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **PSD \_ DISABLEMARGINS**     | 停用使用者在其中輸入邊界設定的編輯控制項。 |
| **PSD \_ DISABLEORIENTATION** | 停用 **[直** 向] 和 [ **橫向** ] 選項按鈕。               |
| **PSD \_ DISABLEPAPER**       | 停用選取紙張大小和紙張來源的控制項。     |
| **PSD \_ DISABLEPRINTER**     | 停用 **印表機** 按鈕。                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>自訂版面設定對話方塊

您可以提供 [版面 **設定** ] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))函式會使用您的自訂範本來取代預設範本。

**提供 [版面設定] 對話方塊的自訂範本**

1.  藉由修改 Prnsetup 檔案中指定的預設範本來建立自訂範本。 預設的 [版面 **設定** ] 對話方塊範本中使用的控制項識別碼會定義于 Dlgs .h 檔案中。
2.  使用 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構來啟用範本，如下所示：
    -   -   如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **PSD \_ ENABLEPAGESETUPTEMPLATE** 旗標。 使用結構的 **hInstance** 和 **lpPageSetupTemplateName** 成員來識別模組和資源名稱。

            -或者-

        -   如果您的自訂範本已在記憶體中，請設定 **PSD \_ ENABLEPAGESETUPTEMPLATEHANDLE** 旗標。 您可以使用 **hPageSetupTemplate** 成員來識別包含範本的記憶體物件。

若要篩選傳送至對話方塊程式的訊息，您可以提供 [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) 攔截程式。 如果您使用自訂範本來定義其他控制項，您必須提供 **PageSetupHook** 勾點程式來處理控制項的輸入。 此外，您可以提供 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式，以自訂 [版面 **設定** ] 對話方塊所顯示的範例頁面內容。 如需有關 **PagePaintHook** 攔截程式的詳細資訊，請參閱 [自訂範例頁面](#customizing-the-sample-page)。

**啟用 PageSetupHook 勾點程式**

1.  在 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構的 Flags 成員中設定 **PSD \_ ENABLEPAGESETUPHOOK** 旗 **標**。
2.  在 **lpfnPageSetupHook** 成員中指定攔截程式的位址。

處理其 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送至 [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) 攔截程式。 此訊息的 *lParam* 參數是用來初始化對話方塊之 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構的指標。

## <a name="customizing-the-sample-page"></a>自訂範例頁面

[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。 影像包含表示所選紙張或信封類型的矩形，以及表示目前邊界的虛線矩形，以及部分 (希臘文文字) 字元來顯示文字在列印頁面上的外觀。

當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。

**啟用 PagePaintHook 勾點程式**

1.  在 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構的 Flags 成員中設定 **PSD \_ ENABLEPAGEPAINTHOOK** 旗 **標**。
2.  在 **lpfnPagePaintHook** 成員中指定攔截程式的位址。

每當對話方塊即將繪製範例頁面的內容時，攔截程式就會依照列出的順序接收下列訊息。



| 訊息                                                  | 意義                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)     | 對話方塊即將繪製範例頁面。 攔截程式可以使用此訊息來準備繪製範例頁面的內容。     |
| [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)     | 對話方塊即將繪製範例頁面。 此訊息指定範例頁面的周框。                               |
| [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)   | 對話方塊即將繪製範例頁面。 此訊息會指定邊界矩形。                                                    |
| [**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)         | 對話方塊即將繪製邊界矩形。                                                                                            |
| [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)   | 對話方塊即將在邊界矩形內繪製希臘文文字。                                                                      |
| [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)     | 對話方塊即將在信封範例頁面的信封戳記矩形中繪製。 這則訊息只會傳送給信封。             |
| [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md) | 對話方塊即將繪製信封範例頁面的傳回位址部分。 傳送信封和其他紙張大小的訊息。 |



 

如果此攔截程式針對繪製順序的前三個訊息中的任一個傳回 **TRUE** ([**WM \_ psd \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)、 [**wm \_ psd \_ FULLPAGERECT**](wm-psd-fullpagerect.md)或 [**WM \_ psd \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) 對話方塊不會傳送其他訊息，也不會在範例頁面中繪製，直到下次系統需要重新繪製範例頁面為止。 如果這三個訊息的攔截程式都傳回 **FALSE** ，則對話方塊會傳送繪圖順序的其餘訊息。

如果此攔截程式針對繪圖順序中的任何其餘訊息傳回 **TRUE** ，對話方塊就不會繪製範例頁面的對應部分。 如果攔截程式針對上述任何訊息傳回 **FALSE** ，則對話方塊會繪製範例頁面的該部分。

若要防止對話方塊繪製範例頁面的內容，您可以設定 **PSD \_ DISABLEPAGEPAINTING** 旗標。 此旗標不會影響您的 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)攔截程式，它仍會接收所有的 **WM \_ PSD \_ \*** 訊息，並且可以繪製範例頁面內容。

 

 