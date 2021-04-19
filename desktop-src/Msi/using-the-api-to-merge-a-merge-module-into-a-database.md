---
description: 合併模組提供一種標準方法，可讓開發人員將共用的 Windows Installer 元件和設定邏輯傳遞給其應用程式。
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: 使用 API 將合併模組合併至資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68298671045825dda41ad120896fa22c89f068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987680"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>使用 API 將合併模組合併至資料庫

[合併模組](merge-modules.md) 提供一種標準方法，可讓開發人員將共用的 Windows Installer [*元件*](c-gly.md) 和設定邏輯傳遞給其應用程式。 合併模組必須合併為使用合併工具的安裝套件。 最好的替代方法是取得自由散發的合併工具，或購買獨立軟體廠商提供的其中一個合併工具。 例如，您可以使用 [Mergemod.dll](merge-module-automation.md)所提供的功能。

依序使用下列步驟，透過 [Mergemod.dll](merge-module-automation.md)的 API 將合併模組合併到 Windows Installer 安裝資料庫中。

**將合併模組合併到 Windows Installer 安裝資料庫**

1.  使用 [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog)開啟記錄檔。 只有當您需要為合併進程建立記錄檔或附加現有的記錄檔時，才需要執行此步驟。
2.  開啟安裝資料庫（ [.msi](windows-installer-file-extensions.md)檔案），該檔案將會使用 [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase)接收合併模組。 這是必要步驟。
3.  開啟使用 [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule)合併到資料庫的 merge 模組（ [.msm](windows-installer-file-extensions.md)檔案）。 必須先開啟模組，才能與安裝資料庫合併。 這是必要步驟。
4.  使用 [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) 或 [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex)將模組合併至安裝資料庫。 請注意， **merge** 或 **MergeEx** 只能呼叫一次，以合併 .msi 和 .msm 檔案的特定組合。 只有在使用 [Mergemod.dll 2.0 版](merge-module-automation.md)或更新版本，且只有在使用 [IMsmMerge2](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2)介面時，才能使用 **MergeEx** 。 這是必要步驟。
5.  呼叫 [**取得 \_ 錯誤**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) ，並檢查針對合併衝突或其他錯誤所抓取的錯誤收集。 抓取是非破壞性的。 您可以重複讀取呼叫的 **get \_ 錯誤**，以抓取錯誤集合的多個實例。 您將需要解決適合您案例的任何錯誤。
6.  將合併模組的元件與已經或將使用 [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect)合併到安裝資料庫中的任何其他功能產生關聯。 在呼叫這個方法之前，功能必須已經存在。 只有當您有其他功能時，才需要此步驟。如需詳細資訊，請參閱將 [合併模組連接到多項功能](connecting-a-merge-module-to-multiple-features.md)
7.  如有必要，請執行下列一或多個動作，以從模組中解壓縮原始程式檔。

    若要從內嵌的 .cab 檔解壓縮檔案，然後將檔案複製到指定的目錄中，請使用 [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) 或 [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex)。 請注意， **ExtractFilesEx** 需要 [Mergemod.dll 2.0 版](merge-module-automation.md) 或更新版本。

    若要從內嵌的 .cab 檔解壓縮檔案，然後儲存在指定的檔案中，請使用 [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab)。

    若要從模組解壓縮檔案，然後在合併之後複製到磁片上的來源映射，請使用 [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage)。 請注意， **CreateSourceImage** 僅適用于 [Mergemod.dll 2.0 版](merge-module-automation.md) 或更新版本。

8.  使用 [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule)關閉目前的開啟合併模組。 這是必要步驟。
9.  使用 [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase)關閉目前開啟的安裝資料庫。 這是必要步驟。 關閉資料庫會清除所有相依性資訊，但不會影響任何未取出的錯誤。
10. 使用 [**CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog)關閉目前的記錄檔。 如果您已開啟記錄檔，則需要此步驟。

使用 [Mergemod.dll](merge-module-automation.md)將模組合併到資料庫之後，必須更新 [媒體資料表](media-table.md) 以描述所需的來源影像版面配置。 Mergemod.dll 提供的合併處理不會更新媒體資料表，因為合併模組的取用者可以選取各種配置來源影像的方式。

 

 
