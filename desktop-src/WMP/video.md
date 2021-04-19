---
title: '影片 (Windows Media Player SDK) '
description: 影片
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player 行動外觀、影片
- 外觀、影片
- 外觀、影片的參考
- 外觀影片，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106994968"
---
# <a name="video-windows-media-player-sdk"></a>影片 (Windows Media Player SDK) 

影片顯示器可讓使用者查看數位視訊檔案。 只有當影片現正播放或暫停時，才會顯示影片顯示區域。 當您設計面板時，您會想要在背景影像中保留空間，以包含影片顯示。 如果您沒有這麼做，則影片顯示器可能會顯示在任何可見的圖片上，例如背景檔案、按鈕和 trackbars，這會讓使用者無法操作您面板上的控制項。

面板定義檔的 [影片] 區段必須以以下這一行開頭：


```C++
[ Video ]

```



然後，您必須加入一行，以指定面板中影片顯示區域的位置和大小。


```C++
0,38,240,172

```



您可以使用下列範本作為面板定義檔的影片區段：


```C++
//  <Location>
//  ----------

```



下列各節提供進一步的詳細資料。

-   [影片位置](video-location.md)
-   [影片影像來源](video-image-source.md)
-   [影片大小](video-size.md)
-   [範例影片區段](sample-video-section.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




