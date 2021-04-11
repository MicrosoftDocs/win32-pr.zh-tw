---
title: 列印對話方塊
description: '[列印] 對話方塊可讓使用者選取特定列印工作的選項。'
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面、通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- 列印對話方塊
- '[列印設定] 對話方塊'
- 自訂列印對話方塊
- 預先定義的對話方塊
- 對話方塊、列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fae1dd244391ea16478a0cb4f10803cf622dc64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093256"
---
# <a name="print-dialog-box"></a>列印對話方塊

[ **列印** ] 對話方塊可讓使用者選取特定列印工作的選項。 例如，使用者可以指定要使用的印表機、要列印的頁面範圍，以及份數。

您可以使用 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式來顯示 [列印屬性工作表，該工作表](print-property-sheet.md)的 **[一般** ] 頁面中包含與 [ **列印** ] 對話方塊類似的控制項。 在 [ **一般** ] 頁面之後，屬性工作表也可以有其他的應用程式特定和驅動程式特定的屬性頁。

您可以藉由初始化 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構並將結構傳遞至 [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))函式，來建立和顯示 [**列印**] 對話方塊。

下圖顯示典型的 [ **列印** ] 對話方塊。

![[列印] 對話方塊](images/printdialogboxxp.png)

如果使用者按一下 [ **確定]** 按鈕， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 會傳回 **TRUE** ，並使用 [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構來傳回使用者選取專案的相關資訊。 例如， **hDevMode** 和 **hDevNames** 成員通常會傳回和 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構的全域記憶體控制碼。 您可以使用這些結構中的資訊，建立所選印表機的裝置內容或資訊內容。

如果使用者取消 [ **列印** ] 對話方塊或發生錯誤， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 會傳回 **FALSE**。 您可以使用 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值，以判斷錯誤的原因。

[ **列印** ] 對話方塊包含一組選項按鈕的 **列印範圍** ，指出使用者是否想要列印所有頁面、頁面範圍，或只列印選取的文字。 在呼叫 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))之前，您可以設定其中一個 **PD \_ allpages 提出要求**、 **pd \_ 選取專案** 或 **pd \_ PAGENUMS** 旗標，以指出一開始選取哪一個按鈕。 當 **PrintDlg** 傳回 **TRUE** 時，函式會設定其中一個旗標來表示使用者的選取專案。 如果設定了 **PD \_ PAGENUMS** ， [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 **nFromPage** 和 **nToPage** 成員就會包含使用者所指定的起始和結束頁面。 若要停 **用**[**頁面**] 選項按鈕與其相關聯的和 **來** 編輯控制項，請設定 **PD \_ NOPAGENUMS** 旗標。 若要停用 **選取範圍** 選項按鈕，請設定 **PD \_ NOSELECTION** 旗標。

對話方塊中包含編輯控制項，使用者可在其中輸入要列印的份數。 如果 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 **hDevMode** 成員為非 **Null**，則結構的 **dmCopies** 成員會指定此編輯控制項的初始值。 如果 **hDevMode** 為 **Null**，則 **PRINTDLG** 結構的 **nCopies** 成員會指定初始值。 當 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 傳回時， **nCopies** 通常表示使用者指定的複本數目。 但是，如果您在建立對話方塊時設定了 **PD \_ USEDEVMODECOPIESANDCOLLATE** 旗標，則 **nCopies** 在 return 時一律會設為1，而 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)的 **dmCopies** 成員則表示要列印的份數。

[ **Collate** ] 核取方塊指出如果列印多份副本，使用者是否想要 Collate 頁面。 如果已選取 [ **collate** ] 核取方塊，則會設定 **PD \_ collate** 旗標。 如果您的應用程式不支援多個複本或模擬定序，請在 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 Flags 成員中設定 **PD \_ USEDEVMODECOPIESANDCOLLATE** 旗 **標**。 除非印表機驅動程式支援多個複本和定序，否則此選項會停用 [ **Collate** ] 核取方塊和 [複製] 編輯控制項的 **數目** 。

