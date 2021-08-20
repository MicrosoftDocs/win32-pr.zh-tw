---
title: SeekThumb 檔案
description: SeekThumb 檔案
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Windows Media Player行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于外觀、SeekThumbd 檔案的美工檔案
- Windows Media Player行動外觀、SeekThumb 檔
- 外觀，SeekThumb 檔
- 面板中的 SeekThumb 檔案
- thumb、SeekThumb 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de49bf3a93b5dd3a538fc98c824e274547bf97a883c4255322336c2ba23b54cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933721"
---
# <a name="seekthumb-file"></a>SeekThumb 檔案

SeekThumb 檔案會定義影像，指出搜尋的播放程式在媒體專案內的播放位置。 您可以使用一個檔案並定義它，以供 SeekThumb 和 VolumeThumb 使用。 與其他美工檔案不同的是，thumb 檔案是在外觀定義檔的 Trackbars 區段中定義。

下圖是一般的 SeekThumb 檔案。

![seekthumb 檔案](images/cesdksee.gif)

這兩個按鈕檔看起來相同，但大小稍有不同。 左邊的影像是使用者看到的一般觀點，而右邊的影像則是使用者在按下按鈕時所看到的推播影像。

> [!Note]  
> 針對 Windows Media Player 10 行動裝置版或更新版本中所使用的面板所建立的 SeekThumb 檔案，必須有下列三個映射 (從左至右) ： normal、推送和停用。

 

您可能會想要讓 thumb 影像的特定區域變成透明的。 這可讓您在矩形以外的圖形中建立 thumb 影像。 您以 RGB 值255、0、255所指定的色彩填滿的任何 thumb 影像區域，在您的面板中將會顯示為透明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**美工檔案**](art-files-mobile.md)
</dt> </dl>

 

 




