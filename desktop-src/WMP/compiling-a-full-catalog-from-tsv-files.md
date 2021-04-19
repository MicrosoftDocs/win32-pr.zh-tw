---
title: 從 TSV 檔案編譯完整目錄
description: 從 TSV 檔案編譯完整目錄
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player 線上商店，編譯目錄
- 線上商店，編譯目錄
- 輸入1個線上商店，編譯目錄
- Windows Media Player 線上商店，TSV 檔案
- 線上商店，TSV 檔案
- 輸入1個線上商店，TSV 檔案
- Windows Media Player 線上商店，catcomp.exe
- 線上商店、catcomp.exe
- 輸入1個線上商店，catcomp.exe
- catcomp.exe
- 編譯目錄
- tab 鍵分隔值 (TSV) 檔案
- TSV (定位字元分隔值) 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106968082"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>從 TSV 檔案編譯完整目錄

新的目錄是從一組定位鍵分隔值 (TSV) 檔案建立。 檔案必須採用 Unicode 格式。 將下列所需的 TSV 檔案放入資料夾中， (catcomp.exe) 的輸入路徑引數，並使用下列語法呼叫 catcomp.exe：


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



如果未提供版本號碼，則版本號碼會設定為0。 如果未提供任何地區設定識別碼，則會使用系統地區設定。 如果只提供一個數值選擇性引數，則會假設為版本號碼。 如果指定 debug，畫面的輸出將會提供更詳細的診斷資訊。

例如，下列程式碼會從 C： CatalogData 210 中的檔案編譯 \\ 目錄 \\ ，並為目錄提供210版的版本號碼：


```C++
catcomp C:\CatalogData\210 210
```



若要顯示更詳細的錯誤訊息，可以新增選擇性的 debug 引數，如下所示：


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>必要的 TSV 檔案

下列每個檔案都必須存在，但是如果沒有檔案的資料，就可以使用空的檔案。 比方說，如果您的目錄不包含任何電臺通道，radio.csv 可以是空的。 檔案的命名必須與列出的完全相同。

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> 雖然檔案名必須有 .csv 副檔名，但檔案不是以逗號分隔值 (CSV) 格式。 檔案必須位於 Tab 分隔值 (TSV) 格式。

 

如果編譯成功，catcomp.exe 會建立三個輸出檔。



| 檔案名稱                   | 描述                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog. wmdb                | 未壓縮的已編譯目錄。                                                                                                                                                      |
| catalog. wmdb. lz             | 壓縮格式的目錄。 您的外掛程式可將此檔案的位置提供給 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)中的 Windows Media Player。 |
| 編譯的 \_ 唯一 \_words.txt | 中繼輸出檔。 Windows Media Player 未使用。                                                                                                                      |



 

 

 




