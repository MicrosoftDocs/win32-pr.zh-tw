---
description: COM + 執行緒模型是設計在名為一個單元的物件集合周圍。 一個單元是包含在進程中的內容集合。
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: COM + 執行緒模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0949a27291be43b5981f24f4985fac6911937b2c9fa85785b4d662bd1bf546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793671"
---
# <a name="com-threading-models"></a>COM + 執行緒模型

COM + 執行緒模型是設計在名為一個單元的物件集合周圍。 一個單元是包含在進程中的內容集合，如下圖所示。

![此圖表顯示進程內活動中的內容集合。](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

在一個單元內的呼叫是直接的，而跨 (跨進程的) 則是間接的，且需要 proxy 和存根程式碼。 單元允許具有不同同步處理和重新進入屬性的物件，且有兩個類別：單一執行緒和多執行緒。 單一執行緒單元中的物件 (STA) 在其建立所在的特定執行緒上執行。 Sta 一次只允許一個方法執行。 它們是專為使用者介面所設計，並依賴 Microsoft Windows 訊息佇列來處理傳入的呼叫。

多執行緒單元中的物件 (MTA) 在任何執行緒上執行，並允許任何數目的方法同時發生。 Mta 支援隱含 reentrance。

COM + 類別會以 **>threadingmodel** 屬性標記，可讓 com + 在適當的單元中建立物件。 為了判斷要在其中建立物件的單元， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 會使用 **>threadingmodel** 屬性。

執行緒必須先呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ，才能使用 com +。 這會在正確的單元和內容中建立它們。 主要執行緒的單元會被判斷為 **CoInitializeEx** 所呼叫的第一個 STA。 這通常與進程的主執行緒相關聯。 **CoInitializeEx** 藉由設定下列旗標，指出執行緒所需的單元類型：

-   **COINIT \_多執行緒**-在單一多執行緒單元中尋找執行緒。
-   **COINIT \_APARTMENTTHREADED**：將執行緒放入新的 STA 中。

本節中的下列主題提供有關在 COM + 中使用執行緒模型和單元的詳細資訊：

-   [執行緒模型屬性](threading-model-attribute.md)
-   [中性單元](neutral-apartments.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[進程、執行緒和單元](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**>threadingmodel**](components.md)
</dt> </dl>

 

 
