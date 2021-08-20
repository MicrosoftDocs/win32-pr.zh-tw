---
description: 合併模組提供標準的方法，讓您提供共用的 Windows Installer 元件，並將設定邏輯傳遞給應用程式。
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: 使用 Automation 將合併模組合併至資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513a765670df44396c34537721eb6f75ed98796dd31ddefd5d26387e2a6b5d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141327"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>使用 Automation 將合併模組合併至資料庫

[合併模組](merge-modules.md)提供標準的方法，讓您提供共用的 Windows Installer [*元件*](c-gly.md)，並將設定邏輯傳遞給應用程式。

合併模組必須使用合併工具合併為安裝套件。 最佳做法是取得自由散發的合併工具，或購買可從獨立軟體廠商取得的其中一個合併工具，例如，您可以使用 [Mergemod.dll](merge-module-automation.md)。

下列程式示範如何使用[合併模組自動化](merge-module-automation.md)，將合併模組合併到 Windows Installer 資料庫。

**將模組合併至資料庫**

1.  使用 [**OpenLog**](merge-openlog.md) 方法來開啟記錄檔。

    只有當您需要建立記錄檔，或為合併進程附加現有的記錄檔時，才需要執行此步驟。

2.  使用 [**Merge 物件**](merge-object.md)的 [**OpenDatabase**](merge-opendatabase.md)方法，開啟 [.msi](windows-installer-file-extensions.md)安裝資料庫。

    這是必要步驟。

    您所開啟的資料庫是您想要接收合併模組的資料庫。

3.  使用 [**OpenModule**](merge-openmodule.md)方法來開啟 [.msm](windows-installer-file-extensions.md)合併模組。

    這是必要步驟。

    這是合併到資料庫的合併模組。 必須先開啟模組，才能與安裝資料庫合併。

4.  藉由呼叫 [**merge**](merge-object.md) 方法或 [**MergeEx**](merge-mergeex.md) 方法，將模組合併至安裝資料庫。

    這是必要步驟。

    [**Merge**](merge-object.md)方法或 [**MergeEx**](merge-mergeex.md)方法只能呼叫一次，以合併 [.msi](windows-installer-file-extensions.md)和 .msm 檔案的特定組合。

    > [!Note]  
    > [**MergeEx**](merge-mergeex.md)方法只能在 [Mergemod.dll 2.0 版](merge-module-automation.md)或更新版本中使用，而且只有在使用 [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2)介面時才可使用。

     

5.  抓取 [**Errors**](merge-errors.md) 屬性，並檢查它針對合併衝突或其他錯誤所傳回之 [**錯誤**](error-object.md) 物件的集合。

    您必須解決任何錯誤。

    抓取是非破壞性的，而且可以藉由重複讀取 [**Errors**](merge-errors.md) 屬性來抓取錯誤集合的多個實例。

6.  使用 [**連線**](merge-connect.md)方法，將 merge 模組的元件與功能產生關聯。

    只有當您有現有的功能，而且想要新增功能以合併至安裝資料庫時，才需要執行此步驟。

    在您呼叫這個方法之前，必須先有一項功能。 如需詳細資訊，請參閱將 [合併模組連接至多個功能](connecting-a-merge-module-to-multiple-features.md)。

7.  如有必要，請執行下列一或多個動作，以從模組中解壓縮原始程式檔：
    -   使用 [**ExtractFiles**](merge-extractfiles.md) 或 [**ExtractFilesEx**](merge-extractfilesex.md) 從內嵌的 .cab 檔案解壓縮檔案，然後複製到指定的目錄中。
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) 需要 [Mergemod.dll 2.0 版](merge-module-automation.md) 或更新版本。

         

    -   使用 [**ExtractCAB**](merge-extractcab.md) 從內嵌的 .cab 檔案解壓縮檔案，然後儲存在指定的檔案中。
    -   使用 [**CreateSourceImage**](merge-createsourceimage.md) 從模組解壓縮檔案，然後在合併之後，複製到磁片上的來源映射。
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) 僅適用于 [Mergemod.dll 2.0 版](merge-module-automation.md) 或更新版本。

         
8.  使用 [**CloseModule**](merge-closemodule.md) 方法，關閉目前的開啟合併模組。

    這是必要步驟。

9.  使用 [**CloseDatabase**](merge-closedatabase.md) 方法來關閉開啟的安裝資料庫。

    這是必要步驟。

    關閉資料庫會清除所有相依性資訊，但不會影響任何未取出的錯誤。

10. 使用 [**CloseLog**](merge-closelog.md) 方法來關閉目前的記錄檔。

    如果您有開啟的記錄檔，則需要此步驟。

使用 [Mergemod.dll](merge-module-automation.md)將模組合併到資料庫之後，必須更新 [媒體資料表](media-table.md) 以描述所需的來源影像版面配置。 Mergemod.dll 提供的合併處理不會更新媒體資料表，因為合併模組的取用者可以選取各種配置來源影像的方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



