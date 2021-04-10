---
title: ID3 支援
description: ID3 是定義一組標準的組織，可在 MPEG 層-3 (MP3) 音訊檔案中包含中繼資料。
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK，ID3 支援
- Advanced Systems Format (ASF) 、ID3 支援
- ASF (Advanced Systems Format) 、ID3 支援
- 中繼資料、ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675112"
---
# <a name="id3-support"></a>ID3 支援

ID3 是定義一組標準的組織，可在 MPEG 層-3 (MP3) 音訊檔案中包含中繼資料。 Windows Media 格式 SDK 的物件會提供 ID3 相容屬性的支援。 支援三種不同的 ID3 版本： ID3v1. x、ID3v 2.2 和 ID3v 2.3/v2、4。 如需等同于 ID3 框架的屬性清單，請參閱 [Id3 標記支援](id3-tag-support.md)。

除非另有說明，否則此 SDK 的物件不會執行 ID3 框架資料的驗證。 例如，中繼資料屬性 [**WM/歌詞 \_ 內容**](wm-lyrics-synchronised.md) 會儲存歌曲歌詞與對應的時間戳記。 寫入 **WM/歌詞 \_ 內容** 屬性時，此 SDK 的物件將不會檢查，以確保時間戳記是以時間順序排列，或是執行任何種類的驗證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> <dt>

[**中繼資料功能**](metadata-features.md)
</dt> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




