---
description: 具現化編碼器 MFT
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: 具現化編碼器 MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40337bbef63cf243777978d1672a60de5ebfba8874b3cce0271ca06ccf4ab38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974267"
---
# <a name="instantiating-an-encoder-mft"></a>具現化編碼器 MFT

在 Microsoft 媒體基礎中，編碼器會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 。 建立編碼器之前，您必須先找出最適合您需求的編碼器。

-   Windows媒體音訊編解碼器

    類別： **MFT \_ 類別 \_ 音訊 \_ 編碼器**

    主要類型： MFMediaType \_ 音訊

    子類型： MFAudioFormat \_ WMAudioV9、MFAudioFormat \_ WMAudioV8、MFAudioFormat \_ WMAudio \_ 無損、MFAudioFormat \_ WMASPDIF

-   Windows媒體視頻編碼器

    類別： **MFT \_ 類別 \_ 影片 \_ 編碼器**

    主要類型： MFMediaType \_ 影片

    子類型： MFVideoFormat \_ WVC1、MFVideoFormat \_ WMV3、MFVideoFormat \_ WMV2、MFVideoFormat \_ WMV1

媒體基礎提供數個函式，可讓您的應用程式呼叫以列舉系統中可用的各種編碼器。 編碼器會註冊為 COM 物件，且登錄專案會遵循 COM class factory 的標準格式。 登錄會維護編碼器的 Clsid，以媒體格式 (音訊或影片) 分類。 Windows 媒體編碼器的類別識別碼會定義為 wmcodecdsp .h 標頭檔中的常數。 在媒體基礎中，您可以藉由指定分類、支援的輸入類型和支援的輸出類型，透過呼叫 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) 或 [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) 來註冊編碼器。 成功註冊這些函式時，媒體基礎的列舉函數會考慮 MFTs。

若要建立編碼器 MFT 的實例，應用程式具有下列選項。

-   直接建立編碼器 MFT，並接收指向 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的指標。 如需詳細資訊，請參閱 [使用 CoCreateInstance 建立編碼器](using-an-encoder-s-imftransform--interface.md)。
-   為編碼器 MFT 建立啟用物件的實例，並接收 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。 如需詳細資訊，請參閱 [使用編碼器的啟用物件](using-an-encoder-s-activation-objects.md)。

如果您的應用程式使用 [管線層 ASF 元件](pipeline-layer-asf-components.md) 將檔案編碼為 ASF 格式，您必須將編碼器 MFT 插入管線中作為轉換節點。 在編碼拓撲中建立轉換節點時，您可以將物件類型設定為 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面或 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 物件的指標。 媒體基礎提供 Windows 媒體編碼器的啟始物件，以便方便設定為編碼拓撲中的轉換節點。 當拓撲解決之後，媒體會話會使用啟用物件來建立編碼器 MFT 的實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows媒體編碼器](windows-media-encoders.md)
</dt> </dl>

 

 



