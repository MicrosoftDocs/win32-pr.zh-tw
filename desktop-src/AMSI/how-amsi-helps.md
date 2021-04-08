---
title: AMSI 如何協助您抵禦惡意軟體
description: 作為應用程式開發人員，您可以主動參與惡意程式碼防護。 具體來說，您可以協助保護您的客戶免于動態的腳本式惡意程式碼，以及從網路攻擊的非傳統途徑。
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671632"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>反惡意程式碼掃描介面 (AMSI) 如何協助您抵禦惡意程式碼

如需 Windows 反惡意程式碼掃描介面 (AMSI) 的簡介，請參閱 [反惡意程式碼掃描介面 (AMSI) ](antimalware-scan-interface-portal.md)。

作為應用程式開發人員，您可以主動參與惡意程式碼防護。 具體來說，您可以協助保護您的客戶免于動態的腳本式惡意程式碼，以及從網路攻擊的非傳統途徑。

以範例為例，假設您的應用程式可編寫腳本：它接受任意的腳本，並透過腳本引擎執行。 在腳本準備好提供給腳本引擎的時候，您的應用程式可以呼叫 Windows AMSI Api 來要求掃描內容。 如此一來，您就可以安全地判斷腳本是否為惡意，然後再決定是否要繼續執行。

即使腳本是在執行時間產生的也是如此。 腳本 (惡意或) ，可能會經歷數次的消除混淆。 但是您最終必須以簡單、未混淆的程式碼提供腳本引擎。 這就是您叫用 AMSI Api 的那個點。

以下是 AMSI 架構的圖例，其中您的應用程式是由其中一個 [其他應用程式] 方塊表示。

![AMSI 架構](images/AMSI7Archi.jpg)

Windows AMSI 介面已開啟。 這表示任何應用程式都可以呼叫它;而且任何已註冊的反惡意程式碼引擎都可以處理提交給它的內容。

我們不想要將討論限制在腳本引擎的討論範圍。 您的應用程式可能是通訊應用程式，它會在向您的客戶顯示時，先掃描立即病毒的訊息。 或者，您的軟體可能是在安裝外掛程式之前驗證外掛程式的遊戲。 使用 AMSI 有許多機會和案例。

## <a name="amsi-in-action"></a>AMSI 實際操作

讓我們來看看 AMSI 的實際運作方式。 在此範例中，Windows Defender 是呼叫 AMSI Api 的應用程式。 但是，您可以從自己的應用程式中呼叫相同的 Api。

以下是使用 XOR 編碼技術來隱藏意圖的腳本範例 (該意圖是否為良性或不) 。 在此圖中，我們可以想像此腳本是從網際網路下載。

![以 Base64 編碼的範例腳本](images/AMSI8.png)

為了讓事情更有趣，我們可以在命令列手動輸入此腳本，如此就不會有實際的檔案可供監視。 這會鏡像所謂的「無檔案威脅」。 這並不像是在磁片上掃描檔案一樣簡單。 威脅可能是只有在電腦記憶體中的後門。

接下來，我們會看到在 Windows PowerShell 中執行腳本的結果。 您會看到 Windows Defender 能夠在這個複雜的案例中偵測 AMSI 測試範例，只是使用標準 AMSI 測試範例簽章。

