---
title: 關於 Player 物件模型
description: 關於 Player 物件模型
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，關於
- 物件模型，關於
- Windows Media Player ActiveX 控制項，物件模型
- ActiveX 控制項，物件模型
- Windows Media Player Mobile ActiveX 控制項，物件模型
- Windows Media Player 行動裝置，物件模型
- 軟體發展工具組 (SDK) ，Windows Media Player ActiveX 控制項物件模型
- SDK (軟體發展工具組) ，Windows Media Player ActiveX 控制項物件模型
- 檔，Windows Media Player ActiveX 控制項物件模型
- Player 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968427"
---
# <a name="about-the-player-object-model"></a>關於 Player 物件模型

Microsoft Windows Media Player 控制項是一種標準的 ActiveX 控制項，使用 Microsoft 元件物件模型 (COM) 技術。 Windows Media Player 的功能會在一組遵循標準 COM 指導方針的程式設計介面中。 您可以使用 Player 控制項物件模型搭配 Microsoft JScript 或 Microsoft Visual Basic Scripting Edition (VBScript) ，在標準的 HTML 網頁上撰寫這些介面的程式。 您也可以使用 Microsoft JScript 在面板中進行程式設計。 如果您想要建立內嵌控制項的自訂程式，您可以使用數種語言的其中一種，包括 Visual Basic、c + + 和 c #。

Windows Media Player 的 ActiveX 控制項與 Windows Media Player 一起安裝。 播放機控制項不會隨 Windows Media Player SDK 一起安裝，也不能另外再散發。 您的程式碼可用的特定功能，取決於使用者所安裝的 Windows Media Player 版本。 [C + + 的腳本和物件模型參考](object-model-reference-for-c.md)的[物件模型參考](object-model-reference-for-scripting.md)包含每個屬性、方法和事件的版本需求資訊。

下列各節提供有關 Windows Media Player 物件模型的總覽資訊。



| 區段                                                                                        | 描述                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [指令碼語言的播放程式物件模型](player-object-model-for-scripting-languages.md) | 本節說明物件模型中可用的物件。                                                                                             |
| [關於物件模型版本](about-the-object-model-versions.md)                         | 本節詳細說明自 Windows Media Player 7.0 推出之後，每個版本中已加入的物件模型專案。                             |
| [屬性、方法和事件](properties--methods-and-events.md)                          | 本節說明屬性、方法和事件。                                                                                                        |
| [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)                   | 本節列出 Windows Media Player 和 Windows Media Player control 物件模型所支援的通訊協定和檔案類型。                          |
| [關於程式庫](about-the-library.md)                                                     | 本節說明 Windows Media Player 程式庫。                                                                                                      |
| [使用 HTML 搭配 Windows Media Player](using-html-with-windows-media-player.md)               | 本節說明讓 Windows Media Player 和 HTML 一起運作的各種方式。                                                                  |
| [內嵌 Windows Media Player 控制項](embedding-the-windows-media-player-control.md)   | 本節說明在 Microsoft Office 檔和自訂程式中內嵌 Windows Media Player 控制項的各種方式。                       |
| [關於裝置同步處理](about-device-synchronization.md)                               | 本節說明將數位媒體內容傳輸至可攜式裝置的 Windows Media Player 10 或更新版本控制項所提供的功能。 |
| [關於 CD 燒錄](about-cd-burning.md)                                                       | 本節說明用來建立 Cd 的 Windows Media Player 控制項所提供的功能。                                                       |
| [關於 CD 翻錄](about-cd-ripping.md)                                                       | 本節說明 Windows Media Player 控制項所提供的功能，可將曲目從音訊 Cd 複製到使用者的電腦。               |
| [關於資料夾監控](about-folder-monitoring.md)                                         | 本節說明用來控制播放程式資料夾監控進程的 Windows Media Player 控制項所提供的功能。               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player 物件模型**](windows-media-player-object-model.md)
</dt> </dl>

 

 




