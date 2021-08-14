---
title: 合成語音支援
description: 合成語音支援
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31fcb655ccb5a8fbb2ffbbb8d01d1da317209fbfa3e270a76d92208c06777df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475320"
---
# <a name="synthesized-speech-support"></a>合成語音支援

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

如果您使用合成的語音，則您的字元可以說出幾乎所有的功能，以提供最大的彈性。 有了錄製的音訊之後，您可以為字元提供特定或唯一的聲音。 若要指定輸出，請將說出的文字提供為 [**說話**](speak-method.md) 方法的參數。

因為 Microsoft 代理程式的架構使用 Microsoft SAPI 來進行合成語音輸出，所以您可以使用符合此規格的任何引擎，並支援使用 [**ITTSNotifySinkW**](ittsnotifysinkw.md)介面的 [**視覺**](https://www.bing.com/search?q=**Visual**)方法 (IPA) 輸出的國際注音字母。 如需有關引擎所需的詳細資訊，請參閱 [語音引擎支援需求](requirements-for-text-to-speech-engines.md)。

字元的語言識別項設定會決定其 TTS 輸出。 如果用戶端未指定字元的語言識別項，則字元的語言識別項會設定為使用者預設語言識別項。 如果字元的定義包含特定的引擎，而且可以載入該引擎並且符合字元的語言設定，則會使用該引擎。 否則，Microsoft Agent 會列舉其他可用的引擎，並根據該順序中的語言、性別和年齡 (要求最符合的 SAPI) 。 如果沒有任何相符的引擎可供使用，就不會有該用戶端使用字元的 TTS 輸出。 代理程式會嘗試在第一個 [**說話**](speak-method.md) 呼叫上載入 TTS 引擎，或在您查詢或成功設定其模式識別碼時載入。

用戶端應用程式也可以使用 [**TTSModeID**](ttsmodeid-property.md) 屬性) ，指定其字元 (的 TTS 引擎。 這會覆寫伺服器嘗試根據字元慣用的 TTS 模式識別碼或字元的目前語言識別項設定，自動尋找相符的引擎。 但是，如果該引擎未安裝 (或無法) 載入，則呼叫會失敗 (並在控制項) 中引發錯誤。 然後伺服器會嘗試根據語言識別項、編譯的字元 TTS 設定和可用的 TTS 引擎載入另一個引擎。 如果仍然沒有相符的情況，則不會提供 TTS 給該用戶端，但該字元仍然可以說出其字組氣球。

只有任何用戶端所使用的 TTS 引擎仍會繼續載入。 例如，如果某個字元具有特定引擎的定義喜好設定，但該引擎可供使用，但您的用戶端應用程式已指定不同的引擎 (，方法是設定不同于引擎的字元語言識別項，或指定不同的模式識別碼) ，只有應用程式所指定的引擎會保持載入。 除非有另一個用戶端使用字元的已編譯引擎設定) ，否則會卸載符合為 TTS 設定之字元定義喜好設定的引擎 (。

 

 




