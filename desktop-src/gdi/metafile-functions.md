---
description: 下列函式會搭配增強格式的中繼檔使用。
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: 中繼檔函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512872"
---
# <a name="metafile-functions"></a>中繼檔函式

下列函式會搭配增強格式的中繼檔使用。



| 函式                                                             | 描述                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | 關閉增強型中繼檔的裝置內容。                                                                            |
| [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | 將增強格式中繼檔的內容複寫到指定的檔案。                                                |
| [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | 建立增強格式中繼檔的裝置內容。                                                              |
| [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | 刪除增強格式的中繼檔或增強格式的中繼檔控制碼。                                             |
| [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | 搭配 EnumEnhMetaFile 函式使用的應用程式定義回呼函數。                                       |
| [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | 列舉增強格式中繼檔內的記錄。                                                             |
| [**GdiComment**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | 從緩衝區將批註複製到指定的增強格式中繼檔。                                              |
| [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | 建立控制碼，以識別儲存在指定檔案中的增強格式中繼檔。                            |
| [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | 抓取所指定增強格式中繼檔的內容，並將其複製到緩衝區。                        |
| [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | 從增強格式的中繼檔抓取選擇性的文字描述，並將字串複製到指定的緩衝區。 |
| [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | 抓取記錄，其中包含指定之增強格式中繼檔的標頭。                                 |
| [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | 從指定的增強中繼檔抓取選用的調色板專案。                                               |
| [**GetMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | GetMetaFile 不再適用于 Windows 2000。 相反地，請使用 [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)。  |
| [**GetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | 將增強格式的記錄從中繼檔轉換成 Windows 格式記錄。                                      |
| [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | 顯示以指定的增強格式中繼檔儲存的圖片。                                                 |
| [**PlayEnhMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | 藉由執行記錄所識別的 (GDI) 函式，來播放增強的中繼檔記錄。 |
| [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | 從指定的資料建立以記憶體為基礎的增強格式中繼檔。                                               |
| [**SetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | 將中繼檔從舊版 Windows 格式轉換成新的增強格式。                                          |



 

## <a name="obsolete-functions"></a>過時的函式

下列函式已過時。 提供與 Windows 格式中繼檔的相容性。

-   [**CloseMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**CopyMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**CreateMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**DeleteMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**EnumMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**EnumMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**GetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**PlayMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**PlayMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**SetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
