---
description: 範圍篩選範例
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: 範圍篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a931238b21dd604e7ca5de7943fcb2e85446f002a04ea0826dee9322dc6c7100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951957"
---
# <a name="scope-filter-sample"></a>範圍篩選範例

## <a name="description"></a>Description

範圍篩選器是以 wave 形式顯示音效資料的轉譯器篩選器。

## <a name="usage"></a>使用方式

若要使用此篩選器，請開啟 GraphEdit，然後轉譯音訊檔案 (或包含音訊串流) 的影片檔案。 暫時中斷音訊轉譯器的連線，並) 範例篩選器中插入 Infinite-Pin 的 t ([InfTee 濾波器範例](inftee-filter-sample.md) 。 重新連線音訊轉譯器。 然後將 Infinite-Pin 指標的第二個輸出圖釘連接至範圍篩選器。 現在執行圖形。

範圍視窗會實作為對話方塊，而不是實際的視窗。 建立控制台以即時改變篩選參數的開發人員，可能會想要使用像這樣的技巧，而不是屬性頁。

範圍篩選器會示範如何設定個別的執行緒來處理資料。 在此情況下，資料只會複製到 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法上的另一個緩衝區，然後在另一個執行緒的範圍視窗上進行繪製。

範圍篩選器也可讓您監視音訊輸出，以判斷您是否正在裁剪，以便調整增益。

此篩選器會以 "示波器探棒" 的形式出現在 GraphEdit 中。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的[Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow樣品](directshow-samples.md)
</dt> </dl>

 

 



