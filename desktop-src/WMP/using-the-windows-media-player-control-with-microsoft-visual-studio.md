---
title: 使用 Windows Media Player 控制項搭配 Microsoft Visual Studio
description: 使用 Windows Media Player 控制項搭配 Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，.NET Framework
- Windows Media Player 物件模型，.NET Framework
- 物件模型、.NET Framework
- Windows Media Player Mobile、.NET Framework
- Windows Media Player ActiveX 控制項，.NET Framework
- Windows Media Player 的行動 ActiveX 控制項，.NET Framework
- ActiveX 控制項，.NET Framework
- Windows Media Player ActiveX 控制項，Visual Studio
- Windows Media Player 的行動 ActiveX 控制項，Visual Studio
- ActiveX 控制項，Visual Studio
- .NET Framework，Visual Studio 程式嵌入
- 內嵌、Visual Studio 程式
- Visual Studio，程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "104022151"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>使用 Windows Media Player 控制項搭配 Microsoft Visual Studio

您可以透過 Visual Studio 中的 [工具箱]，將 Windows Media Player 9 系列或更新版本的 ActiveX 控制項新增至 .NET Framework 應用程式。

## <a name="adding-the-windows-media-player-control"></a>加入 Windows Media Player 控制項

建立新專案之前，請確定您的電腦上已安裝最新版本的 Windows Media Player 和 Windows Media Player SDK。

開始 Visual Studio，然後建立新專案。

在 Visual Studio 中，開啟 [工具箱]。

如果 Windows Media Player 未出現在 [工具箱] 的 [ **元件** ] 部分中，請執行下列動作：

1.  在 [工具箱] 中按一下滑鼠右鍵，然後選取 **[選擇專案**]。 這會開啟 [ **自訂工具箱** ] 對話方塊。
2.  在 [ **COM 元件** ] 索引標籤上，選取 [Windows Media Player]。

    如果 Windows Media Player 未出現在清單中，請按一下 **[流覽]**，然後開啟 [Wmp.dll]，這應該會出現在 Windows [ \\ System32] 資料夾中。

3.  按一下 [確定]  。 Windows Media Player 控制項將放置在目前的 [工具箱] 索引標籤上。

您現在可以在 [工具箱] 中選取 Windows Media Player，並將其新增至表單。

Visual Studio 提供 Windows Media Player 的控制項預設名稱，例如 "axWindowsMediaPlayer1"。 您可能會想要將名稱變更為更容易記住的名稱，例如「Player」。

從 [工具箱] 新增 Windows Media Player 控制項也會新增 Visual Studio、AxWMPLib 和 WMPLib 所建立之兩個程式庫的參考。 您可以在 [ **參考**] 下的方案總管中找到它們。

若要更輕鬆地使用 Player 命名空間中的物件，您應該在檔案的 using 或 imports 指示詞中包含命名空間，如下所示：


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



指示詞可確保您可以參考 **Player** 物件，而不需要完整限定其名稱。

> [!Note]  
> Windows Media Player 控制項是來自 **AxWMPLib** 命名空間的 **AxWindowsMediaPlayer** 物件。 不過， **AxWindowsMediaPlayer** 類別會使用 **WMPLib** 命名空間中的資料類型、介面和其他元素。

 

## <a name="configuring-visibility-of-the-control"></a>設定控制項的可見度

當您第一次將 Windows Media Player 控制項新增至表單時，就會顯示該控制項。 如果您不想要在應用程式中使用播放程式的可見影像，請設定下列其中一個屬性來隱藏預設播放程式：



| 屬性        | 值                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | 「隱藏」 (查看 [uiMode](player-uimode.md)。 )  |
| **Visible**     | "false"                                               |
| **大小：寬度**  | 0                                                     |
| **大小：高度** | 0                                                     |



 

當表單設計工具中選取了 Windows Media Player 控制項時，您可以在程式碼或 [ **屬性** ] 視窗中設定這些屬性。

## <a name="object-model-compatibility-of-the-control"></a>控制項的物件模型相容性

在與非受控碼和腳本相同的 .NET Framework 中，Windows Media Player 控制項的物件模型基本上是相同的。 不過，專案的公開方式有一些差異：

-   大部分的物件都會在其基礎 COM 介面的名稱底下公開。 例如， **播放清單** 物件會公開為 **IWMPPlaylist**。
-   某些介面有較新的版本。 例如， **IWMPMedia** 在 **IWMPMedia2** 和 **IWMPMedia3** 中獲得額外的功能。 如果您將物件宣告為 **IWMPMedia**，通常就可以存取所有介面版本的功能。 不過，IntelliSense®將無法辨識較新版介面的方法或屬性，而 Visual Basic .NET 編輯器將不會自動校正大小寫。 若要取得 Visual Studio 的 IntelliSense 和其他功能的完整優點，請使用最新版本的介面（例如 **IWMPMedia3**）來宣告物件。
-   沒有任何索引屬性 (c # ) 或 Visual Basic .NET)  (的預設屬性。 例如，若要取出 **播放清單專案**，您必須在 c # 中呼叫 **IWMPlaylist \_** ，或在 Visual Basic .Net 中取出 **IWMPlayist. item** 屬性。
-   由於 Windows Media Player **Controls** 屬性和每個控制項公開的 **控制項** 屬性之間有命名衝突，所以此屬性的播放程式版本在 ActiveX 控制項的內容中稱為 **CtlControls** 。  (不過，當您以程式設計的方式建立播放機而非 ActiveX 控制項時，就不會發生這種情況。 ) 

使用 Visual Studio 中的物件瀏覽器，在 **AxWMPLib** 和 **WMPLib** 命名空間中找出方法和物件的正確 API 名稱。

## <a name="distributing-your-application"></a>散發您的應用程式

當您散發應用程式時，請務必在應用程式資料夾中安裝 AxInterop.WMPLib.dll 和 Interop.WMPLib.dll。 您也必須確定使用者的電腦上已安裝必要的 Windows Media Player 版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**以程式設計方式建立 Windows Media Player 控制項**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**在 c # 方案中內嵌 Windows Media Player 控制項**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**在 Visual Basic .NET 方案中內嵌 Windows Media Player 控制項**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




