---
title: 在 Web 網頁中使用 Windows Media Player 控制項
description: 在 Web 網頁中使用 Windows Media Player 控制項
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
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
- 網頁內嵌，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc418e715563591ad5ab51265f27086d4980fb54887ff797b0a108e25dc925f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116948"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a>在 Web 網頁中使用 Windows Media Player 控制項

在網頁中內嵌 Windows Media Player 控制項可讓您完全自訂使用者與控制項互動的方式。 您可以使用控制項所提供的介面，也可以隱藏它並顯示您自己的使用者介面。 您可以在內嵌控制項的位置指定多個 Windows Media Player 控制項屬性，也可以在腳本中設定玩家屬性和呼叫 player 方法。

下列各節說明在網頁中內嵌控制項的基本概念。



| 區段                                                                                                        | 描述                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [隱藏 Windows Media Player 控制項](hiding-the-windows-media-player-control.md)                         | 描述當您想要提供您自己的使用者介面時，隱藏 Windows Media Player 控制項的選項。               |
| [OBJECT 元素中的 PARAM 元素](param-elements-in-an-object-element.md)                                 | 描述如何在內嵌 Windows Media Player 控制項時將它初始化。                                                   |
| [在網頁中編寫腳本的簡單範例](simple-example-of-scripting-in-a-web-page.md)                     | 描述簡單但完整的內嵌播放機控制項與自訂使用者介面的範例。                             |
| [搭配 Firefox 使用 Windows Media Player 控制項](using-the-windows-media-player-control-with-firefox.md) | 說明如何將 Windows Media Player 控制項內嵌在網頁中，以供 Firefox 瀏覽器正確顯示。 |
| [使用 Windows Media Player 搭配 Netscape 7.1](using-windows-media-player-with-netscape-7-1.md)               | 說明如何搭配使用 Windows Media Player 控制項與 Netscape 7.1 和其他以 Gecko 為基礎的網頁瀏覽器。                       |



 

> [!Note]  
> Windows Media Player 10 行動裝置版控制項包含的功能，是以 Windows Media Player 控制項的桌上出版本提供的功能子集為基礎。 因此，它可以內嵌于 Pocket Internet Explorer 網頁，就像桌面控制項內嵌在 Internet Explorer 網頁中一樣。 若要瞭解 Windows Media Player 10 個行動控制項是否支援特定的方法、屬性或事件，請參閱[腳本的物件模型參考](object-model-reference-for-scripting.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**播放機控制指南**](player-control-guide.md)
</dt> </dl>

 

 




