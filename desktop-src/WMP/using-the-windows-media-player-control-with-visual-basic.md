---
title: 使用 Windows Media Player 控制項搭配 Visual Basic
description: 使用 Windows Media Player 控制項搭配 Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，Visual Basic
- Windows Media Player 物件模型，Visual Basic
- 物件模型，Visual Basic
- Windows Media Player 行動裝置，Visual Basic
- Windows Media Player ActiveX 控制項，Visual Basic
- Windows Media Player 的行動 ActiveX 控制項，Visual Basic
- ActiveX 控制項，Visual Basic
- 以 Visual Basic 為基礎的程式內嵌
- 內嵌、以 Visual Basic 為基礎的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301296"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>使用 Windows Media Player 控制項搭配 Visual Basic

本節說明如何在使用 Microsoft Visual Basic 6.0 所建立的應用程式中，使用 Windows Media Player 9 系列或更新版本的 ActiveX 控制項。

## <a name="getting-started"></a>開始使用

若要將 Windows Media Player 控制項新增至 [工具箱]，請先從 [**專案**] 功能表選取 [**元件**]。 在 [元件] 對話方塊中，選取 [Windows Media Player] 旁的核取方塊。 在對話方塊底部，確認選取的檔案是 wmp.dll。 關閉對話方塊之後，您可以使用一般方式將 Windows Media Player 控制項的實例放在表單上。

您可以使用屬性視窗來設定許多控制項屬性。 若要設定某些屬性，您必須使用 [Windows Media Player 屬性] 對話方塊，您可以使用屬性視窗中的「 (自訂) 」專案來開啟此對話方塊。

## <a name="object-references"></a>物件參考

您可以使用特定的播放機控制項屬性來取得特定物件的參考。 例如， **cdromCollection** 屬性會傳回 **cdromCollection** 物件的參考。 您必須將這類參考指派給宣告為對應介面的變數。 例如，在 **cdromCollection** 屬性的情況下，您會將其傳回值指派給 **IWMPCdromCollection** 類型的變數。

閱讀[c + + 物件模型參考](object-model-reference-for-c.md)中的[介面](interfaces.md)主題，以識別哪些物件會執行多個介面。 在這些情況下，您必須將物件變數宣告為此 SDK 中記載的最高編號介面，才能存取該物件的所有屬性和方法。 例如，您應該將 Windows Media Player control **currentMedia** 屬性的值指派給宣告為 **IWMPMedia3** 的變數，以確保您可以存取 **getAttributeCountByType** 和 **getItemInfoByType** 方法。

> [!Note]  
> **WindowsMediaPlayer** 物件會實 **IWMPCore**、 **IWMPCore2**、 **IWMPCore3**、 **IWMPPlayer**、 **IWMPPlayer2**、 **IWMPPlayer3** 和 **IWMPPlayer4** 介面的所有屬性和方法。 您不需要為這些介面的任何一個宣告個別的變數。 您可以使用指派給 **WindowsMediaPlayer** 實例的名稱來存取其所有成員。

 

在 Visual Basic 的物件瀏覽器中，您會看到許多用於 Windows Media Player 控制項私用的介面，包括支援面板開發人員的部分。 您應該只使用此 SDK 中記載的物件、屬性、方法和事件。

## <a name="additional-tips"></a>其他秘訣

-   參考檔會顯示 JScript 語法。 在 JScript 中，傳遞給方法的引數一律會以括弧括住。 在 Visual Basic 6.0 中，傳遞至未傳回值之方法的引數不能以括弧括住。
-   某些屬性或方法可能不會出現在 [Visual Basic 程式碼編輯器] 的 [自動清單程式碼-自動完成] 功能中。 您仍然可以使用這些成員的名稱，如同在本檔中所顯示的名稱一樣。
-   使用 **uimode** 屬性管理控制項的視覺外觀。 您可以透過兩種方式來這麼做。 您可以使用 [Windows Media Player 屬性] 對話方塊中的 [ **選取模式** ] 下拉式清單，也可以在屬性視窗中輸入正確的值。

    尤其是，請勿使用 **visible** 屬性來隱藏控制項;相反地，請將值「隱藏」指派給 **uimode** 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**播放機控制指南**](player-control-guide.md)
</dt> </dl>

 

 




