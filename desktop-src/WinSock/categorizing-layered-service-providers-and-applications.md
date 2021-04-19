---
title: 將多層式服務提供者和應用程式分類
description: Winsock 2 容納多層通訊協定。
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a966d54da0be26f75a074de18abe1b9e080c0c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000071"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>將多層式服務提供者和應用程式分類

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

Winsock 2 容納多層通訊協定。 分層式通訊協定是一種只會執行較高層級通訊函式的通訊協定，同時依賴于與遠端端點實際交換資料的基礎傳輸堆疊。 多層式通訊協定或多層式服務提供者的範例是安全性層級，會將通訊協定新增至連線建立程式，以執行驗證並建立相互同意的加密配置。 這種安全性通訊協定通常需要基礎可靠傳輸通訊協定（例如 TCP 或 SPX）的服務。 基底提供者所執行的「基底」（base protocol）一詞是指可執行 TCP 或 SPX 等通訊協定的 Winsock 提供者，其能夠執行與遠端端點的資料通訊。 「多層式通訊協定」一詞是用來描述無法獨立的通訊協定。 這些多層式通訊協定會以 Winsock 多層式服務提供者的形式安裝 (Lsp) 。

LSP 的範例是安裝在 Internet Secutity 和 Authentication Server 中的 Microsoft 防火牆用戶端服務提供者 (ISA) 用戶端。 Microsoft 防火牆用戶端服務提供者會透過 TCP 和 UDP 的 Winsock 基底提供者安裝。 ISA 防火牆用戶端軟體中的動態連結程式庫 (DLL) 變成 Winsock 分層服務提供者，所有 Winsock 應用程式都會以透明的方式使用。 如此一來，ISA 防火牆用戶端 LSP 可以攔截來自用戶端應用程式的 Winsock 函式呼叫，然後將要求路由傳送至原始基礎服務提供者（如果目的地為本機或 ISA Server 電腦上的防火牆服務）（如果目的地為遠端）。 類似的 LSP 會安裝為 Microsoft Forefront Firewall Service 的一部分，而威脅管理閘道 (TMG) 用戶端上的用戶端。

在 LSP 初始化期間，LSP 必須提供指向多個 Winsock 服務提供者介面的指標， (SPI) 函數。 這些函式會在 (其他 LSP 或 Ws232.DLL) 的正常處理期間由 LSP 直接進行呼叫 \_ 。

您可以根據 LSP 所實行的 SPI 函式子集，以及針對每個函式執行的額外處理的本質，來定義 LSP 類別。 藉由將 Lsp 分類，以及分類使用 Winsock 通訊端的應用程式，您可以選擇性地判斷在執行時間是否應該在指定的進程中包含 LSP。

在 Windows Vista 和更新版本上，會提供新的方法，以分類 Winsock 多層式服務提供者和應用程式，因此只會載入特定的 Lsp。 新增這些功能有幾個原因。

其中一個主要原因是某些系統重要的處理常式（例如 winlogon 和 lsass）會建立通訊端，但這些程式並不會使用這些通訊端來傳送網路上的任何流量。 因此大部分的 Lsp 都不應該載入到這些進程中。 許多案例也記載在錯誤 Lsp 可能導致 *lsass.exe* 損毀的情況。 如果 lsass 當機，系統會強制關機。 這些系統進程載入 Lsp 的副作用是，這些程式永遠不會結束，因此當 LSP 已安裝或移除時，需要重新開機。

次要原因是應用程式在某些情況下可能不會想要載入某些 Lsp。 例如，有些應用程式可能不會想要載入密碼編譯 Lsp，以防止應用程式與未安裝 cyptographic LSP 的其他系統進行通訊。

最後，其他 Lsp 可以使用 LSP 類別來判斷 Winsock 通訊協定鏈中應自行安裝的位置。 多年來，不同的 LSP 開發人員都想知道 LSP 的表現方式。 例如，檢查資料流程的 LSP 可能會想要在加密資料的 LSP 上方。 當然，這種 LSP 類別的方法並不是欺騙證明，因為它依賴協力廠商 Lsp 來適當地分類。

Windows Vista 和更新版本中的 LSP 分類和其他安全性增強功能是設計來協助防止使用者不慎安裝惡意 Lsp。

## <a name="lsp-categories"></a>LSP 類別

在 Windows Vista 和更新版本上，LSP 可根據其與 Windows 通訊端呼叫和資料互動的方式進行分類。 LSP 類別是 Winsock SPI 函式子集上可辨識的行為群組。 例如，HTTP 內容篩選器會分類為 (LSP 偵測器類別) 的資料偵測器 \_ 。 LSP 偵測 \_ 器類別會檢查 (，但不會將) 參數變更為資料傳輸 SPI 函數。 應用程式可以查詢 LSP 的類別，並選擇不要根據 LSP 類別和應用程式所允許的 LSP 類別組合來載入 LSP。

下表列出 LSP 可分類的類別。

| LSP 類別              | Description                                                     |
|---------------------------|-----------------------------------------------------------------|
| **LSP \_ 加密 \_ 壓縮** | LSP 是密碼編譯或資料壓縮提供者。         |
| **LSP \_ 防火牆**         | LSP 是防火牆提供者。                                 |
| **LSP \_ 本機快取 \_**     | LSP 是本機快取提供者。                              |
| **LSP \_ 輸入 \_ 修改**  | LSP 會修改輸入資料。                                  |
| **LSP 偵測 \_ 器**        | LSP 會檢查或篩選資料。                               |
| **LSP \_ 輸出 \_ 修改** | LSP 修改了輸出資料。                                 |
| **LSP \_ PROXY**            | LSP 可作為 proxy 並重新導向封包。                  |
| **LSP \_ 重新導向程式**       | LSP 是網路重新導向程式。                                |
| **LSP \_ 系統**           | LSP 可接受用於服務和系統進程。 |



 

