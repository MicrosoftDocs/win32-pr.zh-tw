---
title: 自訂通用對話方塊
description: 本主題討論如何使用通用對話方塊。
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- 通用對話方塊程式庫，自訂
- 通用對話方塊，自訂
- 自訂通用對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6272cbff88b7544ea945851f4f347cb43031b93ae08852bc139c7fb7ca6dd91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786118"
---
# <a name="customizing-common-dialog-boxes"></a>自訂通用對話方塊

您可以使用其標準格式的通用對話方塊，也可以自訂對話方塊。 從使用者的觀點來看，通用對話方塊的主要優點是它與應用程式之間的外觀和功能一致。 因此，只有在應用程式絕對必要時，才需要自訂通用對話方塊，是很重要的。 否則，就會遺失一致的外觀和簡單的程式碼介面。 適當的自訂會盡可能保持不變的原始控制項數目。 增加對話方塊的大小或在對話方塊中已提供的空間中加入新控制項，是適當的自訂。 隱藏原始控制項，或以其他方式變更原始控制項的預期功能，是較不適當的自訂。

本節討論自訂通用對話方塊的下列方法：

-   [自訂範本](#custom-templates)
-   [一般對話方塊的掛勾程式](#hook-procedures-for-common-dialog-boxes)
-   [常見的對話訊息](#common-dialog-messages)
-   [說明支援](#help-support)
    -   [即時線上說明](#context-sensitive-help)
    -   [[說明] 按鈕](#the-help-button)

## <a name="custom-templates"></a>自訂範本

一般對話方塊有預設範本，可在對話方塊中定義標準控制項的數目、類型和位置。 您可以定義自訂範本，讓使用者存取您應用程式特有的其他控制項。

除了 Explorer 樣式 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊以外的所有通用對話方塊中，您可以修改預設範本，以建立可取代預設範本的自訂範本。 自訂範本會定義標準控制項的類型和位置，以及任何其他控制項。

當您藉由修改預設對話方塊範本來建立自訂對話方塊範本時，請確定任何已加入控制項的識別碼都是唯一的，而且不會與標準控制項的識別碼衝突。 下表列出預設範本檔案的名稱，以及每個通用對話方塊類型的 include 檔。



| 對話方塊類型               | 範本檔案 | 包含檔案 |
|-------------------------------|---------------|--------------|
| **色彩**                     | Color. d     | ColorDlg。h   |
| **Find**                      | Findtext，d  | Dlgs。h       |
| **Font**                      | 字型. d      | Dlgs。h       |
| **開啟** (多重選取)  | Fileopen，d  | Dlgs。h       |
| **開啟** (單一選取)    | Fileopen，d  | Dlgs。h       |
| **設定列印格式**                | Prnsetup，d  | Dlgs。h       |
| **Print**                     | Prnsetup，d  | Dlgs。h       |
|  (淘汰) **列印安裝程式**    | Prnsetup，d  | Dlgs。h       |
| **Replace**                   | Findtext，d  | Dlgs。h       |



 

若要啟用自訂範本，您必須在對話方塊的對應結構的 **旗標** 成員中設定旗標。 如果範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **ENABLETEMPLATE** 旗標，並使用該結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。 如果範本已在記憶體中，請在 **旗標** 成員中設定 **ENABLETEMPLATEHANDLE** 旗標，並使用 **hInstance** 成員來識別包含範本的記憶體物件。

在大多數情況下，您也必須啟用對話方塊的攔截程式，以支援和處理自訂範本中其他控制項的輸入。

若為 Explorer 樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊，則無法使用預設範本進行修改。 相反地，您的自訂範本會定義子對話方塊，其中只包含要加入至標準對話方塊的專案。 自訂範本也可以定義靜態控制項，以指定子對話方塊中標準控制項的群集位置。 如需詳細資訊，請參閱 [Explorer 樣式的自訂範本](open-and-save-as-dialog-boxes.md)。

## <a name="hook-procedures-for-common-dialog-boxes"></a>一般對話方塊的掛勾程式

您可以針對每個通用對話方塊啟用攔截程式，以便處理來自預設對話方塊程式的訊息。 常見的對話攔截程式有兩種一般類型：

-   最常見的對話方塊所使用的標準勾點程式
-   [ **開啟** ] 和 [ **另存** 新檔] 對話方塊所支援的 Explorer 樣式攔截程式

當您針對其中一個通用對話方塊提供標準攔截程式時，預設的對話方塊程式會處理其訊息，如下所示。



| 訊息                                 | 處理                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](wm-initdialog.md) | 預設對話方塊程式會先處理訊息，然後再將訊息傳遞至攔截程式。 訊息的 *lParam* 參數是建立對話方塊時所指定之初始化結構的指標。 |
| 所有其他訊息                      | 攔截程式會先接收訊息。 然後，攔截程式的傳回值會決定預設的對話方塊程式是要處理訊息，還是忽略它。                                     |



 

若為 Explorer 樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊，攔截程式就不會在對話方塊中收到標準控制項所需的訊息。 相反地，它會從對話方塊接收通知訊息，並針對您在自訂範本中定義的任何其他控制項接收訊息。 如需詳細資訊，請參閱 [Explorer 樣式的勾點程式](open-and-save-as-dialog-boxes.md)。

若要啟用攔截程式，請在對話方塊的對應結構的 **旗標** 成員中設定 **ENABLEHOOK** 值。 如果設定了 **ENABLEHOOK** 旗標，則結構的 **lpfnHook** 成員必須指定攔截程式的位址。

下表顯示每個通用對話方塊所提供的攔截程式類型。



| 對話方塊類型                          | 攔截程式                                      |
|------------------------------------------|-----------------------------------------------------|
| **色彩**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **尋找** 或 **取代**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Font**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **開啟** 或 **另存為** (Explorer 樣式的)  | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **開啟** 或 **另存為** (舊樣式的)       | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Print**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **設定列印格式**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

在 [版面設定] 對話方塊中，您也可以指定 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)勾點 **程式**。 這是您可以用來自訂 [版面 **設定** ] 對話方塊所顯示之範例頁面外觀的特殊攔截程式。

> [!Note]  
> [ **列印設定** ] 對話方塊已由 [版面 **設定** ] 對話方塊取代。 應用程式應該使用 [版面 **設定** ] 對話方塊。 不過，為了相容性， [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函式會繼續支援顯示 [ **列印設定** ] 對話方塊。 您可以為 [**列印設定**] 對話方塊提供 [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc)攔截程式。

 

## <a name="common-dialog-messages"></a>常見的對話訊息

一般對話方塊會使用訊息，在特定事件發生時通知您的視窗程式或攔截程式。 此外，您還可以傳送訊息給通用對話方塊，以抓取資訊或控制對話方塊的行為或外觀。 本章節描述 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式所註冊的一般對話訊息、[ **字型** ] 對話方塊和 [版面 **設定** ] 對話方塊所使用的訊息，以及 Explorer 樣式 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊所使用的訊息。

通用對話方塊程式庫會定義一組訊息字串。 您可以將與其中一個訊息字串相關聯的常數傳遞給 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) ，以取得訊息識別碼。 然後，您可以使用識別碼來偵測和處理從通用對話方塊傳送的訊息，或將訊息傳送至通用對話方塊。 下表顯示訊息常數，並說明其用法。



| Contants                               | 使用                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | 當使用者選取色彩，然後按一下 [**確定]** 按鈕時，[**色彩**] 對話方塊會將此訊息傳送至攔截程式。 攔截程式可以接受色彩或拒絕它，並強制對話方塊維持開啟狀態。                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | 當使用者選取檔案名，然後按一下 [確定] 按鈕時，[**開啟**] 或 **[** **另存** 新檔] 對話方塊會將此訊息傳送到攔截程式。 攔截程式可以接受檔案名，或將它拒絕，然後強制對話方塊保持開啟狀態。 若為 Explorer 樣式的 [**開啟**] 和 [**另存** 新檔] 對話方塊，此訊息已被 [**CDN \_ FILEOK**](cdn-fileok.md)通知訊息取代。<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | 當使用者按一下 [**尋找下一個**]、[**取代**] 或 [**全部取代**]，或關閉對話方塊時，[**尋找** 或 **取代**] 對話方塊會將此訊息傳送至其父視窗的視窗程式。 訊息的 *lParam* 參數是 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構的指標，其中包含使用者的輸入。                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | 當使用者按一下 [說明] 按鈕 **時，所有** 通用對話方塊都會將此訊息傳送至其父視窗的視窗程式。 若為 Explorer 樣式的 [**開啟**] 和 [**另存** 新檔] 對話方塊，此訊息已由 [**CDN \_ 說明通知**](cdn-help.md)訊息取代。<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | [ **開啟** ] 或 [ **另存** 新檔] 對話方塊會在使用者變更 [ **檔案名** ] 清單方塊中的選取專案時，將此訊息傳送到攔截程式。 若為 Explorer 樣式的 [**開啟**] 和 [**另存** 新檔] 對話方塊，此訊息已被 [**CDN \_ SELCHANGE**](cdn-selchange.md)通知訊息取代。<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | 攔截程式可以將此訊息傳送至 [ **色彩** ] 對話方塊，以設定目前的色彩選取範圍。                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | 當使用者按一下 [**確定]** 按鈕時，如果選取的檔案發生共用違規，[**開啟**] 或 [**另存** 新檔] 對話方塊會將此訊息傳送至攔截程式。 若為 Explorer 樣式的 [**開啟**] 和 [**另存** 新檔] 對話方塊，此訊息已被 [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md)通知訊息取代。<br/>                                                        |



 

某些常見的對話方塊會傳送和接收其他視窗訊息。 [**字型**] 對話方塊的 [攔截程式] 可將任何 **WM \_ CHOOSEFONT \_ \* *_ 訊息傳送至 [_* 字型**] 對話方塊。 如需詳細資訊，請參閱 [ [字型] 對話方塊](font-dialog-box.md)。 如果您已啟用 [_PagePaintHook *](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)攔截程式，則 [版面 **設定**] 對話方塊會傳送 **WM \_ PSD \_ \** _ 訊息。 如需詳細資訊，請參閱版面 [設定對話方塊](page-setup-dialog-box.md)。

Explorer 樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊支援一組預先定義的訊息。 其中包括以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息形式傳送至您的攔截程式訊息的通知訊息，以及您的攔截程式可傳送至對話方塊的訊息。 如需這些訊息的完整清單，請參閱 [Explorer 樣式的勾點程式](open-and-save-as-dialog-boxes.md)。

## <a name="help-support"></a>說明支援

通用對話方塊可提供對話方塊之標準控制項的即時線上說明。 若要提供通用對話方塊的其他說明，您可以在使用者按下按鈕時，顯示 [說明 **] 按鈕並處理產生的訊息** 。 [說明] 按鈕是預設即時線上說明的 **補充資訊。** [說明 **] 按鈕適用** 于描述對話方塊套用至應用程式時的一般用途。

-   [即時線上說明](#context-sensitive-help)
-   [[說明] 按鈕](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive 說明

所有通用對話方塊都提供對話方塊之標準控制項的即時線上說明。 使用者可以使用下列任一種方法來顯示個別控制項的說明：

-   選取控制項，然後按下 F1 鍵。
-   按一下 **？** 按鈕，然後再按一下控制項。
-   在控制項上按一下滑鼠右鍵。

如果您加入新控制項來自訂對話方塊，您也必須藉由處理攔截程式中的 [說明] 要求，擴充這些控制項的 [說明] 支援。 當使用者要求協助時，攔截程式會收到下列訊息。



| 使用者動作                                                           | 訊息                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| 在控制項上按一下滑鼠右鍵。                          | [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) |
| 按下 F1 鍵。                                                   | [**WM \_ 說明**](../shell/wm-help.md)               |
| 按一下 [ **？** ] 按鈕，然後按一下控制項。 | [**WM \_ 說明**](../shell/wm-help.md)               |



 

您應該針對已加入的控制項處理這些訊息，但讓預設對話方塊程式處理標準控制項的訊息。 如需如何處理這些訊息的詳細資訊，請 [參閱說明](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85))。

### <a name="the-help-button"></a>[說明] 按鈕

您可以在對話方塊的初始化結構的 **旗標** 成員中設定 **SHOWHELP** 值，以在任何通用對話方塊中顯示 [說明 **] 按鈕。** 如果您顯示 [說明 **] 按鈕，** 就必須處理使用者的 [說明] 要求。 您可以在其中一個應用程式的視窗程式中，或在對話方塊的勾點程式中完成處理。 一般來說，您會呼叫 [**WinHelp**](/windows/win32/api/winuser/nf-winuser-winhelpa) 函式來處理要求以取得協助。

若要在其中一個視窗程式中處理說明訊息，您必須取得 [**HELPMSGSTRING**](helpmsgstring.md) 值所定義之字串的訊息識別碼，並識別要接收訊息的視窗。 若要取得訊息識別碼，請在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **HELPMSGSTRING** 做為參數。 當您建立對話方塊時，請使用對話方塊初始化結構的 **hwndOwner** 成員來識別要接收訊息的視窗。 每次使用者按一下 [說明 **] 按鈕時** ，對話方塊程式就會將訊息傳送至視窗程式。

若要處理攔截程式中的說明訊息，您應該處理 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。 如果此訊息的 *wParam* 參數指出使用者按下 [說明 **] 按鈕，** 攔截程式就會提供協助。 **[說明] 按鈕的** 識別碼是 Dlgs .h 檔中定義的 **pshHelp** 常數。

針對 [Explorer 樣式 **開啟**] 和 [**另存** 新檔] 對話方塊的 [掛上] 程式，不會收到 [說明 **] 按鈕的** [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息。 相反地，當您按一下 [說明 **] 按鈕時**，對話方塊會傳送 [**CDN \_ 說明**](cdn-help.md)通知訊息到攔截程式。

 

