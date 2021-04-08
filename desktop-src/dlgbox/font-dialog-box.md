---
title: 字型對話方塊
description: '[字型] 對話方塊可讓使用者選擇邏輯字型的屬性，例如字型系列和相關聯的字型樣式、點大小、效果 (底線、刪除線和文字色彩) ，以及腳本 (或字元集) 。'
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面、通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- 字型對話方塊
- 自訂字型對話方塊
- 旗標、字型對話方塊
- 初始化旗標
- 預先定義的對話方塊
- 對話方塊、字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a752ce53ecf496c58efb0c346a8c3d67c4f1b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024029"
---
# <a name="font-dialog-box"></a>字型對話方塊

[ **字型** ] 對話方塊可讓使用者選擇邏輯字型的屬性，例如字型系列和相關聯的字型樣式、點大小、效果 (底線、刪除線和文字色彩) ，以及腳本 (或字元集) 。

您可以藉由初始化 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構並將結構傳遞至 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式，來建立和顯示 **字型** 對話方塊。

下列螢幕擷取畫面顯示一般的 [ **字型** ] 對話方塊。

![顯示 [字型] 對話方塊的螢幕擷取畫面](images/fontdialogboxxp.png)

如果使用者按一下 [ **確定]** 按鈕， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式會傳回 **TRUE** ，並在 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構中設定使用者選取範圍的相關資訊。

如果使用者取消 [ **字型** ] 對話方塊或發生錯誤， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 會傳回 **FALSE** ，且不會定義 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的內容。 您可以使用 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值，以判斷錯誤的原因。

本節將討論下列主題。

-   [字型對話方塊初始化旗標](#font-dialog-box-initialization-flags)
-   [在舊版 Windows 上自訂字型對話方塊](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [在 Windows 7 上自訂字型對話方塊](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>字型對話方塊初始化旗標

在呼叫 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)之前， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **旗標** 成員必須指定 **cf \_ SCREENFONTS**、 **cf \_ PRINTERFONTS** 或 **cf \_ 兩者**，以指出對話方塊是否應列出螢幕字型、印表機字型或兩者。 如果您指定 **cf \_ PRINTERFONTS** 或 **cf \_**， **CHOOSEFONT** 結構的 **hDC** 成員就必須指定印表機的裝置內容控制碼。

如果已設定 **cf \_ PRINTERFONTS** 或 **cf \_ 兩個** 旗標，字型類型描述標籤會出現在 [ **字型** ] 對話方塊的底部。

從 Windows 7 開始，適用于字型列舉的 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式不再使用 **cf \_ PRINTERFONTS**、 **cf \_ SCREENFONTS**、 **cf \_** 和 **cf \_ WYSIWYG** 旗標。 它們在 Windows 7 中已淘汰。 不過， **CF \_ PRINTERFONTS** 旗標會保留一個函式：在 [ **字型** ] 對話方塊底部顯示 [字型類型描述] 標籤。

您可以使用 **旗標** 成員來啟用或停用某些 **字型** 對話方塊控制項，而且您可以搭配其他 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)成員使用 **旗標** 成員來控制某些控制項的初始值。

**若要顯示允許使用者選取 [刪除]、[底線] 和 [色彩] 選項的控制項：**

-   設定 **CF \_ 效果** 旗標。 您可以使用 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **rgbColors** 成員來指定初始字型色彩。

**指定字型、字型樣式、大小、刪除線和底線對話方塊控制項的初始值：**

1.  指定字型、字型樣式、大小、刪除線和底線對話方塊控制項的初始值：
2.  在 **旗標** 成員中設定 **CF \_ INITTOLOGFONTSTRUCT** 旗標，以及 **lpLogFont** 所指向之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的成員，以指定字型屬性的初始值。
3.  您也可以使用 **cf \_ NOFACESEL**、 **cf \_ NOSTYLESEL** 和 **cf \_ NOSIZESEL** 旗標，以防止 [ **字型** ] 對話方塊顯示對應控制項的初始值。 當您使用具有多個字型、樣式或點大小的文字選取專案時，這會很有用。 如果使用者未選取對應的值，則 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)傳回時，這些值也會設定在 **旗標** 中。

**將字型樣式控制項初始化為指定的樣式名稱**

-   設定 **CF \_ USESTYLE** 旗標，並使用 **lpszStyle** 成員指定樣式名稱。

> [!Note]  
> 若要全球化您的應用程式，請使用 **lpLogFont** 所指向之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfWeight** 和 **lfItalic** 成員來指定樣式。 樣式名稱可能會隨著系統使用者介面語言而變更。

 

**若要顯示 [套用] 按鈕**

-   設定 **CF 套用 \_** 旗標，並提供攔截程式來處理 **適用于**[套用] 按鈕的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息。 攔截程式可以將 [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) 訊息傳送至對話方塊，以取得包含字型目前選取範圍的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構位址。

**若要顯示 [說明] 按鈕**

-   設定 **CF \_ SHOWHELP** 旗標。 當使用者按一下 [說明 **] 按鈕時**， **hwndOwner** 成員必須識別要接收 [**HELPMSGSTRING**](helpmsgstring.md)註冊訊息的視窗。

**限制顯示在對話方塊中的字型**

