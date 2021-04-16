---
description: 列印介面的主要元件是列印多工緩衝處理器。
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: 列印多工緩衝處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcc6ea2e46c06b5e51032a4c43f46df7f07c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513444"
---
# <a name="print-spooler"></a>列印多工緩衝處理器

列印介面的主要元件是列印多工緩衝處理器。 列印多工緩衝處理器是一個可執行檔，可管理列印程式。 列印的管理包括取出正確印表機驅動程式的位置、載入該驅動程式、將高階函式呼叫緩衝處理到列印工作、排程列印工作以進行列印等等。 系統會在系統啟動時載入多工緩衝處理器，並繼續執行，直到作業系統關閉為止。

列印 (DC) 的印表機建立印表機裝置內容的應用程式。 當應用程式建立印表機 DC 時，多工緩衝處理器會執行必要的工作，例如判斷所需的印表機驅動程式的位置，然後載入該驅動程式。 列印多工緩衝處理器也會決定用來記錄列印工作的資料類型。

列印多工緩衝處理器支援下列資料類型：

-   增強型中繼檔 (EMF) 。
-   ASCII 文字。
-   原始資料，包括印表機資料類型，例如 PostScript、PCL 和自訂資料類型。

您可以藉由安裝額外的印表機驅動程式和列印處理器，將自訂資料類型新增至多工緩衝處理器。 列印工作是在內部儲存的檔，並使用其中一種支援的資料類型進行編碼，而列印工作可包含一或多個頁面的輸出。 列印工作可能包含多個表單;例如，作業可能包含一個信封和三頁的 A4 紙張。 列印工作的定義 (或由 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 和 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 函式) 括住。

列印工作的預設資料類型是增強的中繼檔。 EMF 記錄是精簡結構，可用來儲存文字輸出命令、點陣圖形命令等等。 當應用程式呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)時，多工緩衝處理器會建立多工緩衝處理檔案和資料檔案，然後開始將 EMF 記錄儲存在多工緩衝處理檔案中。 每次應用程式呼叫其中一個 GDI 繪圖函式時，就會建立一或多個新的 EMF 記錄，並儲存在多工緩衝處理檔案中。 多工緩衝處理和資料檔案會建立在作業系統目錄中。 多工緩衝處理器會使用多工緩衝處理檔案來儲存 EMF 記錄，並使用資料檔案來記錄表單類型、列印工作的資料類型、目標印表機等等。 當工作已順利列印時，多工緩衝處理器會刪除這些檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強格式的中繼檔](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
