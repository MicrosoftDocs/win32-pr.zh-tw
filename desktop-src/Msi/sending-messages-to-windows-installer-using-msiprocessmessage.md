---
description: 使用 MsiProcessMessage 傳送的訊息，與 INSTALLUI 處理常式回呼函數所接收的訊息相同（ \_ 如果呼叫 MsiSetExternalUI）。
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: 使用 MsiProcessMessage 將訊息傳送至 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c639e45b22c2406f446ab31072ceb02ab9b3e906f5973b1436356d96f3782
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629948"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>使用 MsiProcessMessage 將訊息傳送至 Windows Installer

使用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 傳送的訊息，與 [**INSTALLUI \_ 處理常式**](/windows/desktop/api/Msi/nc-msi-installui_handlera) 回呼函數所接收的訊息相同（如果呼叫 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) ）。 否則，Windows Installer 會處理訊息。 如需詳細資訊，請參閱[剖析 Windows Installer 的訊息](parsing-windows-installer-messages.md)。

例如，若要傳送 INSTALLMESSAGE \_ 錯誤訊息與 mb \_ ICONWARNING 圖示和 mb \_ ABORTRETRYCANCEL 按鈕：


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



其中 *hInstall* 是安裝的控制碼，提供給自訂動作或 [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)或 [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)的 *hProduct* 控制碼，而 *hRec* 則是包含要格式化之錯誤資訊的記錄。 如需如何執行格式的詳細資訊，請參閱 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)。

根據預設，如果傳送 INSTALLMESSAGE \_ 錯誤或 INSTALLMESSAGE \_ FATALEXIT 訊息時未指定按鈕類型或圖示類型，則會 \_ 使用 [mb 確定]、[無] 圖示和 [mb \_ DEFBUTTON1]。

Windows在顯示具有 MB ABORTRETRYIGNORE 按鈕規格的 MessageBox 時，安裝程式不會將 [**中止**] 按鈕標示為「中止」 \_ ，而是使用「取消」字串來標記按鈕。 所有錯誤訊息都不會使用 "Abort" 這個字，而是改用 "Cancel" 這個字。

[**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)函數的 *hRecord* 參數取決於傳送至 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)的訊息類型。 下列清單詳細說明記錄相對於訊息類型的需求：

INSTALLMESSAGE \_ FATALEXIT

 

INSTALLMESSAGE \_ 資訊

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| 欄位         | 描述                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 結果字串格式的範本。 如需詳細資訊，請參閱 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 。 記錄的欄位是使用 \[ 1 \] 代表欄位1、 \[ 2 \] 表示欄位2等等。 |
| 1到 *n* | 所有後續的欄位都與欄位0中範本所參考的欄位直接相關。                                                                                                                    |



 

如果欄位0是 null，則 UI 處理常式收到的字串會格式化為：1： \[ 欄位 1 2 的資料 \] ： \[ 欄位2的資料 \] ，這表示針對記錄的每個欄位，此字串會包含欄位編號，後面接著儲存在欄位中的資料。

當 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)、'/l '[命令列選項](command-line-options.md)或 [記錄原則](logging.md)指定 ' I ' 或 INSTALLLOGMODE 資訊時，會記錄來自 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)的資訊訊息 \_ 。

INSTALLMESSAGE \_ 錯誤

 

INSTALLMESSAGE \_ 警告

 

INSTALLMESSAGE \_ 使用者

使用錯誤資料表中的訊息。



| 欄位         | 描述                                           |
|---------------|-------------------------------------------------------|
| 0             | 必須是 null。                                         |
| 1             | [錯誤資料表](error-table.md)中的訊息編號。 |
| 2到 *n* | 與錯誤資料表中指定的訊息相關。  |



 

例如，



| 欄位 | 類型   | 資料       |
|-------|--------|------------|
| 0     | 字串 | null       |
| 1     | int    | 1304       |
| 2     | 字串 | Myfile.txt |



 

從 UI 處理常式收到的產生的訊息為：

錯誤1304。 寫入檔案時發生錯誤： Myfile.txt。 確認您有存取該目錄的許可權。

如果欄位0不是 null，則會覆寫錯誤資料表中的訊息。 相反地，「欄位0」範本會決定訊息的格式。

此訊息也可以指定按鈕（包括預設按鈕），以及與上面所述的訊息搭配使用的圖示。 按鈕和圖示類型會列在 [**INSTALLUI \_ 處理常式**](/windows/desktop/api/Msi/nc-msi-installui_handlera)中。

INSTALLMESSAGE \_ COMMONDATA

傳送此訊息以啟用或停用 [進度] 對話方塊中的 [ **取消** ] 按鈕。



| 欄位 | 描述                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 未使用的。                                                                                                                                      |
| 1     | 2指的是 [ **取消** ] 按鈕。                                                                                                           |
| 2     | 值為1表示應該可以看到 [ **取消** ] 按鈕。 0值表示 [ **取消** ] 按鈕應該是隱藏的。<br/> |



 

例如，若要停用或隱藏 [ **取消** ] 按鈕，記錄會如下所示。



