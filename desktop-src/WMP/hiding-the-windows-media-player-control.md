---
title: 隱藏 Windows Media Player 控制項
description: 隱藏 Windows Media Player 控制項
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player，內嵌 ActiveX 控制項
- Windows Media Player 物件模型，內嵌 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media PlayerMobile、內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項、內嵌
- Windows Media PlayerMobile ActiveX 控制項，內嵌
- ActiveX 控制項，內嵌
- Windows Media Player ActiveX 控制項、網頁
- Windows Media PlayerMobile ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- 內嵌、網頁
- Windows Media Player，隱藏 ActiveX 控制項
- Windows Media Player 物件模型，隱藏 ActiveX 控制項
- 物件模型，隱藏 ActiveX 控制項
- Windows Media PlayerMobile、hidingActiveX 控制項
- Windows Media Player ActiveX 控制項，隱藏
- Windows Media PlayerMobile ActiveX 控制項，隱藏
- ActiveX 控制項，隱藏
- Windows Media Player ActiveX 控制項、網頁
- Windows Media PlayerMobile ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- 內嵌、隱藏 ActiveX 控制項的網頁
- 隱藏 Windows Media Player ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb0b29bbbc1b2eb978c5bd9f29a58aa02bf629d5c6befe9f1dc68bbc92d280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339179"
---
# <a name="hiding-the-windows-media-player-control"></a>隱藏 Windows Media Player 控制項

Windows Media Player 的 ActiveX 物件是使用 object 元素內嵌在網頁中。 與舊版不同的是，定義 Windows Media Player 的物件元素必須放在網頁的 [主體] 區段中，介於 <BODY> 及 </BODY> 標籤。 將 Windows Media Player 的 ActiveX 物件放在網頁的標頭區段中，以隱藏使用者介面可能會產生非預期的結果。

如果您將 Windows Media Player ActiveX 控制項放在網頁的 [主體] 區段中，將會顯示控制項使用者介面。 如果您不想要顯示它，而且想要建立自己的使用者介面，請將物件元素的高度和寬度屬性設定為零。

藉由設定 *播放* 程式，也可以隱藏控制項。**uiMode** 屬性設為「隱藏」。 您可以使用下一節所討論的 PARAM 標記來完成這項操作。 在此情況下，會使用高度和寬度為控制項保留空間，但在 **uiMode** 變更為「不可見」的專案之前，不會在保留空間中顯示任何內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 Web 網頁中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




