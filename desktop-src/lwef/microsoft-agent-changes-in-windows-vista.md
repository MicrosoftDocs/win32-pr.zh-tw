---
title: Windows Vista 中的 Microsoft Agent 變更
description: Windows Vista 中的 Microsoft Agent 變更
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73af45553f876c413fbea906de2369e888f1483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183635"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Windows Vista 中的 Microsoft Agent 變更

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

Windows Vista 引進語音和語音辨識與 Windows Vista 互動的一些變更。

Microsoft Agent 現在支援 SAPI 5 文字轉換語音和語音辨識元件。 代理程式物件的 TTSModeID 和 SRModeID 屬性仍會用來判斷針對代理程式選取的語音或辨識器，以及改變此選取專案。 SAPI 4 模式會顯示為 GUID 字串（例如 "{ca141fd0-ac7f-11d1-97a3-006008273000}"），而 SAPI 5 權杖 (相當於模式) 會顯示為一般名稱，例如 "Microsoft Anna"。 如同在舊版中，此代理程式會建立預設的 TTS 和 SR 引擎選項。 如果已安裝 SAPI 5 引擎，則這些引擎一律會優先于任何可能安裝的 SAPI 4 引擎。 如果使用者的性別符合該字元，則會使用使用者的預設文字轉換語音引擎（如 [控制台] 中所指定），否則會選擇相同性別的 SAPI 5 引擎（如果有的話）。 如果有 SAPI 5 引擎，則會忽略直接在字元上指定的模式識別碼。 您可以讀取腳本開頭的 TTSModeID 和 SRModeID 屬性，以驗證預設的選取專案。

如同之前，如果文字轉換語音或語音辨識功能不存在，TTSModeID 和 SRModeID 將會傳回空白字串。 您可以藉由將這些屬性設定為適當的 SAPI 4 模式字串或 SAPI 5 權杖名稱，來選取特定的語音或辨識器。 設定特定模式或權杖之後，您也可以再次讀取屬性，以確認它的值已被採用，這表示新的模式或權杖確實可用，且已成功選取。 針對透過 web 部署代理程式的開發人員，請注意，有許多 Vista 使用者已經安裝一或多個 SAPI 5 語音，因此您可能會想要避免自動下載 SAPI 4 語音，除非您的腳本明確要求，否則下載的聲音將不會最後使用。

SAPI 5 文字轉換語音引擎所使用的一組標準與 SAPI 4 不同，以使用標記來標注語音，例如變更語音的音調或速率。 在 SAPI 4 中，您可以使用「斜線」命令，例如/pit = 170/。 在 SAPI 5 中，您會使用 XML 標記，例如 <PITCH MIDDLE="5"/> 。 在 Vista 中，代理程式將會在「朗讀」方法字串中接受兩種類型的批註：「斜線」命令將會被 SAPI 5 引擎忽略，而「SAPI 4 引擎」將會忽略 XML 標記。 和斜線標記一樣，支援 SAPI 5 的 XML 標記會因廠商而異，而某些廠商可能會支援其他標記。 如需有關 SAPI 5 XML 標記的詳細資訊，請參閱 SAPI 5 規格。

代理程式已不再支援多種語言。 代理程式所使用的語言一律會假設為使用者目前的語言，並向作業系統註冊。 Agent 物件的 LanguageID 屬性仍然是可寫入的，但 Vista 上的代理程式會忽略它的值。 例如，如果使用者的語言設定為美式英文 (&H0409) ，而他或她使用將 LanguageID 設定為法文 (&H040C) 的程式，則 [語音提示文字] 和 [先進字元選項] 對話方塊仍會以英文顯示。

 

 




