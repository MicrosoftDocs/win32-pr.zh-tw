---
title: 開啟並另存新檔對話方塊
description: '[開啟] 對話方塊可讓使用者指定要開啟之檔案或檔案集合的磁片磁碟機、目錄和名稱。'
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- 通用對話方塊程式庫
- 通用對話方塊
- 開啟對話方塊
- '[另存新檔] 對話方塊'
- 自訂開啟對話方塊
- 自訂另存新檔] 對話方塊
- 對話方塊、開啟
- 對話方塊，另存新檔
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 57f1986f950650840ff3acfc9ee19191088e0dcbe099fc4cb8b21690fa0646c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606294"
---
# <a name="open-and-save-as-dialog-boxes"></a>開啟並另存新檔對話方塊

> [!NOTE]
> [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)函式會在檔案 [使用範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)中示範。

\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

[ **開啟** ] 對話方塊可讓使用者指定要開啟之檔案或檔案集合的磁片磁碟機、目錄和名稱。 您可以藉由初始化 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構並將結構傳遞至 [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)函式，來建立和顯示 **開啟** 的對話方塊。

[ **另存** 新檔] 對話方塊可讓使用者指定要儲存的磁片磁碟機、目錄和檔案名。 您可以藉由初始化 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構並將結構傳遞給 [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)函數，來建立並顯示 [**另存** 新檔] 對話方塊。

Explorer 樣式 [**開啟**] 和 [**另存** 新檔] 對話方塊提供類似于 Windows 檔案總管的使用者介面功能。 不過，系統會繼續支援舊版樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊，適用于必須與舊樣式使用者介面一致的應用程式。

