---
title: 搭配 Windows Media Player 控制項使用外觀
description: 搭配 Windows Media Player 控制項使用外觀
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，c + +
- Windows Media Player 物件模型，c + +
- 物件模型，c + +
- Windows Media Player Mobile，c + +
- Windows Media Player 的 ActiveX 控制項，c + +
- Windows Media Player 的行動 ActiveX 控制項，c + +
- ActiveX 控制項，c + +
- C + + 程式內嵌
- 內嵌，c + + 程式
- Windows Media Player ActiveX 控制項，外觀
- Windows Media Player 的行動 ActiveX 控制項、外觀
- ActiveX 控制項，外觀
- 外觀，內嵌 ActiveX 控制項
- Windows Media Player 的外觀，內嵌 ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183542"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>搭配 Windows Media Player 控制項使用外觀

當您在 c + + 程式中內嵌 Windows Media Player 控制項時，您可以透過將面板定義檔套用至該應用程式， (UI) 自訂播放機使用者介面。 面板定義檔是以 XML 為基礎的檔，指定標準和可自訂 UI 元件的配置和任何隨附的圖形。 您可以使用 Microsoft JScript 來指定這些元件的行為，並操作 Windows Media Player 控制項，而不會產生 c + + 和 COM 語法的額外負荷。

面板提供簡單的方法，讓您的使用者介面程式碼和主要程式碼分開，讓它們可以獨立維護和開發。 您也可以重複使用原本設計的面板，以便在面板模式中供獨立播放程式使用。 您專為 c + + 程式設計的面板程式碼可透過程式可提供的可編寫腳本的物件與程式互動。

若要啟用 Windows Media Player 控制項的面板模式，您的程式必須執行 **IWMPRemoteMediaServices** 介面。 雖然您可以同時使用具有控制項和遠端控制項的面板，但您可以使用這個介面來啟用任一個功能，而不需要啟用另一個功能。 若要停用遠端處理，只要傳遞 "Local" 的值做為 **GetServiceType** 方法的 out 參數，並 \_ 從 **GetApplicationName** 方法傳回 E >notimpl 的 HRESULT。

若要將 Windows Media Player 控制項切換至面板模式，請呼叫 **IWMPPlayer：:p 的 \_ uiMode** 方法，並傳入 "custom" 的值。 從 **IWMPRemoteMediaServices：： GetCustomUIMode** 方法傳回，以指定要使用之面板定義檔的路徑和檔案名。

如果您想要為您的面板和程式之間的通訊提供可編寫腳本的物件，請將名稱和指標傳遞至 **IDispatch** 指標，作為 **IWMPRemoteMediaServices：： GetScriptableObject** 方法的兩個 out 參數。 然後，您的面板就可以使用指定的名稱來呼叫可編寫腳本的物件，就像是類似于 **player** global 屬性的全域屬性一樣。

套用至遠端 Windows Media Player 控制項的面板，可以使用名為 **PlayerApplication** 的另一個全域屬性來存取 **PlayerApplication** 物件。 由於 **playerApplication** 屬性無法由外觀存取，因此當您想要讓面板程式碼管理停駐和移除時，您必須使用這個全域屬性。

## <a name="samples"></a>範例

Windows Media Player SDK 安裝程式套件會安裝示範將面板套用至 Windows Media Player 控制項的範例。 如需詳細資訊，請參閱 RemoteSkin 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**範例**](samples.md)
</dt> <dt>

[**在 c + + 程式中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