![Windows Defender 偵測 AMSI 測試範例](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>AMSI 與 JavaScript/VBA 整合

以下所述的工作流程說明另一個範例的端對端流程，我們會在其中示範 AMSI 與 Microsoft Office 內的宏執行整合。

![AMSI 與 JavaScript/VBA 整合](images/integ-js-vba.png)

- 使用者會收到包含 (惡意) 宏的檔，evades 靜態防毒軟體掃描，方法是採用像是模糊化、受密碼保護的檔案等技術。
- 然後，使用者會開啟包含 (惡意) 宏的檔。 如果檔在 [受保護的檢視] 中開啟，則使用者按一下 [ **啟用編輯** ] 以結束受保護的檢視。
- 使用者按一下 [ **啟用宏** ] 以允許執行宏。
- 當宏執行時，VBA 執行時間會使用迴圈緩衝區來記錄 \[ 與 \] WIN32、COM 和 VBA api 呼叫相關的1資料和參數。
- 當被視為高風險的特定 Win32 或 COM Api (也稱為 *觸發* 程式) \[ 2 時 \] ，會停止執行宏，而迴圈緩衝區的內容會傳遞至 AMSI。
- 註冊的 AMSI 反惡意程式碼服務提供者會以判斷提示回應，指出宏行為是否為惡意。
- 如果行為不是惡意的，則會繼續執行宏。
- 否則，如果行為是惡意的，則 Microsoft Office 會關閉會話以回應警示 \[ 3 \] ，而 AV 可隔離檔案。

## <a name="what-does-this-mean-for-you"></a>這對您的意義為何？

針對 Windows 使用者，任何在 Windows 10 內建腳本主機上使用模糊化和規避技術的惡意軟體，都會自動以比以往更深層的方式進行檢查，以提供額外的保護層級。

如果您是應用程式開發人員，請考慮讓您的應用程式呼叫 Windows AMSI 介面，如果您想要從 (獲益，並使用) 額外的潛在惡意內容掃描和分析來保護您的客戶。

作為防毒軟體廠商，您可以考慮針對 AMSI 介面執行支援。 當您這樣做時，您的引擎將可深入瞭解應用程式 (包含 Windows 10 內建腳本主機的資料，) 考慮可能是惡意的。

## <a name="more-background-info-about-fileless-threats"></a>更多有關無檔案威脅的背景資訊

您可能想要取得有關 Windows AMSI 設計來協助您防禦的無檔案威脅種類的詳細背景資訊。 在本節中，我們將探討惡意程式碼生態系統中的傳統貓和滑鼠遊戲。

我們會使用 PowerShell 作為範例。 但是，您可以利用與任何動態語言（ &mdash; VBScript、Perl、Python、Ruby 等）所示範的相同技巧和流程。

以下是惡意 PowerShell 腳本的範例。

![惡意 PowerShell 腳本範例](images/AMSI1.png)

雖然此腳本只會將訊息寫入畫面，但惡意程式碼通常更是惡意的。 但是，您可以輕鬆地撰寫簽章來偵測這種簽章。 例如，簽章可以搜尋「寫入主機 ' pwnd！ '」字串 在使用者開啟的任何檔案中。 好：我們偵測到我們的第一種惡意程式碼！

不過，在我們的第一個簽章偵測到之後，惡意程式碼作者會回應。 它們會藉由建立動態腳本來回應，例如此範例。

![動態腳本的範例](images/AMSI2.png)

在該案例中，惡意程式碼作者會建立字串，代表要執行的 PowerShell 腳本。 但它們會使用簡單的字串串連技術來中斷先前的簽章。 如果您曾看到載入網頁的來源，您將會看到此技術的許多實例用來避免廣告封鎖軟體。

最後，惡意程式碼作者會將這個串連的字串傳遞給 `Invoke-Expression` Cmdlet &mdash; PowerShell 的機制，以評估在執行時間撰寫或建立的腳本。

在回應中，反惡意程式碼軟體會開始進行基礎語言模擬。 例如，如果我們看到兩個串連的字串，則我們會模擬這兩個字串的串連，然後在結果上執行簽章。 可惜的是，這是一種相當脆弱的方法，因為語言通常會有許多方式來表示和串連字號串。

因此，在此簽章攔截之後，惡意程式碼作者會移至更複雜 &mdash; 的內容，例如，以 Base64 編碼腳本內容，如下列範例所示。

![Base64 的腳本內容範例](images/AMSI3.png)

資源，大部分的反惡意程式碼引擎也都採用 Base64 解碼模擬。 因此，由於我們也會執行 Base64 解碼模擬，因此我們將會提前一段時間。

在回應中，惡意程式碼作者會移至演算法模糊化， &mdash; 例如它們執行的腳本中的簡單 XOR 編碼機制。

![演算法模糊化腳本的範例](images/AMSI4.png)

到目前為止，我們已經超過防毒程式會模擬或偵測到的內容，因此我們不一定會偵測到此腳本的作用。 不過，我們可以開始根據模糊化和編碼技巧來撰寫簽章。 事實上，這就是針對以腳本為基礎之惡意程式碼的大部分簽章的帳戶。

但是如果混淆器很簡單，那麼它看起來就像是很重要的腳本呢？ 它的簽章會產生無法接受的誤報數目。 以下是範例 *stager* 腳本，它本身無法偵測到太良性。

![範例 stager 腳本，太無害，無法自行偵測](images/AMSI5.png)

在該範例中，我們會下載網頁，並叫用其中的一些內容。 以下是 Visual Basic 腳本中的對等專案。

![Visual Basic 腳本中的對等專案](images/AMSI6.png)

這兩個範例中的專案越糟，防毒軟體引擎會檢查使用者開啟的檔案。 如果惡意內容只存在於記憶體中，則可能會偵測到攻擊。

本節說明使用傳統簽章偵測的限制。 但是，雖然惡意腳本可能會經歷數個消除混淆的行程，但最終需要以純 unobfuscated 程式碼提供腳本引擎。 然後，在 &mdash; 上述第一節中所述， &mdash; Windows 10 的內建腳本主機呼叫 AMSI api 來要求掃描這個未受保護的內容。 而您的應用程式也可以達成相同的目的。

## <a name="related-resources"></a>相關資源

* [無檔案型態威脅](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI：新娘惡意宏的](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [看不見但不可見：失去無檔案惡意程式碼與行為監視、AMSI 和下一代 AV](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
