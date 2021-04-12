---
title: 一般對話方塊類型
description: 本主題討論不同的對話方塊。
ms.assetid: 2d0217d2-5410-4f74-8090-a3bb2481f473
keywords:
- 通用對話方塊程式庫
- 通用對話方塊
- 開啟對話方塊
- '[另存新檔] 對話方塊'
- 尋找對話方塊
- 取代對話方塊
- 列印對話方塊
- '[列印設定] 對話方塊'
- '[列印屬性工作表] 對話方塊'
- 版面設定對話方塊
- '[色彩] 對話方塊'
- 字型對話方塊
- 預先定義的對話方塊
- 對話方塊、通用對話方塊程式庫
- 預先定義的對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e143b72a60f3478545f76ce102fd6d99767ce
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/19/2020
ms.locfileid: "104093563"
---
# <a name="common-dialog-box-types"></a>一般對話方塊類型

通用對話方塊程式庫提供了建立函式，以及每一種通用對話方塊的結構。 若要以最簡單的形式使用通用對話方塊，您可以呼叫其建立函式，並指定包含初始值和選項旗標之結構的指標。 初始化對話方塊之後，對話方塊程式會使用結構來傳回使用者輸入的相關資訊。 您也可以自訂通用對話方塊，以符合應用程式的需求。

下表提供不同類型之通用對話方塊的簡短描述，並顯示每個類型所使用的函數和結構。



| 對話方塊                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **色彩**<br/>      | 顯示可用的色彩，並選擇性地讓使用者建立自訂色彩。 使用者可以選取基本或自訂的色彩。 使用 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 函數和 [**ChooseColor**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構。 如需詳細資訊，請參閱 [色彩對話方塊](color-dialog-box.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Find**<br/>       | 顯示對話方塊，讓使用者可以在其中輸入要尋找的字串。 使用者也可以指定搜尋選項，例如搜尋方向以及搜尋是否區分大小寫。 使用 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 函數和 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構。 如需詳細資訊，請參閱 [尋找和取代對話方塊](find-and-replace-dialog-boxes.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **字型**<br/>       | 顯示對話方塊，讓使用者可以在其中選取字型系列以及相關聯的字型樣式、點大小和其他字型屬性，例如字型色彩、底線或刪除線。 使用 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函數和 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構。 如需詳細資訊，請參閱 [ [字型] 對話方塊](font-dialog-box.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **開啟**<br/>       | 顯示對話方塊，讓使用者可以在其中輸入或選取要開啟的檔案或 shell 命名空間物件的名稱。 此對話方塊包含磁片磁碟機、目錄和 shell 命名空間延伸模組的清單，可讓使用者流覽 shell 命名空間。 它也包含副檔名清單，可讓使用者篩選所顯示的檔案名。 使用 [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) 函數和 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構。 如需詳細資訊，請參閱 [開啟和另存](open-and-save-as-dialog-boxes.md)新檔對話方塊。<br/>                                                                                                                                                                                                                                                                                     |
| **設定列印格式**<br/> | 顯示目前的頁面設定。 使用者可以選取頁面設定選項，例如紙張方向、大小、來源和邊界。 使用 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函數和 [**PageSetupDlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構。 如需詳細資訊，請參閱版面 [設定對話方塊](page-setup-dialog-box.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Print**<br/>      | 顯示已安裝之印表機與其設定的相關資訊。 使用者可以選取列印工作選項，例如要列印的頁面範圍和份數，然後開始列印程式。 使用 [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) 函數和 [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 結構。 如需詳細資訊，請參閱 [ [列印] 對話方塊](print-dialog-box.md)。<br/> 若要顯示 **列印** 屬性工作表，而不是 [ **列印** ] 對話方塊，請使用 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數搭配 [**PrintDlgEx**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) 結構。 屬性工作表的 [ **一般** ] 頁面類似于 [ **列印** ] 對話方塊。 在 [ **一般** ] 頁面之後，屬性工作表可以有其他的應用程式特定和驅動程式特定的屬性頁。 如需詳細資訊，請參閱 [列印屬性工作表](print-property-sheet.md)。<br/> |
| **Replace**<br/>    | 顯示對話方塊，讓使用者可以在其中輸入要尋找的字串和取代字串。 使用者可以指定搜尋選項，例如搜尋是否區分大小寫，以及替代選項（例如取代的範圍）。 使用 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函數和 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構。 如需詳細資訊，請參閱 [尋找和取代對話方塊](find-and-replace-dialog-boxes.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **另存新檔**<br/>    | 顯示對話方塊，讓使用者可以在其中輸入或選取用來儲存檔案或 shell 命名空間物件的名稱。 此對話方塊包含磁片磁碟機、目錄和 shell 命名空間延伸模組的清單，可讓使用者流覽 shell 命名空間。 它也包含副檔名清單，可讓使用者篩選所顯示的檔案名。 使用 [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) 函數和 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構。 如需詳細資訊，請參閱 [開啟和另存](open-and-save-as-dialog-boxes.md)新檔對話方塊。<br/>                                                                                                                                                                                                                                                                             |



 

雖然 [ **列印設定** ] 對話方塊可供使用，但已被 [版面 **設定** ] 對話方塊取代。 應用程式應該使用 [版面 **設定** ] 對話方塊，而不是 [ **列印設定** ] 對話方塊。

除了 [ **尋找** 和 **取代** ] 對話方塊以外，所有通用對話方塊都是強制回應。 在用來建立對話方塊的函數可以傳回之前，使用者必須關閉強制回應對話方塊。 [ **尋找** 和 **取代** ] 對話方塊為無模式;此函數會在對話方塊關閉之前傳回。 如果您使用 [ **尋找** 和 **取代** ] 對話方塊，您也必須在應用程式的主要訊息迴圈中使用 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函式，以確保這些對話方塊能正確地處理鍵盤輸入，例如 TAB 和 ESC 鍵。

 

