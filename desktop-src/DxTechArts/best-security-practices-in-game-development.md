---
title: 遊戲開發的最佳安全性作法
description: 本文討論在遊戲開發中使用的最佳做法。
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba4f02d5e1a2e3da2e50feedd89f085a0c063be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842471"
---
# <a name="best-security-practices-in-game-development"></a>遊戲開發的最佳安全性作法

本文討論在遊戲開發中使用的最佳做法。

-   [簡介](#introduction)
-   [不安全的程式碼範例](#examples-of-insecure-code)
-   [改善安全性的方法](#ways-to-improve-security)
-   [總結](#summary)

## <a name="introduction"></a>簡介

有越來越多的人使用使用者製作的內容來玩線上遊戲和遊戲。 這與 Microsoft Windows 作業系統的提高安全性結合，表示遊戲是不斷成長且更吸引人的目標，可讓攻擊者入侵。 遊戲開發人員應該特別強調，以確保他們發行的遊戲不會建立新的安全性漏洞，讓攻擊者得以入侵。 遊戲開發人員必須負責協助防止客戶的電腦遭到惡意網路資料、使用者修改或篡改攻擊，而有意。 如果惡意探索弱點，可能會導致客戶和/或金錢損失。 本文概述並說明在不因而誇大開發時間的情況下，可提高程式碼安全性的一些常見方法和工具。

發行產品時，開發團隊所做的三個最常見的錯誤包括：

-   需要系統管理許可權。 遊戲應該不需要系統管理許可權。 如需詳細資訊，請參閱 [遊戲開發人員的使用者帳戶控制](./user-account-control-for-game-developers.md)。
-   未使用自動保護。 開發人員通常不會使用 **/gs**、 **/SAFESEH** 或 **/NX**。 使用這些編譯/連結旗標可以找出或消除許多基本的安全性漏洞，而不會大幅增加工作負載。 本文稍後會討論這些旗標。
-   使用禁止的 Api。 有許多 Api (**strcpy**、 **strncpy** 等，而且很容易發生程式設計人員錯誤並輕鬆產生安全性漏洞的) 。 開發人員應該以安全的版本取代這些 Api。 Visual Studio 2005 提供分析二進位檔案的工具，可自動檢查目的檔是否有 unsafe Api 的參考。 如需有關使用此工具所產生之資訊的詳細資訊，請參閱 Martyn Lovell [的 Visual Studio 2005 Safe C 和 c + + 程式庫的程式碼足以擊退攻擊](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) 。 此外，您也可以取得 [禁止的 .h](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) 標頭檔，以協助您從程式碼中移除禁用的函式。

每個所列出的錯誤都不只是常見的，但在開發工作負載、編碼標準或功能方面都沒有重大變更，可輕鬆地進行修正。

## <a name="examples-of-insecure-code"></a>不安全的程式碼範例

以下是讓攻擊者執行緩衝區溢位攻擊所需的簡單範例：


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



在表面上，這段程式碼看起來沒問題，它會在所有的情況下呼叫安全的函式。 來自網路的資料會複製到256個位元組的緩衝區。 **Strncpy** 函式依賴在來源字串中尋找 Null 結束字元，或受限於提供的緩衝區計數。 問題在於緩衝區大小不正確。 如果網路中的資料未經過驗證或緩衝區大小錯誤 (如這個範例) 所示，攻擊者可以直接提供大型緩衝區來覆寫堆疊資料，在緩衝區結束之後，將任何資料包含在網路封包中。 這可讓攻擊者藉由覆寫指令指標並變更傳回位址，來執行任意程式碼。 此範例最基本的課程是在驗證之前永遠不信任輸入。

即使資料一開始並不是來自網路，仍會有潛在的風險。 新式遊戲開發需要許多人設計、開發和測試相同的程式碼基底。 我們無法知道未來將如何呼叫函式。 永遠詢問您自己的資料來源，以及攻擊者的控制權為何？ 雖然以網路為基礎的攻擊是最常見的，但它們並不是建立安全性漏洞的唯一方法。 攻擊者可以建立 mod，還是以開啟安全性漏洞的方式編輯已儲存的檔案？ 使用者提供的圖像和音效檔呢？ 這些檔案的惡意版本可能會在網際網路上張貼，並為您的客戶建立危險的安全性風險。

請注意，請使用 >strsafe.h 或 Safe CRT （而不是 **strncpy** ）來修正範例。 Safe CRT 是 C 執行時間的完整安全性檢修，隨附于 Visual Studio 2005 的一部分。 如需安全 CRT 的詳細資訊，請參閱 Michael Howard 在 [CRT 中的安全性增強功能](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) 。

## <a name="ways-to-improve-security"></a>改善安全性的方法

有數種方式可改善開發週期的安全性。 以下是一些最佳方式：

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>閱讀安全性資訊
</dt> <dd>

《 Michael Howard 和 David LeBlanc 》這本書 *撰寫安全的程式碼、第二版* ，可提供防止攻擊和緩和入侵的策略和方法的深入說明。 從設計安全性的方法到版本，到保護網路應用程式的技術，本書都涵蓋了遊戲開發人員所需的所有層面，以協助保護自己、其產品和客戶免受攻擊者的攻擊。 本書可以用來在開發 studio 中投注信任感安全性文化特性。 別把程式碼安全性視為開發人員的問題或測試人員的問題。 將安全性視為整個團隊的資訊，從程式經理到設計人員到開發人員，都應該考慮它們在專案上的運作方式。 在審核流程中，越眼睛越好，在發行之前攔截安全性漏洞的機率就愈大。

*撰寫安全的程式碼，第二版* 可在 [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) 找到，在未來的攻擊中可以找到更多的一般安全性資訊，方法是藉由 Michael Howard [減少受攻擊面](/previous-versions/ms972812(v=msdn.10)) 。

Michael Howard、David LeBlanc 和 John Viega 撰寫了另一本書，討論所有常見的作業系統和程式設計語言，其涵蓋 *了 19 Deadly sins of 的軟體安全性*。

您可以在 Microsoft 產品的 [開發人員簡報](/previous-versions/dn629515(v=msdn.10)) 下載頁面找到著重于遊戲的安全性簡報。

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>威脅模型分析
</dt> <dd>

威脅分析模型分析是評估系統安全性的好方法，而不是以特定語言或使用工具來評估，但在少數的端對端方法中，可以在幾個會議中完成。 當適當地執行時，執行緒模型可以找出系統的所有優點和缺點，而不會在專案中加入重要的工作負載或會議時間。 威脅分析模型的方法也強調了在開發過程中評估系統安全性的概念，以協助確保在將焦點放在最具風險的功能時進行全面的評估。 您可以將它視為安全性分析工具。 藉由不是以特定語言為基礎或依賴特定工具，威脅分析模型可用於任何在任何類型的專案上運作的開發 studio。 威脅分析模型也是一種很好的方法，可以強化安全性是每個人的責任，而不是其他人的問題。

當威脅模型化時，請特別注意：

-   UDP 資料來源
-   不需要驗證的資料來源
-   經常且通常會在大規模資訊收集過程中探查的資料來源
-   用戶端將資料直接傳送給其他用戶端的任何能力

這些都是可能有安全性弱點的領域。

有關威脅分析模型的詳細資訊，可以在 MSDN 安全性開發中心的 [威脅分析模型](https://technet.microsoft.com/security/) 中找到，也可以在「Frank Swiderski 和「視窗 Snyder」這本書的 [威脅模型](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) 中找到。

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>資料執行防止 (/NX) 
</dt> <dd>

減少多重入侵的最新工具是資料執行防止 (DEP) 。 如果您在 build 命令中包含 switch **/NX** ，Visual Studio 會以旗標標示記憶體頁面，指出程式碼是否有權執行。 任何嘗試在未標示 EXECUTE 許可權的記憶體頁面中執行的程式，將會導致程式終止 forcible。 系統會對處理器層級強制執行預防措施，而且會影響使用自我修改程式碼或原生 JIT 語言編譯器的開發人員。 目前，只有 AMD 的 Athlon64 和皓龍處理器和 Intel 的 Itanium 和最新 Pentium 4 處理器支援執行預防，但預期所有的32位和64位處理器都支援未來的執行防止。  (開發人員所使用的禁止複製配置可能會受到執行防止的影響，但 Microsoft 已與禁止複製廠商合作，將影響降至最低。 ) 使用 DEP 是不錯的作法。

如需 DEP 的詳細資訊，請參閱 [資料執行防止](../memory/data-execution-prevention.md)。

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>緩衝區安全性檢查 (/GS) 和映射具有安全的例外狀況處理常式 (/SAFESEH) 
</dt> <dd>

*緩衝區安全性檢查*（由編譯器旗標 **/gs** 指定）和 *影像具有安全的例外狀況處理常式*，由連結器旗標 **/SAFESEH** 指定 (第一次在 Visual Studio .NET 2003) 中執行，可讓開發人員更輕鬆地保護程式碼的安全。

使用 **/gs** 旗標會讓編譯器針對某些形式的堆疊型緩衝區溢位來檢查檢查，以覆寫函式的傳回位址。 使用 **/gs** 將不會偵測到每個可能的緩衝區溢位，也不應該視為全部攔截，而是良好的深度防禦技術。

使用 **/SAFESEH** 旗標會指示連結器只產生可執行檔或 dll （如果它也可以產生可執行檔或 dll 的安全例外狀況處理常式資料表）。  () SafeSEH 的安全結構化例外狀況處理，藉由確保在分派例外狀況之前，會將例外狀況處理常式註冊到位於影像檔案的函式資料表中，以避免例外狀況處理作為緩衝區溢位攻擊的目標。 這些保護優點可透過 Windows XP SP2、Windows Server 2003、Windows Vista 和 Windows 7 啟用。 此外，若要讓 **/SAFESEH** 正常運作，則必須將它用於「全部」或「無」的方法。 所有包含系結至可執行檔或 DLL 之程式碼的程式庫都必須使用 **/SAFESEH** 進行編譯，否則就不會產生資料表。

有關 [緩衝區安全性檢查](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) (**/Gs**) 和 [映射有安全例外狀況處理常式](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) 的詳細資訊 (**/SAFESEH**) 可在 MSDN 中找到。

另請參閱 Microsoft Visual Studio 2012 [ **/SDL** 旗](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019)標的相關資訊，以及對 [ **/gs** 旗](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/)標 Visual Studio 2012 的增強功能。

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

PREfast 是 Microsoft 提供的免費工具，可分析編譯 C 或 c + + 中的執行路徑，以協助找出執行時間的 bug。 PREfast 的運作方式是在所有函式中處理所有執行路徑，並評估每個路徑的問題。 這項工具最初用來開發驅動程式和其他核心程式代碼，可協助遊戲開發人員消除一些難以尋找或編譯器會忽略的 bug，藉此節省時間。 使用 PREfast 是降低工作負載的絕佳方法，並專注于開發小組和測試團隊的工作。 PREfast 可在 Visual Studio Team Suite 中取得，並 Visual Studio Team Edition for Software Developers 為程式碼分析，由編譯器參數 **/analyze** 啟用。  (此選項也適用于隨附于 Windows 軟體開發套件的免費編譯器版本。 ) 

> [!Note]  
> Visual Studio 2012 支援所有版本中的 **/analyze** 。 如需所有 Visual Studio 版本中程式碼分析可用性的詳細資訊，請參閱程式 [代碼分析的新功能](/archive/blogs/codeanalysis/?m=20123)。

 

透過使用標頭注釋 (特別是) 的緩衝區指標引數，PREfast 可能會公開其他問題，例如記憶體覆寫錯誤、損毀的常見來源，以及潛在的安全性弱點。 這是使用標準注釋語言 (SAL) 來完成，這是 C/c + + 函式原型的標記形式，可提供預期指標引數語義的詳細資訊，以及與長度參數、宣告的緩衝區大小等相關的詳細資訊。所有適用于 Windows 作業系統的標頭都會加上批註，並在您自己的程式庫的公用 API 標頭中新增 SAL 標記，讓 PREfast 能夠在您的用戶端程式代碼中針對這類 Api 執行更詳細且更積極的檢查。 For an introduction to SAL and links to more information, see Michael Howard's blog entry, "[A Brief Introduction to the Standard Annotation Language (SAL)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)."

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>Windows 應用程式驗證器
</dt> <dd>

Windows 應用程式驗證器（或 AppVerifier）可以在一個工具中提供多個功能，以協助測試人員。 AppVerifier 是為了讓常見的程式設計錯誤更容易測試而開發的工具。 AppVerifier 可以檢查傳遞給 API 呼叫的參數、插入錯誤的輸入以檢查錯誤處理能力，以及記錄對登錄和檔案系統的變更。 AppVerifier 也可以偵測堆積中的緩衝區溢位，檢查是否已正確定義 ACL)  (的存取控制清單，並強制執行通訊端 Api 的安全使用。 雖然並非詳盡，但 AppVerifier 可以是測試人員工具箱中的一項工具，以協助開發 studio 發行品質的產品。

如需應用程式驗證器的詳細資訊，請參閱 MSDN 上的 [應用程式驗證器](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) 和 [使用軟體發展生命週期中的應用程式驗證器](/previous-versions/aa480483(v=msdn.10)) 。

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>模糊測試
</dt> <dd>

*模糊測試* 是一種半自動化的測試方法，可以增強目前的測試方法。 模糊測試背後的核心概念，是藉由輸入亂數據來查看有哪些中斷，來全面評估所有輸入;這包括所有網路資料、mods > 和已儲存的遊戲等等。模糊測試相當簡單。 只要插入隨機位元組、翻轉連續的位元組或否定數值，就可以改變格式正確的檔案或網路資料。 0xff、0xffff、0xffffffff、0x00、0x0000、0x00000000 和0x80000000 是可在模糊測試時公開安全性漏洞的值。 您可以使用 AppVerifier 觀察產生的互動組合。 雖然模糊化並非詳盡的，但很容易就能實現和自動化，而且可以攔截出更難以捉摸和無法預測的錯誤。

如需模糊測試的詳細資訊，請參閱 *遊戲安全性中* 的 [Gamefest 2007](/previous-versions/dn629515(v=msdn.10))展示實用步驟。

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Authenticode 簽署
</dt> <dd>

Authenticode 是一種方法，可確保使用者收到的可執行檔、DLL 檔和 Windows installer 封裝 ( .msi 檔案) ，而不會改變開發人員所發行的內容。 藉由使用密碼編譯原則、受信任實體和產業標準的組合，Authenticode 可驗證可執行內容的完整性。 Microsoft 提供密碼編譯 API CryptoAPI，可用來自動偵測已簽署程式碼的篡改。 如果在發行之後發生安全性漏洞，就可以撤銷憑證，並使用該憑證簽署的所有程式碼都會停止驗證。 撤銷憑證將會撤銷所有以該憑證簽署之標題的驗證。 Windows 的設計目的是要使用 Authenticode 簽章，並在特定情況下警示使用者未簽署的程式碼，這可能會使使用者的電腦遭受攻擊。

Authenticode 不應被視為消除安全性問題的方法，而是在發行可執行檔之後偵測到的方法。 可執行檔或 DLL （包含可利用的安全性問題）可以使用 Authenticode 進行簽署和驗證，但仍然會對新系統造成安全性問題。 只有在產品或更新已驗證為安全之後，才應該簽署程式碼，以確保使用者具有未遭篡改的版本。

即使開發人員認為沒有修改其發行的威脅，其他技術和服務也會依賴 Authenticode。 程式碼簽署很容易整合和自動化;開發人員沒有任何理由會簽署其發行。

如需 Authenticode 簽署的詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](./authenticode-signing-for-game-developers.md)。

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>最小化許可權
</dt> <dd>

一般程式應以操作所需的最低許可權集合來執行。 在 Windows Vista 和 Windows 7 上，您可以使用 [ [使用者帳戶控制](./user-account-control-for-game-developers.md)] 來完成這項作業，讓遊戲以標準使用者而非系統管理員的身分執行。 針對 Windows XP，遊戲通常一律以系統管理員身分執行。 即使是在 Windows Vista 和 Windows 7 上，有時也需要提高某些特定作業的完整系統管理員許可權。

在以完整系統管理許可權執行進程的情況下，通常只需要標準使用者以外的一些許可權。 系統管理存取權包括合法程式碼不需要的許多許可權，但攻擊者可能會利用程式中的一些弱點。 這類許可權的範例包括 SE \_ 取得 \_ 擁有權、se \_ DEBUG、se \_ 建立 \_ 權杖、se \_ ASSIGNPRIMARYTOKEN、SE \_ TCB、se \_ 安全性、SE \_ LOAD \_ 驅動程式、se \_ SYSTEMTIME、se \_ 備份、se \_ 還原、se \_ 關機和 se \_ AUDIT (查看許可權 [常數](../secauthz/privilege-constants.md)) 。

雖然處理常式在啟動之後無法獲得更多許可權，但它可以輕鬆地授與許可權。 在啟動時，進程可以立即使用 Win32 Api 來移除不需要的許可權。

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>利用 Windows 安全性功能
</dt> <dd>

Windows Vista 和 Windows 7 包含許多可改善程式碼安全性的新功能。 「[使用者帳戶控制](./user-account-control-for-game-developers.md)」當然是最重要的一項，也是最重要的功能，但還有其他功能。 除了 windows XP SP2 的技術（例如 Windows 防火牆、資料執行防止、緩衝區安全性檢查，以及安全的例外狀況處理常式，在 Windows Vista 和 Windows 7 上也有提供），還有三個要考慮的新安全性功能：

-   加入宣告位址空間配置隨機功能。 這是藉由連結 Visual Studio 2005 Service Pack 1 或 Visual Studio 2008 上的選項 **/DYNAMICBASE** 來啟用。 如此一來，系統就會在您的進程空間中隨機化許多重要系統 Dll 的位置，使其更難以撰寫可在網際網路上廣泛傳播的可攻擊攻擊程式。 Windows XP 和舊版的 Windows 會忽略此連結器旗標。
-   堆積損毀可能會導致整個類別的安全性漏洞，因此 Windows Vista 和 Windows 7 的記憶體系統現在支援在偵測到堆積損毀時終止進程的模式。 使用 **HeapEnableTermianteOnCorruption** 呼叫 [**HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation)時，將會加入宣告此行為。 在 Windows XP 和舊版的 Windows 上，此呼叫會失敗。
-   撰寫服務時，可以使用新功能來設定這些服務，以指定實際需要的許可權，以及限制特定 SID 的資源存取權。 這是透過 [ChangeSeviceConfig2](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a)，使用服務設定 \_ \_ 所需的 \_ 許可權 \_ 資訊和服務設定 \_ \_ 服務 \_ SID \_ 資訊來完成。

</dd> </dl>

## <a name="summary"></a>總結

為目前和未來的 marketplace 開發遊戲相當昂貴且耗時。 釋出含有安全性問題的遊戲，最終會產生更多的金錢和時間來妥善修正。 因此，所有遊戲開發人員都有興趣整合工具和技術，以在發行之前減輕安全性攻擊。

這篇文章中的資訊只是開發 studio 為了協助自己和客戶而能做的簡介。 如需一般安全性作法和安全性資訊的詳細資訊，請參閱 [Microsoft 安全性開發人員中心](https://technet.microsoft.com/security/)。

 

 