---
description: 多媒體串流的優點
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: 多媒體串流的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06df23ce833462aee9b7d4b3840c1fae2d4f3b15c4ee6daee2e4a421259493a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537538"
---
# <a name="advantages-of-multimedia-streaming"></a>多媒體串流的優點

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md)篩選器或執行自訂篩選，以從 DirectShow 的篩選圖形取得資料。

 

當開發人員在其應用程式中使用多媒體串流時，可以大幅減少所需的格式特定程式設計。 一般而言，必須從檔案或硬體來源取得媒體資料的應用程式，必須知道資料格式和硬體裝置的所有相關資訊。 應用程式必須處理連接、資料傳輸、任何必要的資料轉換，以及實際的資料轉譯或檔案儲存體。 因為每種格式和裝置都稍微不同，所以此程式通常很複雜而且很麻煩。 另一方面，多媒體串流會自動協調將資料從來源傳送和轉換至應用程式的工作。 串流介面提供一致且可預測的資料存取和控制方法，可讓應用程式輕鬆地播放資料（不論其原始來源或格式為何）。

下列步驟說明如何執行串流，從硬體裝置到轉譯的播放。

1.  影片資料的來源（例如 DirectShow）會公開串流介面。
2.  應用程式開發人員會使用多媒體串流介面來處理資料格式轉換。
3.  應用程式開發人員會使用 DirectDraw 介面來轉譯產生的資料。

多媒體串流的規格包含數個介面;每個介面都包含可控制串流處理常式特定層面或處理特定資料類型的方法。 如需其他資訊，請參閱 [多媒體串流介面的清單](list-of-multimedia-streaming-interfaces.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於多媒體串流架構](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



