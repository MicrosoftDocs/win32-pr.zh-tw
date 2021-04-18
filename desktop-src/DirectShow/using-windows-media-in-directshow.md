---
description: 在 DirectShow 中使用 Windows Media
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: 在 DirectShow 中使用 Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104386324"
---
# <a name="using-windows-media-in-directshow"></a>在 DirectShow 中使用 Windows Media

本節說明如何使用 DirectShow 來播放和寫入 Advanced 系統格式 (ASF) 檔。 ASF 檔案通常包含使用 Windows Media 音訊和影片編解碼器編碼的音訊和影片內容。 不過，ASF 可以包含任何類型的資料。

下列 DirectShow 篩選器支援讀取和寫入 ASF 檔案：

-   [WM ASF 讀取器篩選器](wm-asf-reader-filter.md)。 讀取 ASF 檔。
-   [WM ASF 寫入器篩選器](wm-asf-writer-filter.md)。 Wrties ASF 檔案。
-   [Sql-dmo 包裝](dmo-wrapper-filter.md)函式篩選。 包裝 Windows Media 編碼器和解碼器 DMOs。

### <a name="versions"></a>版本

WM ASF 讀取器和 WM ASF 寫入器篩選器封裝在名為 qasf.dll 的 DLL 中，而篩選器統稱為「QASF 元件」。 這些篩選器是 Windows Media Format SDK 的包裝函式。 DLL (qasf.dll) 先在 DirectX SDK 中發佈，但稍後會在 Windows Media Format SDK 中更新。 以下是 QASF 篩選的版本歷程記錄：

-   DirectShow 8.1 支援 Windows Media Format SDK 7.0 版。
-   DirectShow 9.0 支援 Windows Media Format SDK 7.1 版。
-   Windows XP Service Pack 2 支援 Windows Media Format 9 SDK。
-   Windows Vista 支援 Windows Media Format 11 SDK。
-   Windows Media Format 9 SDK 和更新版本包含 QASF 的對應版本。

若要取得最新版本的 QASF，請一律下載最新的 Windows Media Format SDK。

### <a name="legacy-windows-media-source-filter"></a>舊版 Windows Media 來源篩選

在 Windows XP Service Pack 1 及更早版本中，適用于 ASF 檔案的預設來源篩選 ( .asf、.wmv 和 .wma 副檔名) 是過時的 [Windows Media 來源篩選](windows-media-source-filter.md)。 維護此行為的目的，是為了確保與使用 Windows Media Player 6.4 的應用程式回溯相容。 新的應用程式應該使用較新版本的 QASF，這會讓 WM ASF 讀取器篩選播放 ASF 檔案的預設篩選器。

如需有關 Windows Media 套件軟體發展工具組的詳細資訊，請參閱 MDSN 文件庫的 [音訊和影片](../audio-and-video.md) 章節。

本文包含下列主題：

-   [在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
-   [在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow](using-directshow.md)
</dt> </dl>

 

 
