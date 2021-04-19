---
description: 視應用程式而定，當地語系化可能需要修改或新增資源（例如檔案或登錄機碼）。
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: 新增當地語系化的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7646499e4bb48e3df9fc1527bff1273e6b6784bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974650"
---
# <a name="adding-localized-resources"></a>新增當地語系化的資源

視應用程式而定，當地語系化可能需要修改或新增資源（例如檔案或登錄機碼）。 範例應用程式 MNP2000 的當地語系化需要將一個額外的檔案新增至封裝、Fre.txt，以及兩個現有檔案的法文版本： Help.txt 和 Readme.txt。

在此情況下，最佳作法是將封裝當地語系化，讓英文和法文版本可以安全地共存于電腦上。 這包括永遠不會將兩個具有相同檔案名的不同檔案安裝在相同的目錄中。 由於 Help.txt 和 Readme.txt 在兩個語言版本中都有相同的檔案名，因此法文套件應該將這些檔案安裝到與英文不同的目錄中。

法文套件會將 Help.txt 安裝到 RedPark 資料夾的新子目錄中，也就是法文。 因為新增 Fre.txt 會將資源新增至原始說明元件，所以法文和英文套件中的說明元件的元件程式碼必須不同。 請參閱 [變更元件程式碼](changing-the-component-code.md)中元件程式碼的規則。

法文套件會將 Readme.txt 安裝到目錄法文中，如此一來，此檔案名就不會與英文版發生衝突。 檔案 Readme.txt 是與 [記事本] 元件一起安裝，但是元件規則不需要變更元件程式碼。 在此範例中，[記事本] 的元件程式碼不應該變更，因為 RedPark.exe （登錄 [表](registry-table.md)中指定的登錄值）都是由這兩種語言版本所共用。 請參閱 [新增登錄資訊](adding-registry-information.md)。

從原始程式檔移除英文版的 Help.txt 和 Readme.txt，並新增 Help.txt、Readme.txt 和 Fre.txt 的法文版。 當地語系化的封裝應該將檔案的安裝從來源對應到目標，如下所示。



| 檔案        | 描述                  | 來源的路徑                   | 目標路徑                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | 文字編輯器可執行檔。 | C： \\ 範例 \\ Notepad \\Redpark.exe | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 法文 \\Redpark.exe |
| Readme.txt  | 資訊檔。       | C： \\ 範例 \\ Notepad \\Readme.txt  | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 法文 \\Readme.txt  |
| Help.txt    | 協助手動                  | C： \\ 範例 \\ Notepad \\Help.txt    | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 法文 \\Help.txt    |
| Fre.txt     | 電話清單                   | C： \\ 範例 \\ Notepad \\Fre.txt     | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 法文 \\Fre.txt     |



 

使用 SDK 或其他編輯器提供的資料庫編輯器 Orca 來開啟目錄表格，並新增安裝新目錄的記錄（法文）。

[目錄資料表](directory-table.md)



| 目錄                                        | 目錄 \_ 父系                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | 藝術：活動       |
| HOLDIR                                           | MONDIR                                           | .：假日        |
| MENUDIR                                          | NOTEPADDIR                                       | 功能表              |
| MONDIR                                           | NOTEPADDIR                                       | 門              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | 紅色 \_ 公園：記事本 |
| SPORTDIR                                         | NOTEPADDIR                                       | 運動：活動     |
| FRENCHDIR                                        | NOTEPADDIR                                       | 法語：。          |



 

您可以使用資料表編輯器，將 MNPFren.msi 中的 [說明] 元件的元件變更為新的 GUID。

[元件資料表](component-table.md)



| 元件 | ComponentId                            | 目錄\_ | 屬性 | 條件 | Keypath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| 棒球  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| 演唱會   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| 舞蹈     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| 足球  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Help      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| 一月   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| [記事本]   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

您可以使用資料表編輯器，將 Fre.txt 加入 MNPFren.msi 的檔案 [資料表](file-table.md) 中。 在當地語系化檔案的 [語言] 欄位中輸入法文的 LANGID。 所有其他專案都相等，如果所安裝的檔案與電腦上的檔案具有不同的語言，則安裝程式會使用符合所要安裝產品的語言來表示檔案。 中性語言的檔案會被視為另一種語言，因此會再次接受安裝的產品。 如需詳細資訊，請參閱檔案 [版本控制規則](file-versioning-rules.md)。

[FileTable](file-table.md)



| 檔案         | 元件\_ | FileName     | FileSize | 版本 | 語言 | 屬性 | 順序 |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | 棒球    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | 演唱會     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | 舞蹈       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | 足球    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Help        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | 一月     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | [記事本]     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | [記事本]     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Help        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

這會完成範例當地語系化。

 

 



