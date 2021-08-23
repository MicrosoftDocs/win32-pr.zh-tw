---
title: 指令碼語言的播放程式物件模型
description: 指令碼語言的播放程式物件模型
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，關於
- 物件模型，關於
- Windows Media Player ActiveX 控制項，物件模型
- ActiveX 控制項，物件模型
- Windows Media PlayerMobile ActiveX 控制項，物件模型
- Windows Media Player行動裝置，物件模型
- 軟體發展工具組 (SDK) ，Windows Media Player ActiveX 控制項物件模型
- SDK (軟體發展工具組) ，Windows Media Player ActiveX 控制項物件模型
- 檔、Windows Media Player ActiveX 控制項物件模型
- Windows Media Player，指令碼語言
- Windows Media Player 物件模型，指令碼語言
- 物件模型，指令碼語言
- Windows Media Player ActiveX 控制項、指令碼語言
- ActiveX 控制項，指令碼語言
- Windows Media PlayerMobile ActiveX control、指令碼語言
- Windows Media Player行動、指令碼語言
- 指令碼語言
- Windows Media Player，Player 物件
- Windows Media Player 物件模型、Player 物件
- 物件模型、Player 物件
- Windows Media Player ActiveX control、Player 物件
- ActiveX control、Player 物件
- Windows Media PlayerMobile ActiveX control、Player 物件
- Windows Media PlayerMobile、Player 物件
- Player 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe34bfc227dfe250a9c9d7ebb60977a9ab079c4a062067c65e83e62f0e5976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996021"
---
# <a name="player-object-model-for-scripting-languages"></a>指令碼語言的播放程式物件模型

ActiveX 使用物件的概念來包含程式設計功能。 Windows Media Player 會使用數個物件來分割控制項所提供的功能。 根物件是 **player** 物件，而其他物件則是透過特定屬性附加至 **player** 物件。

下圖顯示 Windows Media Player 11 ActiveX 控制項物件模型如何針對指令碼語言運作。

![windows media player 11 物件模型的圖表](images/playeromdiag.png)

在 c + + 中，有時也是在 .NET 語言中，物件是由 COM 介面表示。 在 Windows Media Player 物件模型中，COM 介面名稱與物件名稱相同，但前面會加上 "IWMP"。 例如，透過 **IWMPNetwork** 介面公開 **網路** 物件。

下列各節提供每個物件的概念總覽：

-   [關於 Cdrom 和 CdromCollection 物件](about-the-cdrom-and-cdromcollection-objects.md)
-   [關於 ClosedCaption 物件](about-the-closedcaption-object.md)
-   [關於控制項物件](about-the-controls-object.md)
-   [關於 DVD 物件](about-the-dvd-object.md)
-   [關於 Error 和 ErrorItem 物件](about-the-error-and-erroritem-objects.md)
-   [關於 MediaCollection 和 Media 物件](about-the-mediacollection-and-media-objects.md)
-   [關於 MetadataPicture 物件](about-the-metadatapicture-object.md)
-   [關於 MetadataText 物件](about-the-metadatatext-object.md)
-   [關於 Network 物件](about-the-network-object.md)
-   [關於 Player 物件](about-the-player-object.md)
-   [關於 PlayerApplication 物件](about-the-playerapplication-object.md)
-   [關於播放清單、PlaylistCollection 和 PlaylistArray 物件](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [關於 Query 物件](about-the-query-object.md)
-   [關於設定物件](about-the-settings-object.md)
-   [關於 StringCollection 物件](about-the-stringcollection-object.md)

您可以透過特定的 COM 介面取得額外的功能。 您是否可以存取這些介面，可能取決於您用於程式設計的語言和其他因素，例如用來建立 Windows Media Player 控制項實例的模式。 如需 Windows Media Player 控制項公開的 COM 介面完整清單，請參閱[c + + 的物件模型參考](object-model-reference-for-c.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> <dt>

[**在 .NET Framework 方案中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




