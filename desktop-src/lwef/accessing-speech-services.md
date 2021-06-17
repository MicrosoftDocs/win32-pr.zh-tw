---
title: " (Microsoft 代理程式伺服器介面存取語音服務) "
description: 瞭解如何使用 Microsoft Agent 伺服器介面存取語音服務。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bf5cf88141344d5328592c9e823c7365c5d5
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262700"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a> (Microsoft 代理程式伺服器介面存取語音服務) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

雖然 Microsoft 代理程式的服務包括對語音輸入的支援，但必須安裝相容的命令和控制語音辨識引擎，才能存取代理程式的語音輸入服務。 同樣地，如果您想要使用 Microsoft Agent 的語音服務來支援合成字元的合成語音輸出，您必須為您的字元安裝相容的文字轉換語音 (TTS) 語音引擎。 由於 Microsoft 代理程式的語音服務是以 Microsoft Speech API (SAPI) 為基礎，因此您可以使用相容性支援所需語音介面的任何引擎。

若要在您的應用程式中啟用語音輸入支援，請定義 [**命令**](https://www.bing.com/search?q=**Command**) 物件並設定其 [**Voice**](https://www.bing.com/search?q=**Voice**) 屬性。 Microsoft Agent 會自動載入語音服務，因此當使用者按下接聽鍵或撥打 [**接聽**](https://www.bing.com/search?q=**Listen**)時，就會載入語音辨識引擎。 依預設，字元的語言識別項會決定要載入的引擎。 代理程式會嘗試載入由 SAPI 傳回的第一個引擎，使其符合此語言。 如果您想要載入特定的引擎，請使用 **IAgentCharacterEx：： SetSRModeID** 。

若要啟用文字到語音轉換輸出，請使用「 [**說話**](https://www.bing.com/search?q=**Speak**) 」方法。 Microsoft Agent 會自動嘗試載入符合字元語言識別項的引擎。 如果字元的定義包含特定的 TTS 引擎模式識別碼，且該引擎可供使用且符合字元的語言識別項，則代理程式會為該字元載入該引擎。 如果不是，Agent 會載入由 SAPI 傳回的第一個 TTS 引擎，以符合字元的語言設定。 您也可以使用 **IAgentCharacterEx：： SetTTSModeID** 載入特定的引擎。

一般而言，Microsoft Agent 會在接聽模式起始時載入語音辨識引擎，並在第一次呼叫 [**說話**](https://www.bing.com/search?q=**Speak**) 時載入文字轉換語音引擎。 但是，如果您想要預先載入語音引擎，您可以藉由查詢與語音介面相關的屬性來完成這項作業。 例如，呼叫 **IAgentCharacterEx：： GetSRModeID** 或 **IAgentCharacterEx：： GetTTSModeID** 將會嘗試載入該類型的引擎。

 

 




