---
title: 修補 Windows XP、Windows Vista 和 Windows 7 的遊戲軟體
description: 本文將探討一些修補方法，在 Windows Vista 和 Windows 7 以及 Windows XP 中都能正常運作。
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dae9b3bc91c96006f3b2117093962ee485db948fd983191f2db3c7f88fb33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042498"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>修補 Windows XP、Windows Vista 和 Windows 7 的遊戲軟體

WindowsVista 和 Windows 7 有許多功能可讓作業系統更安全。 新增安全性表示將修補程式套用到軟體並不像過去一樣簡單。 本文將探討一些修補方法，在 Windows Vista 和 Windows 7 以及 Windows XP 中都能正常運作。

有兩個主要的遊戲類別需要修補程式：

-   只需要偶爾修補程式的遊戲，例如大部分的離線遊戲。
-   需要經常修補的遊戲，例如大部分的線上遊戲。

本文也提供「使用者帳戶控制」 (UAC) 的簡介，以作為開發人員可預期使用者在 Windows Vista 和 Windows 7 中所擁有之許可權的背景。

-   [使用者帳戶控制](#user-account-control)
-   [只需要偶爾修補程式的遊戲](#games-that-require-only-occasional-patches)
    -   [方法1：針對偶爾的修補程式使用 Windows Installer](#method-1-use-windows-installer-for-occasional-patches)
    -   [方法2：需要系統管理員許可權才能套用修補程式](#method-2-require-administrator-rights-to-apply-patches)
-   [需要經常修補的遊戲](#games-that-require-frequent-patches)
    -   [方法3：安裝每位使用者](#method-3-install-per-user)
    -   [方法4：安裝到常見的 Per-Computer 位置](#method-4-install-to-a-common-per-computer-location)
    -   [其他可能性](#other-possibilities)
-   [總結](#summary)

## <a name="user-account-control"></a>使用者帳戶控制

WindowsVista 和 Windows 7 有兩種主要類型的使用者帳戶：標準使用者和系統管理員。 標準使用者帳戶有數個存取限制;例如，它無法將資料寫入% SystemDrive% 程式檔中的檔案系統 \\ 或 HKEY 本機電腦中的登錄 \_ \_ 。 如果將修補程式安裝在唯讀的位置，這會對套用修補程式造成影響。 不同于 Windows XP，標準使用者帳戶在 Windows Vista 和 Windows 7 中更為普遍。 作業系統的重要功能（例如家長監護）也需要標準使用者帳戶。 家長監護要求子帳戶必須是標準使用者，而將這類帳戶提升為系統管理員甚至是一項遊戲，以防止家長監護與其他所有遊戲合作。 因此，針對標準使用者設計遊戲相當重要。

WindowsVista 和 Windows 7 有較新的使用者權限模型，可協助防止使用者執行嘗試執行使用者不打算或授權之作業的程式。 為了達成此目的，使用者帳戶控制 (先前稱為最低許可權的使用者帳戶或 LUA) 可讓使用者在大部分的情況下，使用低層級的許可權來操作電腦，同時也能夠在必要時輕鬆地執行需要更高許可權的應用程式。 這表示標準使用者帳戶和系統管理員帳戶都是使用標準使用者權限來執行應用程式，但只有系統管理員帳戶能夠將更高的許可權授與應用程式。 作業系統會在以較高的許可權執行應用程式之前，要求具有系統管理員帳戶的使用者進行明確同意，如果需要系統管理員許可權的程式是在標準使用者帳戶上執行，系統會提示系統管理員核准。

## <a name="games-that-require-only-occasional-patches"></a>只需要偶爾修補程式的遊戲

有些遊戲在整個生命週期中只需要一些修補程式。 您可以針對此修補頻率採用的兩種方法，就是將修補程式散發為 Windows Installer 套件，這通常不需要系統管理員許可權，也不需要使用其他直接修改遊戲檔案的散發類型。

> [!Note]  
> 無論遊戲是否需要經常修補，應用程式通常都需要安裝或移除系統管理員許可權。

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>方法1：針對偶爾的修補程式使用 Windows Installer

在此方法中，會使用 Windows Installer 來安裝套件 (.msi 檔) 以及 Windows Installer 修補程式 ( .msp 檔) 發佈以安裝修補程式。 封裝必須有 MsiPatchCertificate 資料表，而修補程式必須由資料表中的憑證以數位方式簽署。 如需有關數位簽章的詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。

如需使用此修補方法的詳細資訊和需求，請參閱 Windows Installer 檔：

-   [修補和升級](/windows/desktop/Msi/patching-and-upgrades)
-   [ (UAC) 修補的使用者帳戶控制](/windows/desktop/Msi/user-account-control--uac--patching)

這種方法的缺點是，如果遊戲未從 Windows XP 上的卸載式媒體安裝，則修補需要系統管理員許可權。 不過，這不太可能太過嚴格，因為 Windows XP 上的大部分使用者系統管理員，以及從卸載式媒體安裝之軟體的限制並不存在於 Windows Vista 中。

這種方法的主要優點是可以由標準使用者帳戶套用修補程式，而不需要提示和驗證更高的許可權。 這可提供更好的使用者體驗，因為若要玩遊戲，具有標準使用者帳戶的使用者不需要要求具有系統管理員帳戶的使用者安裝修補程式，或提供具有永久系統管理員許可權的標準使用者帳戶。

這種方法可能適用于需要頻繁修補程式的遊戲，但使用 Windows Installer 套件的額外負荷（例如組建整合和支援大量檔案）可能會讓這個方法比其他方法更不理想。

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>方法2：需要系統管理員許可權才能套用修補程式

在這個方法中，套用修補程式的可執行檔需要系統管理員許可權才能執行。 使用系統管理員許可權，修補可執行檔可以直接修改位於% SystemDrive% Program Files 的遊戲檔案 \\ 。

這種方法的優點是它的簡化方式。 但是，如果遊戲需要經常修補程式，這個方法並不適合，因為如果使用者的標準使用者帳戶想要播放需要經常修補的遊戲，例如大量的多玩家線上遊戲，那麼該使用者就有兩個選擇：

-   讓系統管理員登入並修補遊戲，這對雙方來說可能不方便。
-   以系統管理員許可權永久提高其帳戶的許可權。

> [!Note]  
> 後者的解決方案不僅會削弱整體系統的安全性，還能防止重要功能（例如家長監護）運作。

 

在執行此方法時，套用修補程式的可執行檔必須與遊戲可執行檔不同。 修補可執行檔的資訊清單應指定 requireAdministrator for 並無 requestedexecutionlevel，以將它表示為需要系統管理員許可權的應用程式。 如需如何進行這項作業的詳細資訊，請參閱「應用程式資訊清單架構」中 [最低許可權環境中應用程式的開發人員最佳做法和指導方針](/previous-versions/dotnet/articles/aa480150(v=msdn.10))。

使用這個方法時，即使是資訊清單中的設定，在兩種情況下，可執行檔可能仍不會以系統管理員許可權啟動：

-   如果作業系統是 Windows XP，而且使用者的帳戶是受限制的使用者。
-   如果作業系統是 Windows Vista 或 Windows 7，則使用者的帳戶是標準使用者，且 UAC 已停用。

這兩個都是罕見的取用者案例。 不過，patcher 應該要有資訊清單需要系統管理員許可權，而且應該呼叫 [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin);如果此函數傳回 FALSE，則會顯示錯誤訊息「需要系統管理員許可權」。

整體來說，方法1適用于只需要一些修補程式存留期的遊戲。

## <a name="games-that-require-frequent-patches"></a>需要經常修補的遊戲

許多以網際網路為基礎的遊戲不斷改進，通常需要定期修補。 針對這些遊戲，可以依使用者或每部電腦套用修補程式，如下列主題所述。 其他可能的解決方案包括改變保護% SystemDrive% 程式檔案 \\ 或建立自訂服務的 ACL。

### <a name="method-3-install-per-user"></a>方法3：安裝 Per-User

其中一個建議和簡單的方法是將整個遊戲安裝至本機應用程式 data 資料夾的每個使用者子資料夾，您可以藉由呼叫 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with CSIDL \_ local APPDATA 找到這個資料夾 \_ 。 範例路徑為 C： \\ Documents 和設定 \\ 使用者名稱 \\ 本機設定 \\ Application Data \\ ExampleGame。 這類位置可讓使用標準使用者權限執行的應用程式直接修改遊戲檔案。

但是，當電腦有多個使用者時，這個方法會有一個缺點：每個使用者都安裝了一份遊戲，而且每個使用者都必須下載並套用修補程式。 這不僅浪費使用者的時間和磁碟空間，還會增加使用網路頻寬給提供修補程式的伺服器。 此外，因為任何具有標準使用者權限的應用程式都可以修改遊戲，所以遊戲可執行檔會受到較低的保護;由遊戲製造商決定是否可接受這項功能。

### <a name="method-4-install-to-a-common-per-computer-location"></a>方法4：安裝到常見的 Per-Computer 位置

另一種方法是將無法執行的遊戲資料安裝到 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL COMMON APPDATA 所指定路徑的 \_ 子目錄 \_ ; 範例路徑為 C： \\ Documents 和設定 \\ 所有使用者的 \\ 應用程式資料 \\ ExampleGame。 這是所有使用者的共用位置，可由以標準使用者權限執行的應用程式進行修改。 當遊戲從一個以上的帳戶播放時，此方法會將重新套用大型修補程式的需求降到最低。 遊戲的可執行檔應該保留在% SystemDrive% 的程式檔中， \\ 以將系統上其他帳戶的風險降至最低。 可執行檔應確認共用目錄中新內容的完整性，因為該位置可以由具有標準使用者權限的程式或人員修改;請考慮使用 [**MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) 來計算檔案的總和檢查碼。

這個方法的優點是，在 Windows XP 和 Windows Vista 上都能正常運作，而且不需要系統管理員許可權。

### <a name="other-possibilities"></a>其他可能性

在已經討論過的方法之外，另一個可能的原因是， \\ 在安裝遊戲時改變% SystemDrive% Program files 遊戲資料夾的 ACL， \\ \\ 讓修補工具可以直接寫入遊戲的檔案，即使以標準使用者權限執行也一樣。 雖然這並不困難，但它會略過系統提供給遊戲檔案的安全性保護，並讓惡意程式有機會改變目錄的內容。 這不是建議的作法，強烈建議您改為使用替代方法。

最後一個可能的原因是撰寫自訂服務。 一般情況下，撰寫自訂服務來修補遊戲並不是個好主意，因為這樣做會很複雜而且容易出錯。 建議您使用本文中討論的其他方法來進行修補。 不過，當自訂服務與反或反盜版解決方案結合時，可能是必要的。 這類服務應該支援大量的遊戲，並將其設計為只能下載修補檔，並只寫入目標遊戲的安裝目錄。 很重要的是，這項服務很重要，有一個很小的介面區很容易受到攻擊，而且當遊戲未執行時，盡可能地使用最少的系統資源。

## <a name="summary"></a>摘要

最後，您必須決定要執行的方法。 您必須權衡這些因素對您很重要。 安全性、修補頻率、客戶容易使用、執行所需的工作負載、解決方案的複雜度，以及平臺功能合規性，是每位開發人員在決定特定方法之前必須考慮的因素。

您可以在[Windows Vista 應用程式開發需求中找到使用者帳戶保護的詳細資訊， (UAC) 的使用者帳戶控制](/previous-versions/aa905330(v=msdn.10))。

 

 