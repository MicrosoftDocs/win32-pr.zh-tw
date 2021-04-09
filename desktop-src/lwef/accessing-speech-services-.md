---
title: " (Microsoft Agent Control) 存取語音服務"
description: 存取語音服務
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83459cfd7ee478fca7d2cf2d25c4c1d590d8ed54
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685447"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a> (Microsoft Agent Control) 存取語音服務

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

雖然 Microsoft 代理程式的服務包括對語音輸入的支援，但必須安裝相容的命令和控制語音辨識引擎，才能存取代理程式的語音輸入服務。 同樣地，如果您想要使用 Microsoft Agent 的語音服務來支援合成字元的合成語音輸出，您必須為您的字元安裝相容的文字轉換語音 (TTS) 語音引擎。

若要在您的應用程式中啟用語音輸入支援，請定義 [**命令**](https://www.bing.com/search?q=**Command**) 物件並設定其 [**Voice**](https://www.bing.com/search?q=**Voice**) 屬性。 代理程式將會自動載入語音服務，因此當使用者按 [**下接聽鍵或接聽電話時**](https://www.bing.com/search?q=**Listen**)，將會載入語音辨識引擎。 根據預設，字元的 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) 會決定載入的引擎。 代理程式嘗試載入 Microsoft Speech API (SAPI) 傳回的第一個引擎，使其符合此語言。 如果您想要載入特定的引擎，請使用 [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) 。

若要啟用文字到語音轉換輸出，請使用「 [**說話**](https://www.bing.com/search?q=**Speak**) 」方法。 代理程式會自動嘗試載入符合字元 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)的引擎。 如果字元的定義包含特定的 TTS 引擎模式識別碼，且該引擎可供使用且符合該字元的 **LanguageID**，則代理程式會為該字元載入該引擎。 如果不是，則會載入 SAPI 傳回的第一個 TTS 引擎，以符合字元的語言設定。 您也可以使用 [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) 來載入特定的引擎。

一般情況下，代理程式會在接聽模式起始時載入語音辨識，並在第一次呼叫 [**說話**](https://www.bing.com/search?q=**Speak**) 時載入文字轉換語音引擎。 但是，如果您想要預先載入語音引擎，請查詢與語音介面相關的屬性。 例如，查詢 [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) 或 [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) 會嘗試載入該類型的引擎。

因為 Microsoft 代理程式的語音服務是以 Microsoft Speech API 為基礎，所以您可以使用任何支援所需語音介面的引擎。

 

 