-   設定 **cf \_ TTONLY**、 **cf \_ FIXEDPITCHONLY**、 **cf \_ NOVECTORFONTS**、 **cf \_ NOVERTFONTS**、 **cf \_ SCALABLEONLY** 和 **CF \_ WYSIWYG** 旗標的任何組合。 您也可以使用 **CF \_ NOSIMULATIONS** 值，限制對話方塊針對某些字型顯示的可用樣式。

從 Windows 7 開始，對話方塊中顯示的字型清單會根據使用者的顯示字型而受到限制。 若要移除限制，請設定 **CF \_ INACTIVEFONTS** 旗標。

**限制使用者可指定的字型名稱、樣式和點大小**

1.  設定 **CF \_ FORCEFONTEXIST** 旗標，以限制使用者只指定有效的字型名稱、樣式，以及對話方塊中所列的點大小。
2.  設定 **CF \_ LIMITSIZE** 旗標，以限制使用者在 **nSizeMin** 和 **nSizeMax** 成員所指定的範圍中指定點大小。

**限制或停用腳本下拉式方塊**

-   將 **cf \_ NOSCRIPTSEL** 旗標設定為停用 [ **腳本** ] 下拉式方塊，或設定 **cf \_ SELECTSCRIPT** 旗標，將 [ **腳本** ] 下拉式方塊中的選取範圍限制為指定的字元集。

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>在舊版 Windows 上自訂字型對話方塊

您可以提供 [ **字型** ] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式會使用您的自訂範本來取代預設範本。

**提供 [字型] 對話方塊的自訂範本**

1.  藉由修改 Font-family 檔案中指定的預設範本來建立自訂範本。 在 [預設字型] 對話方塊範本中使用的控制項識別碼是在 Dlgs 檔中定義。
2.  使用 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構來啟用範本，如下所示：
    -   如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **CF \_ ENABLETEMPLATE** 旗標。 使用結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。
    -   如果您的自訂範本已在記憶體中，請設定 **CF \_ ENABLETEMPLATEHANDLE** 旗標。 您可以使用 **hInstance** 成員來識別包含範本的記憶體物件。

您可以針對 [**字型**] 對話方塊提供 [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式。 攔截程式可以處理傳送至對話方塊的訊息，並將訊息傳送至對話方塊。 如果您使用自訂範本來定義其他控制項，您必須提供攔截程式來處理控制項的輸入。

**若要啟用 [字型] 對話方塊的勾點程式**

1.  在 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **旗標** 成員中設定 **CF \_ ENABLEHOOK** 旗標。
2.  在 **lpfnHook** 成員中指定攔截程式的位址。

處理 [**wm \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送到攔截程式。 此訊息的 *lParam* 參數是用來初始化對話方塊之 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構的指標。

攔截程式可以將 [**wm \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)、 [**wm \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)和 [**wm \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) 訊息傳送至對話方塊，以取得和設定對話方塊的目前值和旗標。

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>在 Windows 7 上自訂字型對話方塊

下列螢幕擷取畫面顯示 Windows 7 中的一般 **字型** 對話方塊。

![顯示 [字型 dialob] 方塊的螢幕擷取畫面](images/fontdialogboxwin7.png)

在舊版的 Windows 中，font-family 範本檔案包含一個預設 ChooseFont 範本。 Windows 7 上的 font-size 範本檔包含兩個預設範本：舊版 Windows 的預設範本和新的 Windows 7 ChooseFont 範本。 因此，當您在 Windows 7 上自訂 [ **字型** ] 對話方塊時，您必須考慮下列問題。

1.  當您針對在 Windows 7 上執行的應用程式建立自訂範本時，請使用新的範本。 這個新範本包含連結控制項，可讓使用者按一下以啟動字型 **主控台** 視窗，如下列螢幕擷取畫面所示。

    ![顯示 windows 7 中字型 [控制台] 的螢幕擷取畫面](images/fontcontrolpanelforwin7.png)

2.  若要使用此連結控制項，呼叫的應用程式必須使用 COMCTL32.DLL 6 版或更新版本。 否則，當 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式嘗試在您的自訂範本中建立連結控制項時，會傳回錯誤。 若要判斷是否已啟用此控制項，請針對 COMCTL32.DLL 版本6.0 編譯您的呼叫應用程式。 如需詳細資訊，請參閱 [使用通用控制項啟用視覺化樣式](/previous-versions//ms649781(v=vs.85))。
3.  如果您的應用程式使用 COMCTL32.DLL 5.0 版或更早版本，當您建立自訂範本時，必須執行下列動作：

    -   將控制項指定為 **按鈕**。 用來啟動字型 **主控台** 的控制項將會顯示為按鈕，而不是連結。
    -   取代下列字型中的文字： d：

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        使用下列文字：

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   為確保您的應用程式使用自訂範本，您必須使用 **CF \_ ENABLETEMPLATE** 旗標來指定自訂範本、根據 Windows 7 ChooseFont 範本建立自訂範本，然後選擇性地啟用攔截程式。

        如果您在未建立自訂範本的情況下啟用攔截程式，將會載入舊版 Windows 的預設 ChooseFont 範本。

> [!Note]  
> 您必須根據應用程式所編譯的 COMMCTL.DLL 版本，在新的範本中指定 **控制項** 或 **按鈕** 控制項類型。 另請注意，當您的應用程式在舊版 Windows 作業系統上執行時，就無法使用 Windows 7 特有的功能，例如，字型清單和延伸系列的 WYSIWYG 顯示。

 

 

 