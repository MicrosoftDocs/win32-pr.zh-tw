---
title: 文字顯示類型
description: 文字顯示類型
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Windows Media Player 行動外觀、文字
- 外觀中的文字、顯示類型
- 外觀，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672576"
---
# <a name="text-display-types"></a>文字顯示類型

您不需要在面板中包含文字顯示，但您可能會想要在許多情況下。 例如，您可能想要包含搜尋字幕，讓使用者移至媒體專案中的任何位置，但您也可能想要包含文字顯示，以顯示自目前媒體專案開始播放以來經過的秒數。

**顯示方塊**

以下是 text 元素可以顯示的數個屬性：

-   Time
-   播放清單
-   Track\#
-   \#軌道
-   標題
-   作者
-   著作權
-   檔案名稱
-   FilenameExt
-   Bitrate
-   頻率
-   狀態
-   VolPercent

如需文字顯示類型的詳細資訊，請參閱外觀參考的 [文字](text.md) 區段。

**滾動字幕**

除了使用個別的文字專案，您還可以將一或多個屬性結合成滾動文字字幕。 如果您想要在社區域中顯示相關的文字資訊群組，這會很有用。 例如，您可以在字幕中顯示標題、作者和著作權資訊。

如需建立文字字幕的詳細資訊，請參閱面板參考的 [ [字幕]](marquee.md) 區段。

**狀態顯示**

另一種類型的文字顯示是狀態顯示。 這可讓您自動顯示 Windows Media Player Mobile 目前狀態的相關資訊。 例如，當媒體專案為緩衝時，狀態顯示會通知使用者，讓播放程式很容易就能正常運作。

下列訊息會出現在狀態顯示中：

-   緩衝
-   Connecting
-   已暫停
-   正在播放
-   就緒
-   已停止

> [!Note]  
> 播放媒體專案時，狀態顯示會透過子標題、演出者、專輯、內容類型和目前的位元速率來旋轉。

 

如需透過 Status 元素建立狀態顯示的詳細資訊，請參閱面板參考的 [狀態](status.md) 區段。不過，建議您在 Text 元素中使用 status 屬性，而不要使用 Status 元素。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player 行動功能**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




