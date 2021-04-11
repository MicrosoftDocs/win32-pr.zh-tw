---
description: 非同步篩選範例
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: 非同步篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025780"
---
# <a name="async-filter-sample"></a>非同步篩選範例

## <a name="description"></a>Description

非同步篩選範例是支援漸進式下載的檔案讀取器篩選器。 此範例篩選準則會執行 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 和 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) 介面。 它支援 MPEG 檔案，但非 AVI 檔。

## <a name="usage"></a>使用方式

此範例包含示範篩選的小型命令列應用程式 Memfile.exe。 命令列引數會指定媒體檔案和位元速率（以每秒 kb 數為單位）。 應用程式會以指定的速率將檔案讀取到記憶體中，然後播放該檔案。 若要這樣做，它會建立篩選的實例、將篩選準則加入至篩選圖形，然後轉譯篩選的輸出圖釘。

在命令列輸入：

**Memfile 檔案名位元速率**  

非同步範例篩選不支援 AVI 檔案，因為它無法連接到 [Avi 分隔](avi-splitter-filter.md) 器篩選器。 非同步篩選的輸出圖釘會建議 \_ \_ 媒體類型的媒體類型，並 MEDIASUBTYPE Null。 AVI 分隔器篩選器上的輸入 pin 不接受 MEDIASUBTYPE \_ Null，且不會建議任何類型。 因此，pin 連接會失敗。 可以增強非同步篩選，以 \_ 在適當時提供 MEDIASUBTYPE Avi。 例如，它可以檢查檔案格式，或使用副檔名。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： \[ *SDK 根* \] \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 非同步。

## <a name="related-topics"></a>相關主題



[DirectShow 範例](directshow-samples.md)


 

 



