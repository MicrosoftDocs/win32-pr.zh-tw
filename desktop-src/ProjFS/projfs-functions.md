---
title: ProjFS 函式
description: 下列函數是在 projectedfslib 中宣告。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 47e4371a7d00ca6564223f7415a69ee0308bf8757041b49f5df9f214e6c978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792605"
---
# <a name="projfs-functions"></a>ProjFS 函式

下列函數是在 projectedfslib 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | 配置符合虛擬化實例儲存裝置記憶體一致性需求的緩衝區。 |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | 清除虛擬實例的負路徑快取（如果有作用中）。 |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | 表示提供者已完成處理先前傳回 HRESULT_FROM_WIN32 (ERROR_IO_PENDING) 的回呼。 |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | 讓提供者刪除已在本機檔案系統上快取的專案。 |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | 判斷名稱是否包含萬用字元。 |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | 比較兩個檔案名，並傳回值，指出它們的相對定序順序。 |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | 判斷檔案名是否符合搜尋模式。 |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | 提供某個檔案或目錄的資訊給列舉。 |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | 提供一個檔案或目錄的相關資訊給列舉，並讓呼叫者指定延伸的資訊。 |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | 釋放已配置的緩衝區。 |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | 取得檔案或目錄的磁片上檔狀態。 |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | 抓取虛擬化實例的相關資訊。 |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | 將現有目錄轉換成目錄預留位置。 |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | 設定 ProjFS 虛擬化實例並啟動它，使其可供服務 i/o 使用，並在提供者上叫用回呼。 |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | 停止執行中的 ProjFS 虛擬化實例，使其無法供服務 i/o 使用，或涉及提供者的回呼。 |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | 讓提供者更新已在本機檔案系統上快取的專案。 |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | 將檔案內容傳送至 ProjFS。 |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | 將檔案或目錄中繼資料傳送至 ProjFS。 |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | 將檔案或目錄中繼資料傳送至 ProjFS，並允許呼叫者指定擴充資訊。 |
