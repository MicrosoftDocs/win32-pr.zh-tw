---
description: Orca.exe 是用來建立和編輯 Windows Installer 封裝和合併模組的資料庫資料表編輯器。
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f1b0d31936bf81e60efd8eb9799ddb30b4d5a6f78363e2ff5d3d638ae40c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082678"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe 是用來建立和編輯 Windows Installer 封裝和合併模組的資料庫資料表編輯器。 此工具會提供用於驗證的圖形化介面，並反白顯示驗證錯誤或警告發生的特定專案。

此工具僅適用于[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。 它是以 Orca.msi 檔案的形式提供。 安裝適用于 Windows Installer 開發人員的 Windows SDK 元件之後，請按兩下 Orca.msi 以安裝 Orca.exe 檔。

## <a name="syntax"></a>Syntax

**orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>命令列選項

Orca.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。



| 選項 | 描述                                                 |
|--------|-------------------------------------------------------------|
| -Q     | 無訊息模式                                                  |
| -S     | <*database*> 架構資料庫 \[ "orca"-預設\] |
| -?     | 說明對話方塊                                                 |



 

Orca.exe 在合併模組中使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。 執行 merge 時，-f、-m 和 <*sourcefile*> 全部都是必要的。



| 選項     | 描述                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | 如果沒有錯誤，請將 merge 認可至資料庫。                                     |
| -!         | 即使發生錯誤，也會將合併認可至資料庫。                       |
| -M         | <*模組*> 合併模組以合併到資料庫。                      |
| -f         | 功能 \[ ： Feature2 \] 功能 (s) 連接到合併模組。                |
| -r         | <模組根重新導向的 *目錄識別碼*> 目錄專案。    |
| -X         | <*目錄*> 將檔案解壓縮至目錄下的映射。         |
| -g         | <用來開啟模組的 *語言*> 語言。                         |
| -l         | <*記錄* 檔> 要作為記錄檔的檔案，如果已經存在，則附加。      |
| -i         | <*目錄*> 將檔案解壓縮至目錄下的來源映射。 |
| -cab       | <*檔案名*> 將 .msm 封包解壓縮至檔案。                        |
| -lfn       | 在解壓縮期間使用長檔名。                                 |
| -設定 | <*檔案名*> 使用檔案中的資料來設定模組。            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