除了外觀上的差異以外，Explorer 樣式和舊樣式的對話方塊在使用自訂範本和攔截程式以自訂對話方塊時不同。 不過，Explorer 樣式和舊樣式的對話方塊對於大部分基本作業都具有相同的行為，例如指定檔案名篩選、驗證使用者的輸入，以及取得使用者指定的檔案名。 如需有關 Explorer 樣式和舊樣式對話方塊的詳細資訊，請參閱 [開啟和另存](#open-and-save-as-dialog-box-customization)新檔對話方塊的自訂。

下圖顯示一般 Explorer 樣式的 **開啟** 對話方塊。

![開啟檔案對話方塊](images/opendialogboxxp.png)

下圖顯示典型的 Explorer 樣式 [ **另存** 新檔] 對話方塊。

![[儲存檔案] 對話方塊](images/saveasdialogboxxp.png)

如果使用者指定檔案名，然後按一下 [ **確定]** 按鈕， [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) 或 [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) 會傳回 **TRUE**。 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFile** 成員所指向的緩衝區包含使用者所指定的完整路徑和檔案名。

如果使用者取消 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊或發生錯誤，函數會傳回 **FALSE**。 若要判斷錯誤的原因，請呼叫 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值。 如果 **lpstrFile** 緩衝區太小而無法接收完整名稱， **CommDlgExtendedError** 會傳回 **FNERR \_ BUFFERTOOSMALL** ，而且 **lpstrFile** 成員指向之緩衝區的前2個位元組會設定為整數值，以指定接收完整名稱所需的大小。

本節將討論下列主題。

-   [檔案名和目錄](#file-names-and-directories)
-   [篩選條件](#filters)
-   [檔案和目錄驗證](#file-and-directory-validation)
-   [開啟並另存新檔對話方塊自訂](#open-and-save-as-dialog-box-customization)
-   [Explorer 樣式的勾點程式](#explorer-style-hook-procedures)
-   [Explorer 樣式的自訂範本](#explorer-style-custom-templates)
-   [Explorer 樣式控制項識別碼](#explorer-style-control-identifiers)
-   [自訂 Old-Style 對話方塊](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>檔案名和目錄

本節中的資訊適用于 Explorer 樣式和舊樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊。

在呼叫 [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)或 [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)函式之前， [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFile** 成員必須指向緩衝區才能接收檔案名。 **NMaxFile** 成員必須指定 **lpstrFile** 緩衝區的大小（以字元為單位）。 若為 ANSI 函數，這是位元組的數目，但對於 Unicode 函式，這是字元數。

如果使用者指定檔案名，然後按一下 [ **確定]** 按鈕，此對話方塊會將選取的磁片磁碟機、目錄和檔案名複製到 **lpstrFile** 緩衝區。 函式也會將 **nFileOffset** 和 **nFileExtension** 成員分別設定為從緩衝區開頭到檔案名和副檔名的位移（以字元為單位）。

若只取出檔案名和副檔名，請將 **lpstrFileTitle** 成員設定為指向緩衝區，並將 **nMaxFileTitle** 成員設定為緩衝區的大小（以字元為單位）。 或者，您可以在 [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea)函式的呼叫中傳遞 **lpstrFile** 緩衝區，以取得所選檔案的顯示名稱。 不過請注意， **GetFileTitle** 傳回的檔案名只有在使用者偏好顯示檔案名時，才會包含副檔名。

對話方塊會使用目前目錄做為呼叫進程的初始目錄，以從中顯示檔案和目錄。 您可以使用 [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) 和 [**>setcurrentdirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) 函數來取得和變更進程的目前的目錄。 若要指定不同的初始目錄，而不變更您目前的目錄，請使用 **lpstrInitialDir** 成員指定目錄的名稱。 當使用者選取不同的磁片磁碟機或目錄時，對話方塊會自動變更您目前的目錄。 若要防止對話方塊變更您目前的目錄，請設定 **OFN \_ NOCHANGEDIR** 旗標。 此旗標不會防止使用者變更目錄以尋找檔案。

若要指定預設副檔名，請使用 **lpstrDefExt** 成員。 如果使用者指定的檔案名沒有副檔名，對話方塊會加入您的預設副檔名。 如果您指定了預設副檔名，而使用者指定副檔名不同的檔案名，則對話方塊會設定 **OFN \_ EXTENSIONDIFFERENT** 旗標。

若要讓使用者從目錄中選取一個以上的檔案，請設定 **OFN \_ ALLOWMULTISELECT** 旗標。 為了與繼承應用程式相容，預設的多重選取對話方塊會使用舊樣式的使用者介面。 若要顯示 [Explorer 樣式的多重選取專案] 對話方塊，您也必須設定 **OFN \_ Explorer** 旗標。

如果使用者選取一個以上的檔案， **lpstrFile** 成員指向的緩衝區會傳回目前目錄的路徑，後面接著所選檔案的檔案名。 **NFileOffset** 成員是第一個檔案名的位移，且不會使用 **nFileExtension** 成員。 下表描述在傳回多個檔案名時，Explorer 樣式和舊樣式對話方塊之間的差異。



| 對話方塊樣式            | 描述                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Explorer 樣式對話方塊 | 目錄和檔案名字串會以 **null** 分隔，並在最後一個檔案名之後加上額外的 **Null** 字元。 此格式可讓 Explorer 樣式的對話方塊傳回包含空格的長檔名。 |
| 舊樣式對話方塊      | 目錄和檔案名字串會以空格分隔。 對於具有空格的檔案名，此函式會使用簡短的檔案名。                                                                                              |



 

您可以使用 [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) 函數，在 long 和 short 檔案名之間進行轉換。

如果您指定 **OFN \_ ALLOWMULTISELECT** ，而使用者只選取一個檔案，則 **lpstrFile** 字串的路徑和檔案名之間沒有分隔符號。

## <a name="filters"></a>篩選

本節中的資訊適用于 Explorer 樣式和舊樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊。

您可以提供檔案名篩選器，協助使用者限制對話方塊所顯示的檔案名。 檔案名篩選器是由一對以 null 終止的字串、描述和模式所組成，其中一個會串連至另一個。 對話方塊會顯示描述，讓使用者挑選要使用的篩選準則;它會使用模式來選取要顯示的檔案。

若要指定篩選，請將 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFilter** 成員設定為指向包含篩選字串組陣列的緩衝區。 陣列中的最後一個字串後面必須接著額外的 null 字元。

模式字串可以是有效檔案名字元和星號 () 的組合 \* 。 星號是萬用字元，代表有效檔案名字元的任何組合。 對話方塊只會顯示符合模式的檔案。 若要為相同的描述指定多個模式，您必須使用分號 (; ) 來分隔模式。 請注意，模式字串中的空白字元可能會產生非預期的結果。

下列程式碼片段會指定兩個篩選準則。 具有「來源」描述的篩選具有兩種模式。 如果使用者選取此篩選準則，對話方塊只會顯示具有的檔案。C 和。CXX 延伸模組。 請注意，在 C 程式設計語言中，以雙引號括住的字串會以 null 終止。


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **nFilterIndex** 成員會指定索引，以指出對話方塊一開始所使用的篩選準則。 緩衝區中的第一個篩選具有索引1，第二個則是2，依此類推。 如果使用者在使用對話方塊時變更篩選， **nFilterIndex** 成員就會在傳回時設定為所選篩選準則的索引。

您可以建立自訂篩選，方法是將 **lpstrCustomFilter** 成員設定為包含單一篩選的緩衝區位址，並將 **nMaxCustFilter** 成員設定為緩衝區的大小（以字元或位元組為單位）。 對話方塊一律會將自訂篩選準則放在篩選清單的開頭，而在傳回時，一律會以使用者選取之篩選準則的模式來更新篩選的模式部分。

若為 Explorer 樣式的對話方塊，當使用者選取不同的篩選時，預設的擴充功能可能會變更。 如果使用者選取的篩選器的第一個模式是表單 \* 。*xxx* (也就是，延伸不包含萬用字元) ，此對話方塊會使用 *xxx* 作為預設副檔名。 只有當您在 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrDefExt** 成員中指定了預設副檔名時，才會發生這種情況。 例如，如果使用者選取 [來源 \\ 0] \* 。C; \* 。CXX \\ 0 "filter，預設延伸模組會變更為" C "。 但是，如果您已經將篩選定義為「來源 \\ 0」 \* 。C \* \\ 0」，預設擴充功能不會變更，因為擴充功能包含萬用字元。

[**CDN \_ INCLUDEITEM**](cdn-includeitem.md)通知訊息提供另一種方式來篩選對話方塊所顯示的名稱。 若要使用此訊息，請在建立對話方塊時，提供 [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)攔截程式，並在 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構中指定 **OFN \_ ENABLEINCLUDENOTIFY** 旗標。 每次使用者開啟資料夾時，對話方塊都會針對新開啟的資料夾中的每個專案，將 **CDN \_ INCLUDEITEM** 通知傳送至您的勾點程式。 攔截程式的傳回值指出對話方塊是否應該在資料夾的專案清單中顯示專案。

## <a name="file-and-directory-validation"></a>檔案和目錄驗證

除了所述，本節中的資訊也適用于 Explorer 樣式和舊樣式的 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊。

對話方塊會自動驗證使用者輸入的檔案名，以確保名稱只包含有效的字元。 若要覆寫檔案名字元驗證，請設定 **OFN \_ NOVALIDATE** 旗標。

若要強制對話方塊確認使用者是否指定了現有檔案的名稱，請設定 **OFN \_ FILEMUSTEXIST** 旗標。 若要強制驗證指定的路徑存在，請設定 **OFN \_ PATHMUSTEXIST** 旗標。 如果您設定 **OFN \_ CREATEPROMPT** 旗標，對話方塊會提示使用者建立不存在的檔案的許可權。 如果設定此旗標，且使用者選擇建立新的檔案，則會關閉對話方塊，而且此函式會傳回指定的名稱。 否則，對話方塊會保持開啟狀態。

當您使用 [ **另存** 新檔] 對話方塊時，可以指示對話方塊提示使用者透過設定 **OFN \_ OVERWRITEPROMPT** 旗標來覆寫現有檔案的許可權。

根據預設，對話方塊會建立長度為零的測試檔案，以判斷是否可以在選取的目錄中建立新檔案。 若要避免建立此測試檔案，請設定 **OFN \_ NOTESTFILECREATE** 旗標。

如果您啟用攔截程式，此對話方塊會在使用者指定的檔案名發生網路共用違規時，通知您的攔截程式。 如果您設定 **OFN \_ EXPLORER** 旗標，此對話方塊會將 [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md)訊息傳送到攔截程式。 如果您未設定 **OFN \_ EXPLORER**，此對話方塊會將已註冊的 [**SHAREVISTRING**](sharevistring.md) 訊息傳送到攔截程式。 若要防止對話方塊傳送任何共用違規通知，請設定 **OFN \_ SHAREAWARE** 旗標。

如果使用者選取 [唯讀] 核取方塊，對話方塊會在傳回時設定 **OFN \_ READONLY** 旗標。 若要隱藏 [ **開啟為唯讀** ] 核取方塊，請 **設定 \_ OFN HIDEREADONLY** 旗標。 若要防止對話方塊傳回具有唯讀屬性之現有檔案的名稱，請設定 **OFN \_ NOREADONLYRETURN** 旗標。

若要防止對話方塊參考連結檔，請設定 **OFN \_ NODEREFERENCELINKS** 值。 在此情況下，對話方塊會傳回連結檔案的名稱，而不是連結檔案所參考的檔案名。

## <a name="open-and-save-as-dialog-box-customization"></a>開啟並另存新檔對話方塊自訂

您可以藉由提供攔截程式、自訂範本或兩者來自訂 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊。 不過，Explorer 樣式和舊樣式版本的對話方塊在使用自訂範本和攔截程式時不同。

如需自訂 Explorer 樣式對話方塊的詳細資訊，請參閱 [Explorer 樣式](#explorer-style-hook-procedures)的攔截程式、 [Explorer 樣式的自訂範本](#explorer-style-custom-templates)，以及 [explorer 樣式的控制項識別碼](#explorer-style-control-identifiers)。 如需自訂舊樣式對話方塊的詳細資訊，請參閱 [自訂 Old-Style 對話方塊](#customizing-old-style-dialog-boxes)。

下表摘要說明這兩種樣式之間的差異。



| 自訂                  | 描述                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Explorer 樣式的掛勾程式  | 攔截程式會接收從通用對話方塊傳送的通知訊息，以及您藉由指定子對話方塊範本所定義之任何其他控制項的訊息。 攔截程式不會接收預設對話方塊之標準控制項的訊息。 |
| Explorer 樣式的自訂範本 | 系統會使用自訂範本來建立子對話方塊。 範本可以定義其他控制項，也可以指定標準控制項叢集的位置。 自訂範本不會取代預設範本。                                          |
| 舊樣式的勾點程式       | 攔截程式會接收所有傳送至對話方塊的訊息，包括標準控制項和任何自訂控制項的訊息。 攔截程式也會接收從通用對話方塊傳送的已註冊訊息。                                                         |
| 舊樣式的自訂範本      | 自訂範本會取代預設範本。 藉由修改 Fileopen 檔案中指定的預設範本來建立自訂範本。                                                                                                                                  |



 

Explorer 樣式和舊樣式對話方塊的預設標題為 [**開啟**] 或 [**另存** 新檔]。 若要變更標題，請在 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrTitle** 成員中指定新的標題。

使用者的 **HKEY \_ 目前 \_ 使用者** 登錄 hive 可以包含值，這些值會自訂 Explorer 樣式 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊的內容。 這些登錄專案只會影響與登錄 hive 相關聯的使用者所顯示的對話方塊。

若要隱藏 Explorer 樣式 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊的功能，系統管理員可以在下列子機碼底下設定下表中的值：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
```



| 值名稱       | 值 | 意義                                  |
|------------------|-------|------------------------------------------|
| **NoPlacesBar**  | 1     | 隱藏位置列。                    |
| **NoFileMRU**    | 1     | 隱藏最近使用的 (MRU) 清單。 |
| **NoBackButton** | 1     | 隱藏 [ **上一步** ] 按鈕。               |



 

**位置** 列的內容取決於下列子機碼的內容：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
                     Placesbar
```

目前，此機碼下只能有五個專案，而值/名稱索引是以零為基底。 專案的名稱應為 Place0、Place1、Place2、Place3 和 Place4。 專案的值可以是 **REG \_ DWORD**、 **reg \_ SZ** 或 **reg \_ 展開 \_ SZ** 值，以識別要包含在位置列的位置。



| 值類型                         | 意義                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | 識別資料夾的 CSIDL 值。 如需 CSIDL 值的清單，請參閱 [**CSIDL 值**](../shell/csidl.md)。 |
| **REG \_SZ** 或 **REG \_ EXPAND \_ sz** | 以 null 終止的字串，指定有效的路徑。                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style 攔截程式

您可以藉由提供攔截程式、自訂範本或兩者來自訂 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊。 如果您為 Explorer 樣式的對話方塊提供攔截程式，系統會建立一個對話方塊，做為預設對話方塊的子系。 攔截程式可作為子對話方塊的對話方塊程式。 這個子對話方塊是以自訂範本為基礎，如果未提供則為預設範本。 如需詳細資訊，請參閱 [Explorer 樣式的自訂範本](#explorer-style-custom-templates)。

若要啟用 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的攔截程式，請在建立對話方塊時使用 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構。 在 **旗標** 成員中設定 **OFN \_ ENABLEHOOK** 和 **OFN \_ EXPLORER** 旗標，並在 **lpfnHook** 成員中指定 [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)攔截程式的位址。 如果您提供攔截程式並省略 **OFN \_ EXPLORER** 旗標，則必須使用 [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) 攔截程式，而您將會取得舊樣式的使用者介面。 如需詳細資訊，請參閱 [自訂 Old-Style 對話方塊](#customizing-old-style-dialog-boxes)。

當對話方塊開啟時，Explorer 樣式的勾點程式會收到各種訊息。 這些選項包括：

-   [**Wm \_ INITDIALOG**](wm-initdialog.md)訊息和其他標準對話方塊訊息，例如 [**wm \_ CTLCOLORDLG**](wm-ctlcolordlg.md) control color message。
-   一組 [**WM \_ 通知**](../controls/wm-notify.md) 通知訊息，表示使用者或其他對話方塊事件所採取的動作。
-   您藉由指定子對話方塊範本所定義之任何其他控制項的訊息。

此外，也有一組訊息可傳送至 Explorer 樣式的對話方塊，以取得資訊或控制對話方塊的行為和外觀。

如果您為 [Explorer 樣式] 對話方塊提供攔截程式，則預設對話方塊程式在處理其 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息時，會建立子對話方塊。 攔截程式可作為子對話方塊的對話方塊程式。 此時，攔截程式會收到自己的 **WM \_ INITDIALOG** 訊息，並將 *lParam* 參數設定為用來初始化對話方塊的 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構位址。 在子對話方塊完成處理自己的 **WM \_ INITDIALOG** 訊息之後，預設的對話方塊程式會視需要移動標準控制項，以騰出空間給子對話方塊的任何其他控制項。 接著，預設的對話方塊程式會將 [**CDN \_ INITDONE**](cdn-initdone.md)通知訊息傳送到攔截程式。

攔截程式會收到 [**WM \_ 通知**](../controls/wm-notify.md) 通知訊息，指出使用者在對話方塊中採取的動作。 您可以使用其中一些訊息來控制對話方塊的行為。 例如，當使用者選擇檔案名，然後按一下 [**確定]** 按鈕時，攔截程式就會收到 [**CDN 的 \_ FILEOK**](cdn-fileok.md)訊息。 為了回應此訊息，攔截程式可以使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式來拒絕選取的名稱，並強制對話方塊維持開啟狀態。

每個 [**WM \_ 通知**](../controls/wm-notify.md)訊息的 *lParam* 參數都是定義動作之 [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)或 [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構的指標。 此結構的標頭中的程式 **代碼** 成員包含下列其中一項通知訊息。



| 訊息                                           | 意義                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDN \_FILEOK**](cdn-fileok.md)                 | 使用者按一下 [ **確定]** 按鈕;對話方塊即將關閉。                                                                                                                                                                                                                          |
| [**CDN \_FOLDERCHANGE**](cdn-folderchange.md)     | 使用者開啟了新的資料夾或目錄。                                                                                                                                                                                                                                                     |
| [**CDN \_説明**](cdn-help.md)                     | 使用者按一下 [說明 **] 按鈕。**                                                                                                                                                                                                                                                          |
| [**CDN \_INCLUDEITEM**](cdn-includeitem.md)       | 決定是否應該顯示專案。 當使用者開啟新的資料夾或目錄時，系統會傳送此通知給資料夾或目錄中的每個專案。 只有在已設定 **OFN \_ ENABLEINCLUDENOTIFY** 旗標的情況下，系統才會傳送此通知。                          |
| [**CDN \_INITDONE**](cdn-initdone.md)             | 系統已完成對話方塊的初始化，而對話方塊已完成了 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息的處理。 此外，系統已完成在 [通用] 對話方塊中排列控制項，以騰出空間給子對話方塊的控制項， (是否有任何) 。 |
| [**CDN \_SELCHANGE**](cdn-selchange.md)           | 使用者從檔案清單中選取了新的檔案或資料夾。                                                                                                                                                                                                                                     |
| [**CDN \_SHAREVIOLATION**](cdn-shareviolation.md) | [一般] 對話方塊在要傳回的檔案上發生共用違規。                                                                                                                                                                                                        |
| [**CDN \_TYPECHANGE**](cdn-typechange.md)         | 使用者從檔案類型清單中選取了新的檔案類型。                                                                                                                                                                                                                                 |



 

這些 [**WM \_ 通知**](../controls/wm-notify.md)訊息會取代舊版 [**開啟**] 和 [**另存** 新檔] 對話方塊所使用的 [**FILEOKSTRING**](fileokstring.md)、 [**LBSELCHSTRING**](lbselchstring.md)、 [**SHAREVISTRING**](sharevistring.md)和 [**HELPMSGSTRING**](helpmsgstring.md)註冊的訊息。 但是，如果 **wm \_ 通知** 處理未使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)來設定非零的 **DWL \_ MSGRESULT** 值，則攔截程式也會在 **wm \_ 通知** 訊息之後收到被取代的訊息。

若要抓取對話方塊狀態的相關資訊，或控制對話方塊的行為和外觀，攔截程式可以將下列訊息傳送至對話方塊。



| 訊息                                             | 意義                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GETFILEPATH**](cdm-getfilepath.md)         | 抓取所選取檔案的路徑和檔案名。                                                                                                                                                                   |
| [**CDM \_ GETFOLDERIDLIST**](cdm-getfolderidlist.md) | 抓取對應至對話方塊已開啟之目前資料夾的專案識別碼清單。 如需專案識別碼清單的詳細資訊，請參閱 [Shell 命名空間的簡介](/windows/desktop/shell/namespace-intro)。 |
| [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md)     | 抓取對話方塊的目前資料夾或目錄的路徑。                                                                                                                                                |
| [**CDM \_ GETSPEC**](cdm-getspec.md)                 | 抓取檔案名 (不包含目前在對話方塊中選取之檔案的路徑) 。                                                                                                                       |
| [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md)         | 隱藏指定的控制項。                                                                                                                                                                                             |
| [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md)   | 設定指定之控制項中的文字。                                                                                                                                                                                  |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)             | 設定對話方塊的預設副檔名。                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style 自訂範本

若要定義 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的其他控制項，請使用 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構來指定子對話方塊的範本，其中包含其他控制項。 如果您的子對話方塊範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **OFN \_ ENABLETEMPLATE** 旗標，並使用該結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。 如果範本已在記憶體中，請設定 **OFN \_ ENABLETEMPLATEHANDLE** 旗標，並使用 **hInstance** 成員識別包含範本的記憶體物件。 提供 [Explorer 樣式] 對話方塊的子對話方塊範本時，您也必須設定 **OFN \_ explorer** 旗標; 否則，系統會假設您要提供舊樣式對話方塊的取代範本。 一般而言，如果您提供其他控制項，您也必須提供 [Explorer 樣式的勾點程式](#explorer-style-hook-procedures) 來處理新控制項的訊息。

您可以建立子對話方塊範本，就像您對任何其他範本一樣，不同的是，您必須指定 **ws \_ 子** 系和 **ws \_ CLIPSIBLINGS** 樣式，而且應指定 **ds \_ 3DLOOK** 和 **ds \_ 控制項** 樣式。 系統需要 **WS \_ 子** 樣式，因為您的範本定義了預設 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的子對話方塊。 **WS \_ CLIPSIBLINGS** 樣式可確保子對話方塊不會在 [預設] 對話方塊中的任何控制項上繪製。 **DS \_ 3DLOOK** 樣式可確保子對話方塊中控制項的外觀，與 [預設] 對話方塊中的控制項一致。 **DS \_ 控制項** 樣式可確保使用者可以使用索引標籤和其他流覽鍵，在自訂對話方塊中的所有控制項（預設或自訂）之間移動。

為了騰出空間給新的控制項，系統會依自訂對話方塊的寬度和高度來展開預設對話方塊。 根據預設，自訂對話方塊中的所有控制項都位於 [預設] 對話方塊的控制項底下。 不過，您可以覆寫這個預設位置，方法是在自訂對話方塊範本中包含靜態文字控制項，並為其指派 **stc32** 的控制項識別碼值。  (此值定義于 Dlgs .h 標頭檔中。 ) 在此情況下，系統會使用控制項作為參考點，以決定要在何處放置新的控制項。 **Stc32** 控制項上方和左邊的所有新控制項，都位於 [預設] 對話方塊中控制項的上方和左邊。 **Stc32** 控制項右邊和右邊的新控制項位於預設控制項的下方和右邊。 一般情況下，每個新控制項都位於相同的位置，使其具有與 **stc32** 控制項相同的預設控制項位置。 為了為這些新的控制項騰出空間，系統會視需要在預設對話方塊的左邊、右邊、底端和頂端加上空格。

系統會要求攔截程式處理所有適用于自訂對話方塊的訊息，因此會將相同的視窗訊息傳送至與其他任何對話方塊程式相同的攔截程式。 例如，當使用者按一下 [自訂] 對話方塊中的按鈕控制項時，攔截程式就會收到 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。 當對話方塊關閉時，攔截程式會負責初始化這些控制項，以及從控制項中取出值。 請注意，當攔截程式收到 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息時，系統尚未將控制項移至其最終位置。

預設對話方塊程式會處理 [預設] 對話方塊中所有控制項的訊息，但是攔截程式會接收這些控制項上使用者動作的通知訊息，如 [Explorer 樣式](#explorer-style-hook-procedures)的攔截程式中所述。

## <a name="explorer-style-control-identifiers"></a>Explorer-Style 控制項識別碼

Windows 軟體開發套件 (SDK) 提供舊樣式對話方塊的預設對話方塊範本，但不包含 Explorer 樣式對話方塊的預設範本。 這是因為 [Explorer 樣式] 對話方塊可讓您加入自己的控制項，但不支援修改標準控制項的範本。 不過，在某些情況下，您可能需要知道預設範本中所使用的控制項識別碼。 例如， [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md) 和 [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md) 訊息需要控制項識別碼。

下表顯示 [Explorer] 樣式 [ **開啟** ] 和 [ **另存** 新檔] 對話方塊中標準控制項的識別碼。 識別碼是定義于 Dlgs .h 和 Winuser 中的常數。



| 控制項識別碼 | 控制項描述                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | 唯讀核取方塊                                                                                                                                                                                                                                                                    |
| **cmb1**           | 顯示檔案類型篩選清單的下拉式清單方塊                                                                                                                                                                                                                            |
| **stc2**           | **Cmb1** 下拉式方塊的標籤                                                                                                                                                                                                                                                           |
| **cmb2**           | 顯示目前磁片磁碟機或資料夾的下拉式方塊，可讓使用者選取要開啟的磁片磁碟機或資料夾                                                                                                                                                                |
| **stc4**           | **Cmb2** 下拉式方塊的標籤                                                                                                                                                                                                                                                           |
| **cmb13**          | 下拉式方塊中顯示目前檔案的名稱，可讓使用者輸入要開啟的檔案名，然後選取最近開啟或儲存的檔案中的檔案名。 這適用于不含攔截器或對話方塊範本的舊版瀏覽器相容應用程式。 與 **edt1** 比較。 |
| **edt1**           | 編輯控制項，以顯示目前檔案的名稱，或允許使用者輸入要開啟的檔案名。 與 **cmb13** 比較。                                                                                                                                                  |
| **stc3**           | **Cmb13** 下拉式方塊和 edt1 編輯控制項的標籤                                                                                                                                                                                                                                |
| **lst1**           | 顯示目前磁片磁碟機或資料夾內容的清單方塊                                                                                                                                                                                                                         |
| **stc1**           | **Lst1** 清單方塊的標籤                                                                                                                                                                                                                                                            |
| **IDOK**           | [ **確定]** 命令按鈕 (push 按鈕)                                                                                                                                                                                                                                                     |
| **IDCANCEL**       | [ **取消** ] 命令按鈕 (推入按鈕)                                                                                                                                                                                                                                                 |
| **pshHelp**        | [ **說明** ] 命令按鈕 (push 按鈕)                                                                                                                                                                                                                                                   |



 

## <a name="customizing-old-style-dialog-boxes"></a>自訂 Old-Style 對話方塊

您可以藉由提供 [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))攔截程式來自訂舊樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊，以接收適用于預設對話方塊程式的訊息或通知。 您也可以提供用來取代預設範本的自訂範本。 與舊樣式對話方塊搭配使用的攔截程式和範本，類似于與其他通用對話方塊搭配使用的連結。 如需詳細資訊，請參閱 [一般對話方塊](customizing-common-dialog-boxes.md) 和 [自訂範本](customizing-common-dialog-boxes.md)的攔截程式。

若要針對舊版樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊啟用攔截程式，請在建立對話方塊時使用 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構。 在 **旗標** 成員中設定 **OFN \_ ENABLEHOOK** 旗標，並在 **lpfnHook** 成員中指定 [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))攔截程式的位址。 對話方塊程式會將 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息傳送至攔截程式，並將 *Param* 參數設定為用來初始化對話方塊的 **OPENFILENAME** 結構位址。

您可以使用 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) 結構來指定 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的自訂範本，以用來取代預設範本。 如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **OFN \_ ENABLETEMPLATE** 旗標，並使用該結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。 如果您的自訂範本已在記憶體中，請設定 **OFN \_ ENABLETEMPLATEHANDLE** 旗標，並使用 **hInstance** 成員來識別包含範本的記憶體物件。 藉由修改 Fileopen 檔案中指定的預設範本來建立自訂範本。 在 [預設尋找和取代] 對話方塊範本中使用的控制項識別碼是在 Dlgs 檔案中定義。

根據預設， [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) 和 [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) 函式會顯示 Explorer 樣式的對話方塊。 如果您想要顯示舊樣式的對話方塊，您必須提供 [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))的攔截程式，並確定未在 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **旗標** 成員中設定 **OFN \_ EXPLORER** 旗標。

如果您設定 **OFN \_ explorer** 旗標，系統會將攔截程式或自訂範本視為 EXPLORER 樣式的自訂。 如需自訂 Explorer 樣式對話方塊的詳細資訊，請參閱 [Explorer 樣式的自訂範本](#explorer-style-custom-templates)。

## <a name="see-also"></a>另請參閱

* [檔案使用中範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)