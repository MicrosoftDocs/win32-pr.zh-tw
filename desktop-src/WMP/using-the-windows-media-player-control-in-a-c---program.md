---
title: 在 c + + 程式中使用 Windows Media Player 控制項
description: 在 c + + 程式中使用 Windows Media Player 控制項
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
keywords:
- Windows Media Player，內嵌 ActiveX 控制項
- Windows Media Player 物件模型，內嵌 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media PlayerMobile、內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項、內嵌
- Windows Media PlayerMobile ActiveX 控制項，內嵌
- ActiveX 控制項，內嵌
- Windows Media Player，c + +
- Windows Media Player 物件模型，c + +
- 物件模型，c + +
- Windows Media PlayerMobile、c + +
- Windows Media Player ActiveX 控制，c + +
- Windows Media PlayerMobile ActiveX control、c + +
- ActiveX 控制項，c + +
- C + + 程式內嵌
- 內嵌，c + + 程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad860219e07a8834a47dc07e4bf8f851866db325c6795151b5076189d546020d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830457"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a>在 c + + 程式中使用 Windows Media Player 控制項

> [!Note]  
> Windows Media Player 9 系列或更新版本支援使用 c + + 內嵌 Windows Media Player 控制項。

 

有幾種不同的方式可以在 c + + 程式中使用 Windows Media Player 控制項。 您可以在主控台應用程式中建立控制項的實例，也可以將控制項內嵌在 Windows 應用程式中。 此外，您可以執行介面，讓您以遠端模式執行內嵌的播放機控制項。 您可以套用面板定義檔來自訂內嵌控制項的使用者介面。

下列主題將說明這項資訊。



| 主題                                                                                                                                      | 描述                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [在主控台應用程式中使用 Windows Media Player 控制項](using-the-windows-media-player-control-in-a-console-application.md)     | 描述可具現化 Windows Media Player 控制項以顯示版本的簡單 c + + 主控台應用程式。                                                       |
| [在 Windows 應用程式中裝載 Windows Media Player 控制項](hosting-the-windows-media-player-control-in-a-windows-application.md) | 描述如何使用 ATL ActiveX 主視窗，在 Windows 程式中內嵌 Windows Media Player 控制項。                                                            |
| [遠端處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)                                                 | 描述如何以遠端模式在 c + + 程式中內嵌 Windows Media Player 控制項，讓您的使用者取消停駐控制項，以切換到播放程式的完整模式。 |
| [在 c + + 中處理事件](handling-events-in-c.md)                                                                                         | 說明如何從 Windows Media Player 接收事件通知。                                                                                                     |
| [搭配 Windows Media Player 控制項使用外觀](using-skins-with-the-windows-media-player-control.md)                                 | 描述如何將面板檔案套用至內嵌于 c + + 程式中的 Windows Media Player 控制項。                                                                             |



 

> [!Note]  
> 您可以將 Windows Media Player 10 個行動控制項內嵌在 Windows CE 應用程式中。 您用來執行此動作的技巧，類似于桌面 Windows Media Player 控制項所使用的技巧。 不過，Windows 的 atl 和 Windows CE 的 atl 之間有一些差異。 本檔說明這些執行的差異（如果適用）。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**C + + 的物件模型參考**](object-model-reference-for-c.md)
</dt> <dt>

[**播放機控制指南**](player-control-guide.md)
</dt> </dl>

 

 




