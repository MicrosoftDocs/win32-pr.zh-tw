---
title: 重複使用串流設定
description: 重複使用串流設定
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- 串流，重複使用設定
- 設定檔，重複使用串流設定
- 重複使用串流設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ee1a2b51d5a2a659cb24955ab74a5fb285308125b21781c9d42a709d7e4b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110188"
---
# <a name="reusing-stream-configurations"></a>重複使用串流設定

有時您會想要重複使用現有設定檔中的串流設定物件。 您可能會有需要更新的舊設定檔，或您可能需要與系統設定檔中的相同的資料流程。 您可以更輕鬆地重複使用串流設定，而不是建立新的串流設定，而且您通常可以變更設定中的一些設定，以符合您的需求，而不是建立全新的設定。

請注意，您可以變更資料流程設定的方式有所限制。 如果您以錯誤的方式變更設定，您的設定檔可能不會接受串流設定物件。 設定檔通常會接受不正確的串流設定，但會導致寫入器物件拒絕設定檔。 使用和修改現有的串流設定時，請注意下列限制和問題。

-   絕對不要改變 prx 檔案的內容以變更資料流程設定。 當設定檔儲存至 XML 字串並寫入至 prx 檔案時，可以使用任何文字編輯器來讀取這些設定檔。 查看儲存的設定檔可協助您瞭解設定檔的運作方式。 不過，您絕對不應該以任何方式改變 prx 檔。 即使是看似簡單的變更，也可能使設定檔無效。
-   Windows Media 音訊編解碼器的數個版本使用相同的串流設定。 如果您有設定為子類型 WMMEDIASUBTYPE \_ WMAudioV2、WMMEDIASUBTYPE \_ WMAudioV7 或 WMMEDIASUBTYPE WMAudioV8 的串流設定物件 \_ ，則會使用最新的 Windows Media 音訊編解碼器來壓縮產生的串流。 不過，在使用現有的音訊編解碼器之前，您應該先評估您的需求。 您可以藉由升級至最新版的 Windows Media 音訊 Professional 編解碼器或 Windows Media 音訊的無失真編解碼器，來改善許多檔案類型。
-   請勿變更資料流程的子類型，以升級為新的編解碼器。 當您使用 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 的方法來取得資料流程設定時，編解碼器會附加一些資料來識別位流格式。 如果您變更現有資料流程設定物件的子類型，子類型將不會符合編解碼器資料。 寫入器物件不會接受具有這類串流設定的設定檔。
-   請勿改變壓縮音訊串流設定的設定。 如果音訊串流的設定不符合您的需求，請使用 **IWMCodecInfo3** 的方法從編解碼器取得新的串流設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**從編解碼器取得串流設定資訊**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




