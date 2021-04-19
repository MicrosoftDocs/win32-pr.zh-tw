---
title: 存取程式碼中的語音引擎
description: 存取程式碼中的語音引擎
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106983296"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>存取程式碼中的語音引擎

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

若要在您的程式碼中使用特定的語音引擎，請使用代理程式 API 來設定引擎。 針對語音輸入引擎，請使用 [**SRModeID**](https://www.bing.com/search?q=**SRModeID**)來指定引擎的模式識別碼。 不過請注意，必須安裝引擎。 若要判斷引擎是否存在，您可以查詢 **SRModeID**。 引擎必須符合字元的 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) 設定。 例如，您不能將 **LanguageID** 為法文的字元的 **SRModeID** 設定為德文語音辨識引擎模式識別碼。

**語音輸入引擎模式識別碼**



| 語音                                    | 模式識別碼                             |
|------------------------------------------|--------------------------------------|
| Microsoft 語音辨識引擎 v4。0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

請先檢查並設定程式碼中的字元 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) 和 [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) ，然後再嘗試為您的應用程式定義 **命令** 物件之語音參數的文法。 也請考慮檢查瀏覽器或系統語言，以確定您可以符合使用者的設定。 如果您嘗試為引擎不相符的語言定義文法，引擎可能會失敗。

文字轉換語音 (TTS) 輸出的字元集可以使用預設語音輸出引擎的模式識別碼喜好設定來進行編譯。 載入字元時，如果已安裝引擎且符合該字元的 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)，則代理程式會嘗試載入該模式識別碼以用於語音輸出。 如果引擎不存在或有不同的 **LanguageID**，則代理程式會嘗試載入它找到符合字元 **LanguageID** 的第一個模式識別碼，但仍會設定字元的編譯速度和音調設定。

請注意，由於所有 Microsoft 代理程式提供的字元都會編譯為使用 Lernout & Hauspie TruVoice 美式英文引擎作為預設的語音輸出引擎，因此會針對此語言和引擎調整字元的速度和音調設定。 因此，當您使用其他 TTS 引擎或其他語言的引擎時，這些字元可能不會以最佳的音調或速度說話。 雖然您的應用程式或網頁無法撰寫 [**音調**](/previous-versions/ms809428(v=msdn.10)) 和 [**速度**](https://www.bing.com/search?q=**Speed**) 屬性值，但是您可以在輸出文字中包含 [Pit](pit-tag.md) (的) 和 [Spd](spd-tag.md) (速度) 標記，以暫時變更特定語句的音調和速度。 不過，使用 Pit 和 Spd 標記並不會變更 **音調** 和 **速度** 屬性。 如需詳細資料，請參閱 [程式設計 Microsoft Agent 控制項](programming-the-microsoft-agent-control.md) 和 [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md) 。

您也需要安裝 SAPI 4.0 執行時間二進位檔 (SPCHAPI.exe) 使用的是與 L&H TruVoice 美式英文引擎（使用 Microsoft 代理程式提供的字元）的其他 SAPI 相容 TTS 引擎，以便正確列舉引擎。 從您的網頁中，包含下列物件標記以自動安裝元件：

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

若要查詢或設定引擎的模式識別碼，請使用 [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**)。 使用 **TTSModeID** ，您可以設定不同于字元 [**LANGUAGEID**](https://www.bing.com/search?q=**LanguageID**)的模式識別碼。 例如，您可以設定德文字元來使用法文模式識別碼說話。 語音輸出引擎模式識別碼不只會定義您使用的引擎，也會對應至引擎所支援的特定語音。 您也可以使用 Microsoft 代理程式字元編輯器或 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx) 中包含的工具，來查詢您系統上所安裝之 TTS 引擎的模式識別碼。

**語音輸出模式識別碼**



| 語音                                       | 模式識別碼                               |
|---------------------------------------------|----------------------------------------|
| 成人女性 \# 1、US 英文、L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| 成人女性 \# 2、US 英文、L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| 成人男性 \# 1、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| 成人男性 \# 2、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| 成人男性 \# 3、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| 成人男性 \# 4、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| 成人男性 \# 5、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| 成人男性 \# 6、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| 成人男性 \# 7、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| 成人男性 \# 8、US 英文、L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol、英屬英文、L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter、英屬英文、L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Linda、荷蘭文、L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander、荷蘭文、L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique、法文、L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| 聖皮爾、法文、L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna、德文、L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan、德文、L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Barbara、義大利文、L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Stefano、義大利文、L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naoko、日文、L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji、日文、L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shin-Ah、韓文、L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| 六月-Ho、韓文、L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Juliana，葡萄牙文 (巴西) ，L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Alexandre，葡萄牙文 (巴西) ，L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana、俄文、L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Boris、俄文、L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Carmen、西班牙文、L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio、西班牙文、L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> 語音引擎的安裝 CLSID 與其模式識別碼之間有差異。 同樣地，語音引擎也有引擎識別碼，但此識別碼不適用於代理程式 API。

 

 

 