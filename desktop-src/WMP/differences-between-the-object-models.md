---
title: 物件模型之間的差異
description: 物件模型之間的差異
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，版本差異
- 物件模型，版本差異
- Windows Media Player ActiveX 控制，版本差異
- ActiveX 控制項，版本差異
- Windows Media PlayerMobile ActiveX 控制項，版本差異
- Windows Media Player行動裝置，物件模型
- 遷移指南，版本差異
- Windows Media Player 的版本，物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dd3b7862e2d9c5580950ad2eb718bd1c8125a5d22ec6a08533c140de545086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749739"
---
# <a name="differences-between-the-object-models"></a>物件模型之間的差異

Windows Media Player 6.4 物件模型和 Windows Media Player 7 或更新版本的物件模型之間有兩個主要差異。

-   **CLSID** Windows Media Player 7 或更新版本的物件模型完全離開6.4 版物件模型。 元件物件模型 (COM) 規格需要所有現有的介面都必須在新版本的 COM 元件中繼續運作。 這表示新介面可以新增至 COM 元件，但永遠不會改變現有的介面，以確保較舊的用戶端程式代碼一律會使用其設計所使用的特定元件。 因此，Windows Media Player 7 或更新版本的 ActiveX 控制項有新的類別識別碼：6BF52A52-394A-11D3-B153-00C04F79FAA6。 如果您想要利用此版本之控制項的新功能，則必須變更您的 CLSID。
-   **階層式物件模型** 如果您已經使用 Windows Media Player 6.4 ActiveX 控制項，可能已經注意到所有屬性、方法和事件都是透過相同的物件來存取： **Player** 物件。 相反地，Windows Media Player 7 或更新版本的物件模型會組織為物件的階層。 **Player** 物件仍然是根物件，但函式現在可透過各種子物件來存取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件模型遷移指南**](object-model-migration-guide.md)
</dt> </dl>

 

 




