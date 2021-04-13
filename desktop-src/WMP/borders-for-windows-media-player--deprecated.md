---
title: Windows Media Player (已淘汰) 的框線
description: Windows Media Player (已淘汰) 的框線
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player、框線
- Windows Media Player 的外觀、框線
- 外觀、框線
- 框線，相較于外觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300820"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Windows Media Player (已淘汰) 的框線

本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。

框線與面板類似，但不是取代 Windows Media Player compact 模式的使用者介面，而是在完整模式 Windows Media Player 的 [立即播放] 窗格中內嵌框線。

藉由使用 Windows Media 下載套件，您可以包含具有框線的內容，paving 多媒體應用程式的方式。

包含框線和內嵌內容的範例 Windows Media 下載套件包含在此 SDK 的範例目錄中。

## <a name="creating-a-border"></a>建立框線

框線的建立方式與外觀相同。 唯一的差別是，面板內嵌在 [ **立即播放** ] 窗格內。 這表示無法計算外觀大小，而且所有的面板元素都必須是相對的。 如果使用者調整 Windows Media Player 的大小，則框線的某些部分可能會遭到裁剪，而且看不到。

## <a name="loading-a-border"></a>載入框線

載入使用 **面板元素的** Windows Media 中繼檔時，會載入框線。 面板 **元素的** **HREF** 屬性必須參考面板。 一般的 **外觀** 元素如下所示：


```C++
<SKIN HREF="myborder.wmz">

```



如需詳細資訊，請參閱 (已淘汰的面板 [元素) ](skin-element--deprecated.md)。

## <a name="including-content-with-a-border"></a>包含具有框線的內容

您可以使用 Windows Media 下載檔案 (副檔名為 wmd 的) ，來包含內容。 請遵循下列步驟：

1.  建立框線。 請小心建立它，使其調整大小不會損毀框線的組合。 例如，請勿包含背景檔案;使背景變成透明，讓視覺效果可以在它背後執行。
2.  將面板內容 (藝術、JScript 檔案和麵板定義檔) 壓縮至副檔名為 wmz 的檔案中。
3.  使用副檔名為 .asx (的副檔名) 來建立 Windows Media 中繼檔 (，其會參考副檔名為 wmz 的) 檔。 中繼檔可以包含播放清單資訊，其中包含適用于特定內容之藝術和 Url 的中繼資料。
4.  組合數位媒體內容。
5.  將框線、中繼檔和內容壓縮成一個檔案，並提供副檔名為 wmd 的檔案名。

## <a name="using-a-border"></a>使用框線

當您建立 Windows Media 下載檔案之後，使用者只需按兩下該檔案。 檔案將會下載到使用者的電腦。 封裝內的檔案將會解除封裝，播放清單會加入播放清單中，框線會出現在完整模式 Windows Media Player 的 [ **立即播放** ] 窗格中，且新播放清單上的第一個專案會開始播放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於外觀**](about-skins.md)
</dt> <dt>

[**範例**](samples.md)
</dt> <dt>

[**(淘汰的 Windows Media 下載套件)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




