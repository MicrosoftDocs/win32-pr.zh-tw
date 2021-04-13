---
title: 輸出問題
description: 輸出問題
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d909052feb2463637a8eab6343353f0af617c06
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314394"
---
# <a name="output-problems"></a>輸出問題

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>字元會在移動時離開影像或軌跡。

當代理程式字元產生動畫時，需要在該字元後方的應用程式視窗及時更新。 當字元在畫面上移動時，有時會看到一些殘留的影像，會因為您的電腦速度和您) 執行的應用程式而快速消失 (。 如果沒有，則可能是下列原因所造成：

-   您的系統不符合代理程式的最低系統需求。
-   字元後方的應用程式視窗不會及時處理更新。 請嘗試將字元拖曳到桌面或資料夾視窗，或關閉部分應用程式。 如果您發現明顯的改進，可能無法避免問題。
-   您可能未安裝 Microsoft Internet Explorer 4.0 (或更新) 版本的正式發行版本。 早于 Internet Explorer 4.0 的發行前版本未正確地處理更新畫面。 這會導致畫面上剩餘的剩餘字元影像。 若要修正此問題，請安裝最新的官方版本 Internet Explorer ([https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx)) 。
-   您系統的螢幕驅動程式或硬體可能發生問題。 確定您有圖形硬體的最新驅動程式。 如果問題仍然持續發生，您可能會想要聯繫電腦廠商。

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>字元不會在說話時產生任何音訊輸出。

此徵兆可能有數個原因。 請嘗試下列各項以找出問題：

-   確認您的喇叭已插入，且音效卡與 Windows 相容。 最好是使用另一個音效應用程式來測試，以確認音訊輸出正常運作。
-   確認已啟用代理程式的應用程式或網頁支援語音輸入。 並非所有範例頁面都支援語音輸入。 按住接聽鍵 (通常這會是滾動鎖的按鍵，除非您將它變更) 。快顯視窗應該會出現在字元下方。 提示中的文字會告訴您該字元的接聽狀態。 如果未顯示任何提示，表示應用程式或網頁不支援語音輸入，或是您未安裝相容的語音引擎。 如果出現提示，並指出該字元正在接聽，請說出其中一個字元的語音命令。 如果您不知道有哪些聲音命令可供使用：請放開接聽按鍵，然後以滑鼠右鍵按一下字元，然後從快顯功能表中選擇 [開啟語音命令] 視窗。 如果未出現命令，則表示您所使用的應用程式或網頁無法使用語音支援。 如果出現，請再次按下並按住接聽金鑰。 如果接聽提示出現在字元下方，並指出該字元正在接聽，請說出視窗中所列的其中一個命令。 如果字元沒有回應，請移至下一個步驟。
-   確認目前沒有其他應用程式正在使用音訊輸出裝置。
-   確認您使用的字元已針對語音輸出進行設定。  (您可能需要向網站或應用程式供應商確認。 ) 
-   確認您的 Microsoft 代理程式設定已啟用語音輸出
-   如果字元使用文字轉換語音 (TTS) 引擎來產生語音輸出，請確認您已安裝相容的 TTS 引擎。 例如，當安裝為 Internet Explorer 4.0 附加元件時，只會安裝 Microsoft Agent 的核心元件。 核心元件不包含文字轉換語音引擎。 若沒有此 TTS 引擎 (與 Microsoft Speech API 相容的引擎) ，Microsoft 代理程式範例字元將不會產生語音輸出。
-   確認 Microsoft 代理程式的 MIDI 使用未封鎖音訊頻道 (請參閱下一個主題，播放 MIDI 的應用程式在執行 Microsoft 代理程式) 時沒有音訊輸出。

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>當 Microsoft 代理程式正在執行時，播放 MIDI 的應用程式沒有音訊輸出。

當您按下接聽鍵時，Microsoft Agent 會使用 MIDI 來播放音訊。 如果您發現這會干擾其他播放 MIDI 或干擾語音輸入的應用程式，您可以在 [Microsoft 代理程式內容] 的 [說話] 選項時關閉播放音訊。

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>我收到下列訊息：無法進行外寄呼叫，因為應用程式正在分派輸入同步呼叫。

此訊息可能會在下列情況下發生：

以滑鼠右鍵按一下頁面的 [工作列] 專案，並從快顯功能表中選擇 [關閉] 時，就會顯示包含 Microsoft Agent 的網頁 () ，這可能會發生。 這是因為代理程式和瀏覽器之間的時間問題同時關閉。 錯誤是無害的。 按一下 [確定] 以關閉訊息。

發生這種情況時， (或應用程式) 嘗試要求特定的文字轉換語音 (TTS) 引擎。 未安裝 Speechapi.dll。

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>語音引擎似乎不會在 Windows XP 中使用 Microsoft Agent？

Microsoft 代理程式使用 SAPI 4.0 來提供語音服務。 不過，Windows XP 現在隨附于 SAPI 5.0，這不會為其前身提供回溯相容性支援。 幸運的是，在相同的 Windows XP 電腦上，也可以同時存在 SAPI 4.0 和 SAPI 5.0。

若要讓語音引擎可搭配 Windows XP 中的 Microsoft 代理程式使用，請先安裝 [SAPI 4.0 執行時間二進位](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)檔，然後安裝特定的語音引擎。

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>在升級到 Windows XP 之前，用來與 Microsoft 代理程式搭配使用的語音引擎。 發生什麼事？

請參閱先前的問題和解答。 Windows XP 的升級程式可能已經移除電腦上現有的 SAPI 4.0 支援。 升級至 Windows XP 之後，請重新安裝 SAPI 4.0 runtime 和 SAPI 4.0 語音引擎。

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>我將 TTS3000 的文字轉換語音引擎安裝到執行 Windows XP (或 Windows 2000) 的電腦上，並據此正確編輯我的程式設計。 當我或其他本機系統管理員登入時，Microsoft 代理程式字元會使用這些 TTS3000 的文字轉換語音引擎來說語音，而不是在 *沒有系統管理員許可權* 的其他使用者登入此電腦時。 在 Windows 98 和 Windows Me 上，這些 TTS3000 的文字轉換語音引擎可針對這兩組使用者正常運作。 我該怎麼辦？

您必須為 TTS3000 文字轉換語音引擎的某些登錄機碼設定安全性許可權，才能讓使用者帳戶在沒有系統管理員許可權的情況下使用。 您可以使用作業系統的登錄編輯程式來完成這項作業。

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>我依照上述問題所述之問題的解決方案，來說明此程式。 如此一來，當 *沒有系統管理員許可權* 的使用者登入 windows XP (或 windows 2000) 電腦時，Microsoft 代理程式字元就可以使用這些 TTS3000 的文字轉換語音引擎來說語音。 接下來幾個月，這些相同的 TTS3000 文字轉換語音引擎已停止運作。 發生什麼事？

當您遵循先前問題所提供的說明程式時，這會提供非系統管理員的使用者帳戶，並具備所需登錄機碼的「完全控制」許可權。 其中一個使用者可能已故意或不知不覺地編輯這些值、再次變更許可權，或甚至完全刪除登錄機碼。

檢查這些登錄機碼及其許可權是否已編輯、刪除，或自之後變更。 如有必要，請再次變更這些登錄機碼及其許可權，或重新安裝 TTS3000 文字轉語音。

 

 




