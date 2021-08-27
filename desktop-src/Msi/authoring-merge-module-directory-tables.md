---
description: 合併模組可以套用至 .msi 檔案，將目錄新增至安裝，但是無法取代或移除任何現有的目錄。
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: 撰寫合併模組目錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90768dff191b729d482f8ddd58a821a6ed440e79fcd1453ff412aaf7b8a76fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086268"
---
# <a name="authoring-merge-module-directory-tables"></a>撰寫合併模組目錄資料表

合併模組可以套用至 .msi 檔案，將目錄新增至安裝，但是無法取代或移除任何現有的目錄。 [目錄資料表](directory-table.md)會指定合併模組提供給目標安裝之目錄的版面配置。 每個合併模組都需要目錄資料表。

在合併模組中撰寫目錄資料表時，請使用下列指導方針。 如需詳細資訊，請參閱 [目錄資料表](directory-table.md) 和 [使用目錄資料表](using-the-directory-table.md)。

-   合併模組新增的目錄結構必須有單一根目錄。 根目錄必須命名為 TARGETDIR。 使用者可能會在合併期間變更 TARGETDIR 的值，以指定要將模組目錄結構附加至目標目錄樹狀結構的位置。
-   目錄資料表以外的合併模組資料表不能直接參考要 TARGETDIR 的目錄位置。 如果使用者變更了 TARGETDIR 的值，這類參考的位置就會變更。
-   合併模組中的資料表必須參考 TARGETDIR 的子目錄位置，或合併模組樹狀結構中的另一個目錄。 執行下列動作，將 TARGETDIR 指定為合併模組中目錄的父系。 在 [目錄] 資料行中輸入目錄，然後在目錄父資料行中輸入 TARGETDIR \_ 。 在 DefaultDir 資料行中使用 "." 標記法，以表示此目錄位於沒有子目錄的 TARGETDIR 中。 如需詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。
-   合併模組新增的目錄名稱必須使用在 [合併模組資料庫中命名主鍵](naming-primary-keys-in-merge-module-databases.md)所述的命名慣例。 這包括依屬性（例如 [**SystemFolder**](systemfolder.md) 屬性和 [**ProgramFilesFolder**](programfilesfolder.md) 屬性）預先定義的目錄。
-   將 [*GUID*](g-gly.md)附加至目錄資料表中的每個專案 (但 TARGETDIR 除外。 ) 這包含指定 Windows Installer [**SystemFolder**](systemfolder.md)屬性的目錄資料表專案，例如 SystemFolder. 00000000 \_ 0000 \_ 0000 \_ 0000 \_ 000000000000。 程式庫 Mergemod.dll 會新增自訂動作來設定 **SystemFolder** 屬性。
-   當合併模組中包含預先定義的目錄時，合併工具會自動將 [自訂動作類型 51](custom-action-type-51.md) 新增至目標資料庫。 合併模組作者必須確定也包含 [CustomAction 資料表](customaction-table.md) 。 CustomAction 資料表可能是空的，但此資料表必須存在於目標資料庫中，並確保修改過的預先定義目錄會寫入正確的位置。 例如，當合併模組中包含系統目錄時，合併模組作者必須確定自訂動作資料表是否存在。

    請注意，產生這些類型51自訂動作的相符演算法只會檢查目錄名稱的開頭是否為其中一個預先定義的 [**SystemFolder**](systemfolder.md) 屬性。 它不會驗證目錄名稱是否與 directory 屬性完全相等。 任何以這些標準資料夾名稱開頭的任何目錄都會取得類型51自訂動作，即使名稱的其餘部分不是 GUID 也一樣。 作者必須注意，這不會在以其中一個 **SystemFolder** 屬性開頭的衍生主鍵上產生錯誤的正面相符專案，以及非預期的自訂動作產生。

以下是合併模組中的目錄資料表和預期的已解析目錄範例。



| 目錄                                              | 目錄 \_ 父系                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | TARGETDIR                                        | .： MMM \_ 進程 |
| SystemFolder. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | TARGETDIR                                        | MMM \_ Sys    |
| Dir02. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Dir00. BC82E350 \_ C7FC \_ 11d1 \_ A848 \_ 006097ABDE17 | MFC \_ OCX    |



 

具有上述目錄資料表的合併模組預期會產生下列目錄結構。



| 目錄                                              | 目標                                     | 來源                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[合併模組的安裝點\]\\         | \[合併模組的來源點 \] \\ MMM \_ 進程           |
| SystemFolder. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[合併模組的來源點 \] \\ MMM \_ Sys            |
| Dir02. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[合併模組的安裝點 \] \\ MFC \_ OCX | \[合併模組的來源點 \] \\ MMM \_ 程式 \\ MFC \_ OCX |



 

 

 



