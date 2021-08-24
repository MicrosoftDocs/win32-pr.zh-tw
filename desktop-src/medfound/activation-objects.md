---
description: 啟用物件
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: 啟用物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401b4643e7e19c8cf0b7235218eaed2e355565fdb82a9d3756558e1f11991cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035596"
---
# <a name="activation-objects"></a>啟用物件

*啟用物件* 是用來建立另一個物件的 helper 物件，與 class factory 有點類似。 啟用物件會公開 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面。

啟始物件可讓您延遲建立目標物件，因為您可以在不建立目標物件的情況下，保留在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標上。 啟用物件也可以序列化，因此用來在另一個進程中建立目標物件。 例如，啟用物件是用來將管線元件從應用程式程式封送處理到受保護的媒體路徑， (PMP) 進程。 傳回 **IMFActivate** 指標清單的特定列舉函數也會使用啟用物件。 在應用程式建立目標物件之前，它可以檢查啟用物件上的屬性，以取得物件的相關資訊。

若要從啟用物件建立目標物件，請呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法。 使用已建立的物件完成時，呼叫端必須呼叫 [**IMFActivate：： ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) 。 應用程式通常會建立啟用物件，而媒體會話會呼叫 **ActivateObject**。 在此情況下，媒體會話（而不是應用程式）必須呼叫 **ShutdownObject**。 在其他情況下，應用程式會接收來自媒體會話的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標，而應用程式會呼叫 **ActivateObject** 和 **ShutdownObject**。  (例如，請參閱 [如何播放受保護的媒體](how-to-play-protected-media-files.md)檔案。 ) 

啟用物件可以有屬性，而 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 某些啟用物件會使用屬性來設定建立的物件。 每個物件所支援的特定屬性都記載于該啟用物件建立函式的參考中。 使用您從函數接收的 **IMFActivate** 指標來設定屬性。

針對受保護的播放，啟始物件會封送處理至 PMP 程式。 若要支援封送處理，啟用物件必須公開 **IPersistStream** 介面。 此外，如果 PMP 是在受保護的進程中執行，則啟用物件和建立的物件都必須是信任的元件。 在未受保護的進程中載入 PMP 時，不需要這麼做。

若要在 PMP 程式中使用自訂管線物件 (例如媒體接收器) ，您必須為管線物件執行啟用物件：

-   啟用物件必須公開 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 和 **IPersistStream**。
-   啟用物件的 **IPersist：： GetClassID** 方法必須傳回啟用物件的 CLSID。
-   （選擇性）您可以執行 **IPersistStream：： Save** 和 **IPersistStream：： Load** 方法來封送處理您設定啟用物件所需的任何資料。

當媒體會話在 PMP 程式中載入拓撲時，它會呼叫 **CoCreateInstance** 來建立新的啟用物件實例。 然後，它會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立管線物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



