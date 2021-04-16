---
title: 尋找和取代對話方塊
description: 顯示非強制回應對話方塊，可讓使用者指定要搜尋的字串，以及搜尋檔中的文字時要使用的選項。
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面、通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- 尋找對話方塊
- 取代對話方塊
- 自訂尋找對話方塊
- 自訂取代對話方塊
- 預先定義的對話方塊
- 對話方塊、尋找
- 對話方塊、取代
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3cf2c5217d586c0a5ada74fb7dd72aaca5f804
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104553831"
---
# <a name="find-and-replace-dialog-boxes"></a>尋找和取代對話方塊

顯示非強制回應對話方塊，可讓使用者指定要搜尋的字串，以及搜尋檔中的文字時要使用的選項。 [ **取代** ] 對話方塊可讓使用者指定要搜尋的字串和取代字串，以及控制操作的選項。

您可以藉由初始化 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構並將結構傳遞至 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)函式，來建立和顯示 [**尋找**] 對話方塊。 下圖顯示一般 [ **尋找** ] 對話方塊。

![尋找對話方塊](images/finddialogboxxp.png)

您可以藉由初始化 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構並將結構傳遞至 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)函式，來建立和顯示 [**取代**] 對話方塊。 下圖顯示典型的 [ **取代** ] 對話方塊。

![取代對話方塊](images/replacedialogboxxp.png)

不同于其他常見的對話方塊，[ **尋找** 和 **取代** ] 對話方塊是無模式。 非強制回應對話方塊可讓使用者在對話方塊和建立它的視窗之間切換。 這適用于讓使用者搜尋字串、切換至應用程式視窗以處理字串，然後切換回對話方塊來搜尋另一個字串，而不需要重複開啟對話方塊所需的命令。

如果 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 或 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函式成功建立對話方塊，則會將控制碼傳回至對話方塊。 您可以使用此控制碼來移動和與對話方塊進行通訊。 如果函數無法建立對話方塊，則會傳回 **Null**。 您可以藉由呼叫 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值，以判斷錯誤的原因。

本節將討論下列主題。

-   [FINDMSGSTRING 註冊的訊息](#the-findmsgstring-registered-message)
-   [自訂 [尋找或取代] 對話方塊](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>FINDMSGSTRING 註冊的訊息

在建立 [ **尋找** 或 **取代** ] 對話方塊之前，您必須呼叫 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得 [**FINDMSGSTRING**](findmsgstring.md) 註冊訊息的訊息識別碼。 然後，您可以使用識別碼來偵測和處理從對話方塊傳送的訊息。 當使用者按一下對話方塊中的 [ **尋找下一個**]、[ **取代**] 或 [ **取代全部** ] 按鈕時，對話方塊程式會將 **FINDMSGSTRING** 訊息傳送至主控視窗的視窗程式。 當您建立對話方塊時， [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **hwndOwner** 成員會識別擁有者視窗。

[**FINDMSGSTRING**](findmsgstring.md)訊息的 *lParam* 參數是您在建立對話方塊時所指定之 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的指標。 傳送訊息之前，對話方塊會以最新的使用者輸入設定此結構的成員，包括要搜尋的字串、取代字串 (如果有任何) ，以及尋找和取代作業的選項。

在 [**FINDMSGSTRING**](findmsgstring.md)訊息中， [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **flags** 成員會包含下列其中一個旗標，以指出造成訊息的事件。



| 旗標               | 意義                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | 對話方塊正在關閉。 擁有者視窗處理此訊息之後，對話方塊的控制碼將不再有效。                                                                                    |
| **FR \_ FINDNEXT**   | 使用者按一下 [**尋找** 或 **取代**] 對話方塊中的 [**尋找下一個]** 按鈕。 **LpstrFindWhat** 成員會指定要搜尋的字串。                                                         |
| **FR \_ 取代**    | 使用者按一下 [**取代**] 對話方塊中的 [**取代**] 按鈕。 **LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。     |
| **FR \_ 型全部型** | 使用者按一下 [**取代**] 對話方塊中的 [**全部取代**] 按鈕。 **LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。 |



 

如果是 [ **尋找下一個]** 或 [ **取代全部** ] 訊息， **旗標** 成員可以包含下列旗標的任何組合，以表示搜尋選項。



| 旗標              | 意義                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR-FR \_**      | 如果設定，則會選取 [方向] 選項按鈕的 **向下** 按鈕，表示使用者想要從目前的位置搜尋至檔的結尾。 如果未設定 **FR \_ DOWN** ，則會選取 [ **向上** ] 按鈕，讓使用者想要搜尋檔的開頭。       |
| **FR \_ MATCHCASE** | 如果設定，則會選取 [ **符合大小寫** ] 核取方塊，表示使用者想要搜尋區分大小寫。 如果未設定 **FR \_ MATCHCASE** ，則不會選取此核取方塊，讓搜尋不會區分大小寫。                                                                       |
| **FR \_ WHOLEWORD** | 如果設定，則會選取 [ **僅符合全字** 組] 核取方塊，表示使用者只想搜尋符合搜尋字串的全字組。 如果未設定 **FR \_ WHOLEWORD** ，則不會選取此核取方塊，所以您也應該搜尋符合搜尋字串的文字片段。 |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>自訂 [尋找或取代] 對話方塊

若要自訂 [ **尋找** 或 **取代** ] 對話方塊，您可以使用下列任何一種方法：

-   當您建立對話方塊時，在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構中指定值
-   提供自訂範本
-   提供勾點程式

當您建立 [**尋找** 或 **取代**] 對話方塊時，可以在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **旗標** 成員中設定旗標，以隱藏或停用任何搜尋選項控制項。 例如，您可以將 FR \_ NOMATCHCASE 旗標設定為停 **用 [符合大小寫** ] 核取方塊，或將 [fr HIDEMATCHCASE] 旗標設 \_ 為隱藏。

您可以提供 [ **尋找** 或 **取代** ] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)和 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)函數會使用您的自訂範本來取代預設範本。

**若要提供尋找或取代對話方塊的自訂範本**

1.  藉由修改 Findtext 檔案中指定的預設範本來建立自訂範本。 預設的 [ **尋找** ] 或 [ **取代** ] 對話方塊範本中所使用的控制項識別碼會定義在 Dlgs .h 檔案中。
2.  使用 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構來啟用範本，如下所示：
    -   -   如果您的自訂範本是應用程式或動態連結程式庫中的資源，請 \_ 在 **旗標** 成員中設定 FR ENABLETEMPLATE 旗標。 使用結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。

            -或者-

        -   如果您的自訂範本已在記憶體中，請設定 FR \_ ENABLETEMPLATEHANDLE 旗標。 您可以使用 **hInstance** 成員來識別包含範本的記憶體物件。

您可以在 [**尋找** 或 **取代**] 對話方塊中提供 [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)的勾點程式。 攔截程式可以處理傳送至對話方塊的訊息。 如果您使用自訂範本來定義其他控制項，您必須提供攔截程式來處理控制項的輸入。

**若要啟用尋找或取代對話方塊的勾點程式**

1.  \_在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **FLAGS** 成員中設定 FR ENABLEHOOK 旗標。
2.  在 **lpfnHook** 成員中指定攔截程式的位址。

處理其 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送到攔截程式。 此訊息的 *lParam* 參數是用來初始化對話方塊之 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構的指標。

如果攔截程式傳回 **FALSE** 以回應 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息，則不會顯示此對話方塊，除非攔截程式顯示此對話方塊。 若要這樣做，請先執行任何其他繪製作業，然後呼叫 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) 和 [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) 函數。 下列程式碼提供一個範例：


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 