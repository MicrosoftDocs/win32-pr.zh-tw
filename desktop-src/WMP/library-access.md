---
title: 程式庫存取
description: 程式庫存取
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 程式庫，存取
- 程式庫，存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300816"
---
# <a name="library-access"></a>程式庫存取

存取程式庫 Windows Media Player 物件模型的屬性和方法，需要資料庫的唯讀或讀取/寫入存取權。 此程式庫包含某些使用者想要保持私密的資訊，而且應該只透過其同意來存取或更改。

針對 Windows Media Player 9 系列或更新版本，您可以透過程式設計的方式決定存取層級。 若要判斷授與您程式碼的目前存取層級，請取出 *設定*。**mediaAccessRights** 屬性。 該屬性會傳回「無」、「讀取」或「完整」 (讀取/寫入) 。 若要要求特定的存取權限，請呼叫 *設定*。**requestMediaAccessRights** 方法，傳遞指定您所要求層級的參數。 方法會顯示訊息給使用者，說明所要求的存取層級，並傳回 **布林** 值，指出是否已授與存取權。

系統會根據您的程式碼相對於使用者電腦的執行位置，自動授與特定存取權限。

-   如果您的網頁或程式位於使用者的電腦上，則預設會授與完整存取權限。
-   Web pages 具有 *播放玩家* 的讀取權限。**currentMedia**、 *Player*。**currentPlaylist**，以及 *媒體*。當網頁位於與媒體專案或播放清單的安全性區域相同或更受限制的 Internet Explorer 安全性區域中時， **sourceURL** 。

    從最低限制到最受限制的範圍，安全性區域是 **受信任** 的區域 (包括使用者的本機電腦) 、近端 **內部** 網路區域、 **網際網路** 區域和 **受限** 的區域。

    例如，近端 **內部** 網路區域中的網頁具有 *播放* 程式的完整存取權限。**currentMedia** 對應的媒體專案位於近端內部網路或網際網路時，但必須針對位於使用者本機電腦或 **受信任** 區域中網站上的媒體專案要求存取權。

您應該在其可能遇到的所有安全性區域中測試您的 Web 型或 Windows 應用程式。 應用程式應設計為可適當地處理拒絕存取要求。

Windows Media Player 9 系列之前 Windows Media Player 物件模型版本不包含 **mediaAccessRights** 或 **requestMediaAccessRights**。 這些舊版的 Windows Media Player 可讓使用者使用 [ **選項** ] 對話方塊來設定存取層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> <dt>

[**使用程式庫**](working-with-the-library.md)
</dt> </dl>

 

 




