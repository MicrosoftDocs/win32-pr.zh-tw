---
title: 在自訂程式中嵌入 Windows Media Player 控制項
description: 在自訂程式中嵌入 Windows Media Player 控制項
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- 內嵌，自訂程式
- 自訂程式內嵌
- 內嵌、以 Visual Basic 為基礎的程式
- 以 Visual Basic 為基礎的程式內嵌
- 內嵌、手動使用 COM 方法
- 使用 COM 方法進行手動內嵌
- 內嵌，c + + 程式
- C + + 程式內嵌
- 內嵌、Visual Studio 程式
- Visual Studio，程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021224"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>在自訂程式中嵌入 Windows Media Player 控制項

由於 Windows Media Player ActiveX 控制項是以 Microsoft 元件物件模型 (COM) 技術為基礎，因此您可以將它內嵌在以許多不同的程式設計語言撰寫的程式中。 Windows Media Player 控制項代表將複雜數位媒體功能新增至任何程式的簡單方法。

在 Microsoft Visual Basic 中，您可以將控制項加入至控制項工具箱、將控制項放在表單上，然後調整 [屬性] 視窗中的控制項屬性。 如果您想要自訂使用者介面，您可以將命令按鈕放在表單上，並加入管理 Windows Media Player 控制項的程式碼。 在以 Visual Basic 為基礎的程式中內嵌控制項，與在 Office 檔中內嵌控制項並使用 VBA 進行程式設計的方式非常類似。

或者，您可以使用 COM 方法，以手動方式內嵌控制項，將控制項具現化，並存取 [c + + 的物件模型參考](object-model-reference-for-c.md)中記載的 COM 介面。

當您在 c + + 程式中內嵌 Windows Media Player 控制項時，您可以選擇執行允許控制項在遠端模式中執行的 COM 介面。 這表示嵌入的控制項會與播放程式的完整模式共用相同的播放引擎，而使用者可以在完整模式和停駐的狀態之間來回切換，而不會中斷數位媒體播放。 您也可以控制當使用者切換至未移除狀態時，完整模式播放程式的各種窗格中所顯示的內容。

使用 c + + 內嵌，您也可以選擇將面板定義檔套用到內嵌的播放機控制項。 這是建立輕量使用者介面程式碼的簡單方法，您可以將它與您的主要程式碼分開維護。

Microsoft Visual Studio 支援嵌入 ActiveX 控制項，包括 Windows Media Player 控制項。 當您選擇這麼做時，Visual Studio 會建立新的替代互通性 (interop) 元件，以管理 .NET Framework 與 Windows Media Player 控制項之間的互通性。 Visual Studio 使用 .NET Framework tlbimp.exe 工具來建立 interop 元件。 這表示使用 Visual Studio 中的 IntelliSense 功能時所顯示的簽章，會使用目前版本的 tlbimp 所決定的語法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**內嵌 Windows Media Player 控制項**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**在 c + + 程式中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**在 .NET Framework 方案中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**使用 Windows Media Player 控制項搭配 Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