| 欄位 | 類型   | 資料 |
|-------|--------|------|
| 0     | 字串 | null |
| 1     | int    | 2    |
| 2     | int    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

INSTALLMESSAGE \_ ACTIONSTART 記錄會決定 ActionData 記錄的格式。



| 欄位 | 描述                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                          |
| 1     | 動作名稱。 此欄位中的名稱必須是非 null。                                                         |
| 2     | 動作描述。                                                                                           |
| 3     | 動作範本。 這是用於根據此範本格式化訊息的 ActionData。 |



 

請勿在動作範本訊息中參考欄位0。

INSTALLMESSAGE \_ ACTIONDATA 記錄的格式如下。



| 欄位         | 描述                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | null                                                                                                                                               |
| 1到 *n* | 相依于 \_ [ActionText 資料表](actiontext-table.md)中所指定之對應 INSTALLMESSAGE ACTIONSTART 訊息或範本的欄位3。 |



 

例如，INSTALLMESSAGE \_ ACTIONSTART 記錄。



| 欄位 | 類型   | 資料                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | 字串 | null                                                            |
| 1     | 字串 | MyAction                                                        |
| 2     | 字串 | 這是 "MyAction" 的描述                           |
| 3     | 字串 | MyAction 範本： field1 資料為 \[ 1 \] 。 欄位2資料是 \[ 2 \] 。 |



 

INSTALLMESSAGE \_ ACTIONSTART (欄位3的範本) 參考欄位1和2，INSTALLMESSAGE \_ ACTIONDATA 記錄應該有2個欄位包含所保證的資料。 這些欄位可以是 [字串] 或 [整數] 欄位。

INSTALLMESSAGE \_ ACTIONDATA 記錄。



| 欄位 | 類型   | 資料                    |
|-------|--------|-------------------------|
| 0     | 字串 | null                    |
| 1     | int    | 2                       |
| 2     | 字串 | 適用于 MyAction 的 ActionData |



 

INSTALLMESSAGE \_ FILESINUSE

FILESINUSE 記錄是可變長度的記錄。



| 欄位 | 描述                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 這個欄位可以是 null。 針對使用基本 UI 的安裝，此欄位可能會指定靜態文字，以在 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)的[ListBox 控制項](listbox-control.md)中顯示。 針對使用完整 UI 的安裝，此欄位不會有任何作用，因為文字是由撰寫自訂 FilesInUse 對話方塊所指定。 |
| 1     | 使用中的檔案名。                                                                                                                                                                                                                                                                                                                                        |
| 2     | 此欄位會識別保留使用中檔案的進程。**Windows Installer 版本4.0：** 進程的處理序識別碼 (PID) ，或進程的視窗標題。<br/> **Windows Installer 3.1 版及更早版本：** 此欄位必須是進程的處理序識別碼 (PID) 。<br/>                                                      |



 

例如，若要傳送 FilesInUse 訊息以顯示使用中的兩個檔案，red.exe 和 blue.exe，記錄有四個欄位加上0欄位。 記錄格式如下表所示。 此範例需要 Windows Installer 4.0 版。

**Windows Installer 3.1 版及更早版本：** 下列範例中的欄位2和4必須包含持有 red.exe 之進程的 Pid，以及使用 blue.exe。



| 欄位 | 描述       |
|-------|-------------------|
| 0     | null              |
| 1     | Red.exe           |
| 2     | 紅色視窗標題  |
| 3     | Blue.exe          |
| 4     | 藍色視窗標題 |



 

> [!Note]  
> 在 Windows Installer 4.0 版中，如果從服務傳遞的 PID 沒有視窗標題（例如系統匣應用程式），則不會顯示該檔案，而且詳細資訊記錄檔會包含下列訊息。

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ RESOLVESOURCE

INSTALLMESSAGE \_ RESOLVESOURCE 記錄有七個欄位。 為了讓 INSTALLMESSAGE \_ RESOLVESOURCE 能夠正常運作，外部 UI 處理常式可能不會處理 INSTALLMESSAGE \_ RESOLVESOURCE 訊息。 Windows安裝程式必須處理 INSTALLMESSAGE \_ RESOLVESOURCE 訊息。 也就是說，在篩選 INSTALLMESSAGE RESOLVESOURCE 訊息時，外部 UI 處理常式會傳回0，表示「不採取任何動作」 \_ 。 最佳做法是避免傳送 RESOLVESOURCE 的訊息。



| 欄位 | 描述                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                                                                               |
| 1     | null                                                                                                                                                               |
| 2     | 封裝名稱。                                                                                                                                                      |
| 3     | 產品代碼。                                                                                                                                                      |
| 4     | 相對路徑（如果已知）可以是 null。                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | 是否要驗證封裝程式碼。 值為 ' 1 ' 表示應驗證封裝程式碼。 值為 ' 0 ' 表示不應驗證套件。 |
| 7     | 媒體資料表中所需的磁片。 值為 ' 0 ' 表示可接受任何磁片。                                                                              |



 

 

 




