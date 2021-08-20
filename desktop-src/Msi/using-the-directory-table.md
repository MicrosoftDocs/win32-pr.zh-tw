---
description: 目錄資料表會指定安裝的版面配置。
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: 使用目錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f550f32006df16db5811e0fbf5022253373a4b1551983ddda2db55655b4061f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141317"
---
# <a name="using-the-directory-table"></a>使用目錄資料表

[目錄資料表](directory-table.md)會指定安裝的版面配置。 當您在 [CostFinalize 動作](costfinalize-action.md)期間解析目錄時，目錄資料表中的索引鍵會變成將 [屬性](properties.md) 設為目錄路徑。 請注意，安裝程式會將一些標準 [屬性](properties.md) 設定為系統資料夾路徑。 如需設定為系統資料夾的屬性清單，請參閱 [屬性參考](property-reference.md) 。

若要指定目錄的目標位置，最好的方式是在安裝套件中撰寫 [目錄表格](directory-table.md) ，以提供本節所述的正確位置。 如果需要在安裝時變更目錄位置，請參閱「[變更目錄的目標位置](changing-the-target-location-for-a-directory.md)」一節。

以下是目錄資料表的範例。



| 目錄     | 目錄 \_ 父系 | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| EXEDIR        | TARGETDIR         | 應用程式        |
| DLLDIR        | EXEDIR            | 量化        |
| DesktopFolder | TARGETDIR         | 桌面    |



 

目錄資料表的每個資料列都表示來源與目標的目錄。 例如，假設安裝套件位於 \\ \\ 應用程式 \\ 來源 \\ 。 因為 \_ 第一個資料列的目錄父欄位是 Null，所以此記錄會指出來源和目標的根目錄。 針對來源，這個目錄的值是由 DefaultDir 欄位提供。 [**SourceDir**](sourcedir.md)屬性預設為安裝套件的位置。 因此，除非覆寫 **SourceDir** 屬性，否則根目錄來原始目錄是 \\ \\ 應用程式 \\ 來源 \\ 。

第一筆記錄的目錄欄位指出根目標目錄的位置。 在此情況下， [**TARGETDIR**](targetdir.md) 屬性的值會指出此目錄。 一般而言， **TARGETDIR** 屬性的值是在命令列或透過使用者介面設定。 在此情況下，假設 **TARGETDIR** 屬性設定為 C： \\ Program Files \\ Target \\ 。

若為第二筆記錄，目錄 \_ 父欄位不是 Null。 因此，此記錄表示來源和目標的非根目錄。 針對非根目錄來原始目錄，目錄父欄位中所述的記錄所指定的來原始目錄 \_ 是父目錄。 若為第二筆記錄，則 \_ 會 TARGETDIR 目錄父欄位。 如先前所示，TARGETDIR 記錄所指示的來原始目錄已解析為 \\ \\ 應用程式 \\ 來源 \\ 。 因此，第二筆記錄所指出的來原始目錄是 \\ \\ 應用程式 \\ 來源 \\ 應用程式 \\ 。

類似的進程適用于目標目錄。 第二筆記錄中所描述之目標目錄的上層目錄值是目錄父欄位所解析的目標目錄 \_ 。 同樣地，目錄 \_ 父欄位包含值 TARGETDIR。 這表示第一筆記錄會解析為 C： \\ Program Files 目標的目標 \\ 目錄 \\ 。 目錄欄位包含作者定義的屬性，稱為 EXEDIR。 如果設定此屬性，則其值會提供目錄的完整路徑。 因此，如果這個屬性設定為 C： \\ data \\ common，則 \\ 第二筆記錄所指出的目標目錄值為 c： \\ data \\ common \\ 。 如果未設定，目標目錄會採用 DefaultDir 欄位所提供的名稱。 在此情況下，目標目錄為 C： \\ Program Files \\ 目標 \\ 應用程式 \\ 。

相同的進程適用于第三筆記錄。 如果未設定 EXEDIR 和 DLLDIR，則目標目錄為 C： \\ Program Files \\ 目標應用 \\ 程式 \\ bin，而來原始目錄是 \\ \\ 應用程式 \\ 來源應用程式 \\ \\ bin \\ 。

第四筆記錄使用 [**DesktopFolder**](desktopfolder.md) 屬性。 如果使用者的桌面位置為 C： \\ winnt \\ 設定檔 \\ 使用者 \\ 桌面 \\ ，則目標目錄會解析為 c： \\ winnt \\ 設定檔 \\ 使用者 \\ 桌面 \\ 。 來原始目錄會解析為 \\ \\ 應用程式 \\ 來源 \\ 桌面 \\ 。

目錄資料表的 DefaultDir 資料行中有兩種額外的語法功能可供使用。 若為非根來原始目錄， (. ) 在 DefaultDir 資料行中輸入，表示該目錄應該位於其上層目錄，而不含子目錄。 若要指定不同的來源和目標目錄路徑，請以冒號分隔 DefaultDir 資料行中的目標和來源路徑，如下所示： \[ targetpath \] ： \[ sourcepath \] 。 這些功能可以一起使用，以將層級新增至單一目錄的來源或目標路徑。 請參閱下列目錄資料表範例。



| 目錄   | 目錄 \_ 父系 | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| MyAppDir    | TARGETDIR         | MyApp      |
| BinDir      | MyAppDir          | 量化        |
| Binx86Dir   | BinDir            | .： x86      |
| BinAlphaDir | BinDir            | .： Alpha    |



 

MyAppDir、BinDir、Binx86Dir 和 BinAlphaDir 資料列的來源和目標路徑會解析為，如下所示。



| Record       | 目標路徑            | 來源路徑                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[SourceDir \] MyApp             |
| BinDir:      | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin        |
| Binx86Dir:   | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ x86   |
| BinAlphaDir: | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ Alpha |



 

> [!Note]  
> Windows Installer 不支援 Alpha 平臺。

 

 

 



