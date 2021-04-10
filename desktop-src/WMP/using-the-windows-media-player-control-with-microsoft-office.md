---
title: 使用 Windows Media Player 控制項搭配 Microsoft Office
description: 使用 Windows Media Player 控制項搭配 Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player、Office
- Windows Media Player 物件模型，Office
- 物件模型、Office
- Windows Media Player Mobile、Office
- Windows Media Player ActiveX 控制項、Office
- Windows Media Player 的行動 ActiveX 控制項、Office
- ActiveX 控制項，Office
- Office 檔內嵌
- 內嵌、Office 檔
- Windows Media Player ActiveX 控制項，Excel
- Windows Media Player 的行動 ActiveX 控制項、Excel
- ActiveX 控制項，Excel
- 內嵌，Excel 試算表
- Excel 試算表嵌入
- Windows Media Player ActiveX 控制項，PowerPoint
- Windows Media Player Mobile ActiveX 控制項，PowerPoint
- ActiveX 控制項，PowerPoint
- 內嵌，PowerPoint 投影片放映
- PowerPoint 投影片放映內嵌
- Windows Media Player ActiveX 控制項，Word
- Windows Media Player 的行動 ActiveX 控制項，Word
- ActiveX 控制項，Word
- Word 檔內嵌
- 內嵌、Word 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932274"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>使用 Windows Media Player 控制項搭配 Microsoft Office

本節說明如何在使用 Microsoft Office XP 建立的各種檔中內嵌 Windows Media Player 9 系列或更新版本的 ActiveX 控制項。

在 Microsoft Word、Excel 和 PowerPoint®中，您可以從 [**插入**] 功能表選取 [**物件**]，然後從可用的物件類型清單中選擇 [ **Windows Media Player** ] 來內嵌控制項。 Windows Media Player 控制項會出現在檔中的目前位置。 然後，您可以從控制項的快捷方式功能表，選取 [Excel) 中的 **格式控制項** ( **格式物件** ]，以調整配置、文字換行樣式和其他格式選項。 在 Word 和 Excel 中，您必須處於設計模式才能完成這項作業。

一旦將控制項定位並格式化之後，您就可以使用 [ **屬性** ] 對話方塊進行設定，這個對話方塊可從 [ **控制項工具箱** ] 或 Word 和 Excel 的設計模式中的快捷方式功能表進行存取。 您可以在這裡指定基本的播放程式控制項屬性，例如控制項名稱、數位媒體檔案的 URL，以及使用者介面模式。 將 [ **uiMode** ] 屬性設定為 [無] 會隱藏控制項中的所有專案，除了 [影片] 或 [視覺效果] 視窗之外，還可讓您使用 VISUAL BASIC FOR APPLICATIONS (VBA) 來處理按鈕點擊和播放機控制項事件，以新增您自己的按鈕及撰寫腳本程式碼。

在 [基本 **屬性** ] 對話方塊中，您也可以在選取該資料列之後，按兩下 [ (自訂) ] 資料列或按一下省略號 ( [...] ) 按鈕，以存取更精密的 **Windows Media Player 控制項屬性** 對話方塊。 您可以從這個對話方塊修改所有可用的播放程式控制控制項屬性。

> [!Note]  
> 您必須小心不要在播放程式控制項的事件處理常式中採取動作，這會導致控制項遭到終結。 例如，如果您將 Windows Media Player 控制項內嵌在 PowerPoint 簡報中的投影片上，請不要從 Player **openStateChange** 事件或任何其他事件呼叫 PowerPoint **Next** 方法。

 

> [!Note]  
> 此外，您不應該從 Player 控制項事件處理常式設定 **player. URL** 屬性。

 

在 FrontPage 中，從 [**插入**] 功能表選取 [ **Web 元件**]，將 Windows Media Player 控制項新增至網頁。 在 [**插入 Web 元件**] 對話方塊中，從 [**元件類型**] 清單中選取 [ **Advanced Controls** ]，然後從控制項選項清單中選取 [ **ActiveX 控制項**]。 在對話方塊的下一個視窗中，選取 [ **Windows Media Player**]。 如果未列出，請按一下 [**自訂**]，然後選取 **控制項** 清單中的 [ **Windows Media Player** ] 核取方塊。

內嵌 Windows Media Player 控制項之後，您可以將其定位和調整大小，並從控制項的快捷方式功能表中選取 [ **ActiveX 控制項屬性** ] 來修改其屬性。 在 HTML 視圖中，您指定的屬性值會出現在代表 Windows Media Player 控制項的 OBJECT 元素中。 物件名稱會顯示為 ID 屬性，而控制項屬性會顯示為 PARAM 標記。 物件名稱可讓您存取 Windows Media Player 控制項物件模型，您可以使用 Microsoft JScript 進行程式設計。 如需詳細資訊，請參閱 [使用網頁中的 Windows Media Player 控制項](using-the-windows-media-player-control-in-a-web-page.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**播放機控制指南**](player-control-guide.md)
</dt> </dl>

 

 




