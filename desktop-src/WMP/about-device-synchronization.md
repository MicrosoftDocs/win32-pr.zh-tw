---
title: 關於裝置同步處理
description: 關於裝置同步處理
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player，同步處理裝置
- Windows Media Player 物件模型，同步處理裝置
- 物件模型，同步處理裝置
- Windows Media Player ActiveX 控制項，同步處理裝置
- ActiveX 控制項，同步處理裝置
- Windows Media Player 的行動 ActiveX 控制項，同步處理裝置
- Windows Media Player 行動裝置，同步處理裝置
- 正在同步處理裝置，關於
- 裝置同步處理，關於
- 同步處理裝置，手動轉移
- 裝置同步處理，手動傳輸
- 同步處理裝置，自動同步處理
- 裝置同步處理，自動同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967197"
---
# <a name="about-device-synchronization"></a>關於裝置同步處理

Windows Media Player 10 引進了新的模型，可將數位媒體內容與可攜式裝置進行同步處理。 從使用者的觀點來看，這表示您可以指定哪些播放清單 (包括自動播放清單) 自動與裝置同步處理。 您也可以手動將數位媒體內容傳送至裝置。 從開發人員的觀點來看，這表示您可以在應用程式中充分利用新功能。 若要這樣做，您必須建立 Windows Media Player 控制項的遠端實例。

使用者可以透過兩種方式將數位媒體內容複寫到裝置：

-   **手動轉移。** 使用者會在媒體櫃中選取數位媒體內容，然後開始將內容傳送到裝置。 這與舊版 Windows Media Player 所提供的功能類似。 Windows Media Player SDK 不提供將數位媒體傳送至裝置的方法。
-   **自動同步處理。** 使用者指定自動與裝置同步處理的播放清單。 這是 Windows Media Player 10 或更新版本的功能。 Windows Media Player SDK 提供管理自動同步處理的功能。 這項功能的設計目的是讓您為應用程式建立自訂使用者介面，以指定裝置同步處理的執行方式，以及提供狀態資訊給使用者。

若要讓自動同步處理正常運作，必須在 Windows Media Player 和裝置之間建立特殊的關聯性。 此關聯性稱為 *合作* 關係。

下列各節提供有關裝置同步處理的詳細資訊。

-   [關於裝置](about-devices.md)
-   [關於合作關係](about-partnerships.md)
-   [關於同步處理引擎](about-the-synchronization-engine.md)
-   [關於播放清單同步處理](about-playlist-synchronization.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**使用可攜式裝置**](working-with-portable-devices.md)
</dt> </dl>

 

 