[ **列印到** 檔案] 核取方塊會指出使用者是否想要將輸出傳送至檔案，而不是傳送至印表機。 您可以設定 **PD \_ PRINTTOFILE** 旗標，如此一來，一開始就會選取此核取方塊。 若要隱藏此核取方塊，請設定 **PD \_ HIDEPRINTTOFILE** 旗標。 若要停用，請設定 **PD \_ DISABLEPRINTTOFILE** 旗標。 如果使用者選取 [**列印到** 檔案] 選項， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))會設定 **PD \_ PRINTTOFILE** 旗標，並在 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)結構的 **wOutputOffset** 成員所指定的位移處傳回 "File："。 當您呼叫函式來開始列印工作時，請在結構的 **lpszOutput** 成員中指定這個 "FILE：" 字串。 指定這個字串會導致列印子系統查詢使用者輸入輸出檔的名稱。

依預設，[ **列印** ] 對話方塊一開始會顯示目前預設印表機的相關資訊。 若要顯示另一個已安裝之印表機的資訊，請初始化和 [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) 結構，並將全域記憶體控制碼指派給 **hDevMode** 和 **hDevNames** 成員的結構。 您在 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的 **dmDeviceName** 成員中指定的裝置名稱和 **DEVNAMES** 結構的 **wDriverOffset** 成員，都必須識別也列在 Win.ini 檔案的 [裝置] 區段中的印表機裝置 \[ \] 。 如果未列出裝置， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 會傳回錯誤。

您可以藉由在 [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 **旗標** 成員中設定 **pd \_ RETURNDC** 或 **pd \_ RETURNIC** 旗標，指示 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))建立印表機的裝置內容或資訊內容。 函數會將控制碼傳回給 **hDC** 成員中的裝置內容或資訊內容。 如果您使用 **PD \_ RETURNDC** 旗標，您可以使用裝置內容來產生印表機的輸出。

若要取出預設印表機的相關資訊，而不顯示 [ **列印** ] 對話方塊，請設定 [ **PD \_ RETURNDEFAULT** 旗標]。 在此情況下， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 會在將 **hDevMode** 和 **hDevNames** 成員設定為包含資訊之結構的控制碼之後立即傳回。

依預設， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 會在發生錯誤時顯示訊息方塊。 例如，如果沒有安裝印表機，此函式會顯示錯誤訊息。 若要防止函式顯示這些警告訊息，請設定 **PD \_ NOWARNING** 旗標。

本節將討論下列主題。

-   [自訂列印對話方塊](#customizing-the-print-dialog-box)
-   [[列印設定] 對話方塊](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>自訂列印對話方塊

您可以提供 [ **列印** ] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))函式會使用您的自訂範本來取代預設範本。

若要提供 [ **列印** ] 對話方塊的自訂範本：

1.  藉由修改 Prnsetup 檔案中指定的預設範本來建立自訂範本。 預設 [ **列印** ] 對話方塊範本中使用的控制項識別碼是在 Dlgs 檔中定義。
2.  使用 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構來啟用範本，如下所示：
    -   如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **PD \_ ENABLEPRINTTEMPLATE** 旗標。 使用結構的 **hInstance** 和 **lpPrintTemplateName** 成員來識別模組和資源名稱。

        -或者-

    -   如果您的自訂範本已在記憶體中，請設定 **PD \_ ENABLEPRINTTEMPLATEHANDLE** 旗標。 您可以使用 **hPrintTemplate** 成員來識別包含範本的記憶體物件。

您可以為 [**列印**] 對話方塊提供 [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)攔截程式。 攔截程式可以處理傳送至對話方塊的訊息。 它也可以將訊息傳送至對話方塊。 如果您使用自訂範本來定義其他控制項，您必須提供攔截程式來處理控制項的輸入。

若要針對 [ **列印** ] 對話方塊啟用攔截程式：

1.  在 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的 Flags 成員中設定 **PD \_ ENABLEPRINTHOOK** 旗 **標**。
2.  在 **lpfnPrintHook** 成員中指定攔截程式的位址。

處理其 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送到攔截程式。 此訊息的 *lParam* 參數是用來初始化對話方塊之 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構的指標。

## <a name="print-setup-dialog-box"></a>[列印設定] 對話方塊

您可以藉由在 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))函式的呼叫中設定 **PD \_ PRINTSETUP** 旗標，來建立和顯示 [**列印設定**] 對話方塊。 不過，[ **列印設定** ] 對話方塊已被 [版面 **設定** ] 對話方塊取代，而且不應該用於新的應用程式。

下列旗標只適用于 [ **列印設定** ] 對話方塊：

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 