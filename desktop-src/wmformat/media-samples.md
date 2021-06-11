---
title: '媒體範例 (Windows Media Format 11 SDK) '
description: 深入瞭解 Windows Media Format 11 SDK 中的媒體範例。 媒體範例是一個物件，其中包含零或多個緩衝區的已排序清單。
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK，媒體範例
- Windows Media Format SDK，範例
- Advanced Systems Format (ASF) 、媒體範例
- ASF (Advanced 系統格式) 、媒體範例
- Advanced Systems Format (ASF) 、範例
- ASF (Advanced Systems Format) ，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989067"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>媒體範例 (Windows Media Format 11 SDK) 

媒體範例（或範例）是數位媒體資料的區塊。 範例是讀取和寫入 Windows Media 格式 SDK 的物件所操作的基本單位。 個別範例的內容是由與範例相關聯的媒體類型所決定。 在影片中，每個範例都代表一個畫面格。 若是音訊，個別樣本中的資料量是在用來建立 ASF 檔案的設定檔中設定。

範例可以包含未壓縮的資料，也可以包含壓縮的資料，在這種情況下，它們稱為 *串流範例*。 建立 ASF 檔案時，您會將範例傳遞給寫入器。 寫入器會以適當的編解碼器來協調範例的壓縮，並將壓縮的資料排列在 ASF 檔案的 [資料] 區段中。 在播放時，讀取器會讀取壓縮的資料，並將其解壓縮，並提供重新重建的未壓縮資料作為輸出範例。

Windows Media 格式 SDK 所使用的所有範例都會封裝在由 SDK 執行時間元件自動設定其記憶體的緩衝區物件中。 您也可以視需要使用寫入器和讀取器的 advanced 功能來配置自己的緩衝區。

**注意** 此 SDK 中使用「詞彙範例」來參考媒體範例，而非音訊範例。 在音訊編碼中，範例是指單一編碼的音訊值。 一般而言，編碼的音訊品質是以每秒的樣本數來指定。 例如，CD 品質音效會記錄在每秒44100個樣本。 此值通常會以 Hz 標記法縮寫，因此每秒44100個樣本會是 44100 Hz 或 44.1 kHz。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](concepts.md)
</dt> <dt>

[**INSSBuffer 介面**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




