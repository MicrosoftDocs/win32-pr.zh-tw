---
title: 製作更健全的 Windows 遊戲的最佳工具和技術
description: 本文說明可用來協助減少您收到的支援電話數目的工具和技術。
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76b49c228af6a932c453b11e92f612d3419a4af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463417"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>製作更健全的 Windows 遊戲的最佳工具和技術

在遊戲生產環境中，有一項較非期望的成本是支援電話。 每次使用者聯絡客戶支援時，就會降低遊戲的收益。 雖然不會 preventable 某些客戶支援的呼叫，但可以藉由採用良好的開發實務來消除或降低其他電話。 本文說明可用來協助減少您收到的支援電話數目的工具和技術。

此處所述的所有工具都是免費的，而且這些技巧很簡單，可以加入至大部分的開發方法。

工具和技術：

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Microsoft 應用程式相容性工具組](#microsoft-application-compatibility-toolkit)
-   [使用者帳戶保護測試](#user-account-protection-testing)
-   [適用于 Windows 的 PIX](#pix-for-windows)
-   [設定偵測](#configuration-detection)
-   [啟用完整編譯器警告](#enable-full-compiler-warnings)
-   [Microsoft 符號伺服器](#microsoft-symbol-server)
-   [Windows 錯誤報告](#windows-error-reporting)
-   [效能微調工具](#performance-tuning-tools)
-   [總結](#summary)

## <a name="prefast"></a>PREfast

PREfast for 驅動程式是 Microsoft 所提供的工具，可分析編譯 C 或 c + + 中的執行路徑，以協助找出執行時間的 bug。 PREfast 的運作方式是在所有函式中處理所有執行路徑，並評估每個路徑的問題。 雖然這項工具通常是用來開發驅動程式和其他核心程式代碼，但它可以協助遊戲開發人員藉由消除一些難以尋找或編譯器會忽略的 bug，來節省時間。 使用 PREfast 是減少發行後工作負載和支援成本的絕佳方法。

PREfast 隨附 Visual Studio 的 Team System 以及 [Windows 驅動程式套件](https://www.microsoft.com/whdc/devtools/WDK/)的一部分。 如需 PREfast 的詳細資訊，請參閱 [PREfast 的驅動程式](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx)。

## <a name="appverifier"></a>AppVerifier

Microsoft 應用程式驗證器（或 AppVerifier）是一種工具，可協助測試人員在一個工具中提供多個功能。 AppVerifier 是為了方便測試常見程式設計錯誤所開發。 AppVerifier 可以檢查 API 呼叫中傳遞的參數、插入錯誤的輸入以檢查錯誤處理能力，以及記錄對登錄和檔案系統的變更。 AppVerifier 也可以偵測堆積中的緩衝區溢位，檢查是否已正確定義 ACL)  (的存取控制清單，並強制執行通訊端 Api 的安全使用。

雖然並非詳盡，AppVerifier 可以是測試人員工具箱的一個元件，以協助開發 studio 發行品質的產品，並減少可能的發行後成本。

如需應用程式驗證器的詳細資訊，請參閱 MSDN 上的 [應用程式驗證器](/previous-versions/ms220948(v=vs.80)) 和 [使用軟體發展生命週期中的應用程式驗證器](/previous-versions/aa480483(v=msdn.10)) 。 您可以從 [下載詳細資料](https://www.microsoft.com/download/details.aspx?id=20028) 下載應用程式驗證器： Microsoft 下載中心上的應用程式驗證器。

驅動程式和驅動程式驗證器也有類似的工具。 如需詳細資訊，請參閱 [使用驅動程式驗證器找出 Windows 驅動程式的問題](https://support.microsoft.com/Default.aspx?kbid=244617) ，以取得 Microsoft 說明及支援的 Advanced Users。

## <a name="microsoft-application-compatibility-toolkit"></a>Microsoft 應用程式相容性工具組

Microsoft 應用程式相容性工具組是一組免費的工具，可協助開發人員快速查看其發行將如何在 Microsoft Windows 新發行的 service pack 上執行。 藉由準備新的 service pack，開發人員可以防止或針對任何問題做好準備。

應用程式相容性工具組和詳細資訊可在 [Windows 應用程式相容性](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx)中找到。

## <a name="user-account-protection-testing"></a>使用者帳戶保護測試

Windows Vista 和 Windows 7 有兩種主要類型的使用者帳戶：標準使用者和系統管理員。 標準使用者帳戶是所有使用者慣用的類型，因為它們可減少惡意應用程式對系統造成的損害風險。 由於標準使用者有存取限制，例如無法寫入 Program Files 資料夾或 HKEY \_ 本機 \_ 電腦 (HKLM) 在登錄中，因此必須設計和測試遊戲才能使用標準使用者帳戶。

如需有關本主題的詳細資訊，請參閱在 [WINDOWS XP、Windows Vista 和 windows 7 中修補遊戲軟體](./patching-methods-in-windows-xp-and-vista.md) 的文章，以及 [遊戲開發人員的使用者帳戶控制](./user-account-control-for-game-developers.md)。

## <a name="pix-for-windows"></a>適用于 Windows 的 PIX

PIX 是一種工具，用來收集和分析來自執行中應用程式的效能資訊。 PIX 可以收集統計資料，瞭解某些框架轉譯的速度會比其他框架更慢，而且可以識別不良的 API 使用方式。 PIX 也可以自動化以測試每日組建，以及旗標應用程式效能的突然變更。 藉由在各種不同的硬體設定中使用 PIX，測試人員和開發人員可協助將與遊戲效能相關的支援電話降至最低。

## <a name="configuration-detection"></a>設定偵測

驅動程式所公開的裝置功能不一定都是正確的。 其中一個解決方法是使用資料庫導向系統來設定應用程式，例如 ConfigSystem 範例中所示範的系統（隨附于 DirectX SDK）。 與範例中的系統類似的偵測模型可協助識別阻礙遊戲效能的裝置功能，因此可減少對效能的支援呼叫數目。

## <a name="enable-full-compiler-warnings"></a>啟用完整編譯器警告

在專案變得穩定之後，請將 **\# pragma 警告** 所停用的任何編譯器警告還原為最佳做法。 開發人員應該在發行產品之前，嘗試排除所有的警告。 即使警告不會導致開發人員系統發生損毀或錯誤，仍可能在使用者的系統上造成問題。 如果無法消除警告，測試小組必須確定警告是否會在使用者的系統上導致少數或沒有錯誤。

## <a name="microsoft-symbol-server"></a>Microsoft 符號伺服器

Microsoft 提供可存取網際網路的伺服器，以提供 Microsoft Windows 作業系統的符號檔，以及其他 Microsoft 產品。 您也可以從伺服器取得符號，以用於目前的 Beta 和 Windows 產品的發行候選版本，以及熱修正程式和 service pack。 您可以設定偵錯工具在偵錯工具期間視需要下載符號，而不是在偵錯工具會話之前個別下載符號檔。 符號會下載至您指定的目錄位置，而偵錯工具會從該處載入這些符號。

如需 Microsoft 符號伺服器的詳細資訊，請參閱 [偵錯工具和符號：開始使用](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx)。

## <a name="windows-error-reporting"></a>Windows 錯誤報告

Windows 錯誤報告 (WER) 是 Microsoft 所提供的一項服務，可協助開發人員以一致且井然有序的方式，從應用程式收集錯誤資訊。 雖然這完全是自願的，但開發人員應該利用這項服務來協助判斷最常發生哪些錯誤。 使用 WER 有助於偵測常見的回報問題，這有助於消除最 commons 錯誤的支援呼叫。

如需 WER 的詳細資訊，請參閱損毀傾印 [分析](./crash-dump-analysis.md)。

## <a name="performance-tuning-tools"></a>效能微調工具

開發人員可以使用效能分析器來調整其遊戲的效能。 除了 PIX，還有一些適用于 Windows 的熱門效能分析器，例如 [Intel VTune 效能分析器](https://software.intel.com/intel-vtune/) 和 [AMD CodeAnalyst 效能分析器](https://developer.amd.com/cpu/CodeAnalyst/)。 這些工具有助於找出瓶頸，並決定如何改善應用程式的整體效能。 改善發行前的效能瓶頸，將有助於降低發行後的成本。

## <a name="summary"></a>總結

所有牽涉到設計、開發和測試的人都必須考慮其工作將如何影響產品的發行後成本。 藉由在生產過程中使用上述的工具和方法，可減少支援電話數量。 如此一來，就能降低遊戲開發的發行後成本來提高利潤。

 

 