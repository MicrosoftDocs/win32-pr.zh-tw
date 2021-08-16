---
title: 管理檔案和資料
description: 使用者可以更輕鬆地存取 Windows 7 中的檔案和資料。
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9091a2d9bb2cf01d4f9b514c55e78f2f989f01d6d64a929608e14c32bfd395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086655"
---
# <a name="managing-files-and-data"></a>管理檔案和資料

使用者可以更輕鬆地存取 Windows 7 中的檔案和資料。 新的 api 讓檔案和視圖更具資訊性，讓應用程式能夠將相關且特殊的資訊提供給 Windows 檔案總管。 此外，應用程式也受益于新的連結 *庫* 模型、比資料夾更抽象的使用者儲存空間概念，也可以參與不同應用程式共用的類似檔案類型的通用程式庫。

## <a name="libraries"></a>程式庫

Windows 7 引進了連結 *庫* 作為目的地的概念，讓開發人員和終端使用者可以在本機電腦和遠端電腦上的多個位置，將其資料當作專案集合來尋找和組織。

連結 *庫* api 提供簡單的方式，讓開發人員建立應用程式，以在應用程式內建立、互動和支援連結 *庫* 做為第一級專案。 也可以使用 [資料夾選擇器] 對話方塊來選取連結 *庫*。 應用程式可以列舉相關的程式庫範圍，也可以直接使用程式庫做為資料夾。  (參閱[Windows 程式庫](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85))和[Windows 7 程式庫：開發人員資源](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)) 。

![windows 7 圖片庫](images/windows7-10.jpg)

*圖片媒體* 櫃會顯示您的圖片，無論其儲存位置為何

## <a name="file-formats-and-data-stores"></a>檔案格式和資料存放區

在 Windows 7 中，Windows 檔案總管以數種方式讓使用者更容易進行檔案管理和操作：

-   您可以使用新的按鈕，讓使用者顯示及隱藏預覽窗格，以存取應用程式檔案類型的預覽。
-   沉浸式視覺效果堆疊會匯總視圖中檔案類型的縮圖影像。
-   WindowsExplorer 視圖會根據以您的屬性處理常式撰寫的屬性來顯示有用的資訊。
-   檔程式碼片段和搜尋結果醒目提示會使用您的 **IFilter** 介面執行，讓搜尋和尋找檔案變得更容易。
-   內容功能表動詞和命令比以往更容易執行。

藉由為您的通訊協定處理常式所傳回的專案，執行所有適當的格式處理常式，來自自訂資料存放區的搜尋結果可能會與檔案中的搜尋結果一樣豐富。 系統會自動為您的通訊協定處理常式建立連結 *庫*，讓使用者可以輕鬆地範圍搜尋。 您可以透過登錄輕鬆地自訂建立連結 *庫* 的邏輯。  (請參閱[開發 Windows Search 的篩選](../search/-search-3x-wds-extidx-filters.md)。 ) 

![windows 7 文件庫](images/windows7-11.jpg)

在 Windows 7 中，Windows 檔案總管可讓檔案管理和操作變得更容易

 

 