LSP 可能屬於一個以上的類別。 例如，防火牆/安全性 LSP 可能屬於偵測器 (**lsp 偵測 \_ 器**) 和防火牆 (**lsp \_ 防火牆**) 類別。

如果 LSP 沒有設定類別，則會被視為在所有其他類別中。 此 LSP 類別目錄將不會載入至服務或系統進程 (例如，lsass、winlogon 以及許多 svchost 進程) 。

## <a name="categorizing-lsps"></a>將 Lsp 分類

Windows Vista 和更新版本提供數個新功能來分類 LSP：

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

為了將 LSP 分類，會以 GUID 呼叫 [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) 或 [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) 函式，以識別 LSP 隱藏專案、為此 LSP 通訊協定專案設定的資訊類別，以及用來修改函式行為的一組旗標。

[**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)或 [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)函數類似于抓取 LSP 的資訊類別相關資料。

## <a name="categorizing-applications"></a>將應用程式分類

Windows Vista 和更新版本提供數個新的功能，可將應用程式分類：

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

為了將應用程式分類， [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) 函式會以可執行檔映射的載入路徑來呼叫，以識別應用程式、啟動應用程式時使用的命令列引數，以及此應用程式的所有實例允許的 LSP 類別。

[**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)函式類似于抓取多層式服務提供者 (LSP) 類別與應用程式相關聯。

## <a name="determining-which-lsps-get-loaded"></a>判斷要載入的 Lsp

LSP 分類的最後一個部分是決定哪些 Lsp 將會載入至哪些處理常式。 當進程載入 Winsock 時，會對應用程式類別和所有已安裝 Lsp 的 LSP 類別進行下列比較：

-   如果應用程式未分類，則允許將所有 Lsp 載入至進程。
-   如果應用程式和 LSP 都有指派類別，下列所有條件都必須為 true： <dl> 應用程式的指定類別中至少有一個 LSP 類別存在。  
    Lsp 類別中只會指定應用程式指定類別中指定的類別。 例如，如果應用程式指定類別目錄，它必須位於 LSP 的類別中。  
    如果 \_ 應用程式類別中出現 lsp 系統類別，則它必須存在於 lsp 的類別中。  
    </dl>

> [!Note]  
> 如果 LSP 未分類，其類別目錄實際上是零。 若要進行相符，所有 LSP 的指定類別都必須出現在應用程式類別中 (應用程式類別必須是 LSP 類別的超集合) 注意，如果 LSP \_ 系統存在於應用程式類別中，它也必須存在於 lsp 的類別中。

 

請考慮下列範例：

*Foo.exe* 的應用程式會分類為 lsp \_ 系統 + LSP \_ 防火牆 + lsp \_ 加密 \_ 壓縮。 應用程式 *Bar.exe* 會分類為 lsp \_ 防火牆 + lsp \_ 加密 \_ 壓縮。 系統上已安裝四個 Lsp：

-   LSP1 已設定 LSP 系統的類別 \_ 。
-   LSP2 不是分類集合，因此其類別目錄為零。
-   LSP3 已設定 LSP 防火牆的類別 \_ 。
-   LSP4 已設定 LSP \_ 系統 + lsp \_ 防火牆 + lsp \_ 加密 \_ 壓縮 + lsp 偵測 \_ 器的分類

在此範例中， *Foo.exe* 應用程式只會載入 LSP1，而 *Bar.exe* 應用程式會載入 LSP3。

## <a name="determining-winsock-providers-installed"></a>判斷已安裝 Winsock 提供者

Microsoft Windows 軟體開發套件 (SDK) 包含範例 Winsock 程式，可用來判斷本機電腦上安裝的 Winsock 傳輸提供者。 根據預設，此 Winsock 範例的原始程式碼會安裝在 Windows 7 Windows SDK 的下列目錄中：

*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ winsock \\ LSP*

此範例是安裝和測試多層式服務提供者的公用程式。 但是它也可以用來以程式設計的方式，從本機電腦上的 Winsock 類別目錄收集詳細資訊。 若要列出所有目前的 Winsock 提供者（包括基底提供者和層級服務提供者），請建立此 Winsock 範例，然後執行下列主控台命令：

**instlsp-p**

輸出將會是安裝在本機電腦上的 Winsock 提供者清單，包括分層服務提供者。 輸出會列出 Winsock 提供者的目錄識別碼和字串名稱

若要收集所有 Winsock 提供者的詳細資訊，請執行下列主控台命令：

**instlsp-p-v**

輸出將會是本機電腦上所支援的清單 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構。

如需本機電腦上已安裝的多層式服務提供者清單，請執行下列主控台命令：

**instlsp-l**

若要對應 LSP 結構，請執行下列主控台命令：

**instlsp-m**

> [!Note]  
> TDI 功能已被取代，並將在未來的 Microsoft Windows 版本中移除。 根據您使用 TDI 的方式，使用 Winsock Kernel (WSK) 或 Windows 篩選平台 (WFP) 。 如需有關 WFP 和 WSK 的詳細資訊，請參閱 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md) 和 [Winsock 核心](/windows-hardware/drivers/ddi/_netvista/)。 如需有關 WSK 和 TDI 的 Windows 核心網路功能 blog 專案，請參閱 [Winsock 核心 (WSK 簡介) ](/archive/blogs/wndp/)。

 

 

 
