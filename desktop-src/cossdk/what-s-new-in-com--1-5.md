---
description: COM + 1.5 版新增了新功能，其設計目的是為了提升開發人員和系統管理員的 COM + 應用程式的整體擴充性、可用性和管理性。
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: COM + 1.5 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0fd6705775e84f49d3a60afd7d89b7a5412b4a87fd5d04f202fadc77fd850d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304879"
---
# <a name="whats-new-in-com-15"></a>COM + 1.5 的新功能

COM + 1.5 版新增了新功能，其設計目的是為了提升開發人員和系統管理員的 COM + 應用程式的整體擴充性、可用性和管理性。

從 Windows XP 和 Windows Server 2003 開始，可以使用 com + 1.5。 Windows 2000 中無法使用新的 com + 1.5 功能。

## <a name="application-level-access-checks-enabled-by-default"></a>預設啟用 Application-Level 存取檢查

作為系統的增強安全性的一部分，建立 COM + 應用程式時，預設會啟用存取檢查。 在先前的版本中，預設會在應用層級停用存取檢查，並且預設會在元件層級啟用。 從 Windows Server 2003 開始，依預設會在應用層級啟用存取檢查，並且在元件層級預設為停用。 如需有關如何變更預設設定的詳細資訊和程式，請參閱 [建立新的 COM + 應用程式](creating-a-new-com--application.md)、 [啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md)，以及在 [元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md) 。

## <a name="application-pooling"></a>應用程式集區

使用 [**應用程式**](applications.md)集合中 [**COMAdminCatalogObject**](comadmincatalogobject.md)物件的新 ConcurrentApps 屬性，com + 應用程式共用會為單一執行緒進程新增擴充性，並與新的 Com + 應用程式回收服務整合。 如需詳細資訊，請參閱 [Com + 應用程式](com--application-pooling.md) 集區。

## <a name="application-recycling"></a>應用程式回收

應用程式回收可大幅提升應用程式的整體穩定性。 因為大部分應用程式的效能可能會因為像是記憶體流失、依賴協力廠商程式碼，以及 nonscalable 資源使用情形等因素而降低，所以 COM + 應用程式回收提供簡單的解決方案，可正常關閉與應用程式相關聯的進程並重新啟動。 如需詳細資訊，請參閱 [Com + 應用程式回收](com--application-recycling.md) 。 另請參閱「元件服務管理說明」中的「設定進程回收」，以取得設定進程回收的逐步程式。

## <a name="com-partitions"></a>COM + 磁碟分割

在此版本中，COM + 引進了 COM + 分割的支援，這項功能可讓您在同一部電腦上安裝及設定多個版本的 COM + 應用程式。 這項功能可以節省使用多部伺服器來管理不同應用程式版本的成本和耗時的工作。 在單一電腦上，每個磁碟分割實際上都會作為虛擬伺服器。 將應用程式安裝到每個資料分割之後，您可以建立將使用者對應至邏輯伺服器的資料分割集。 如需如何設定和管理 COM + 分割的詳細資訊，請參閱 [Com +](com--partitions.md) 分割。 另請參閱「元件服務管理說明」中的「管理應用程式磁碟分割」，以取得逐步程式。

## <a name="com-services-without-components"></a>沒有元件的 COM + 服務

使用 COM + 1.5，您可以使用 COM + 所提供的服務，而不需要建立元件來包含呼叫這些服務的方法。 這可大幅獲益于通常不使用元件，但想要使用 COM + 服務（例如交易或 COM + 追蹤器）的開發人員。 藉由使用沒有元件的 COM + 服務，開發人員可以避免建立元件的額外負荷，而此元件只會用來存取所需的 COM + 服務。 如需詳細資訊，請參閱 [沒有元件的 Com + 服務](com--services-without-components.md) 。

## <a name="com-soap-service"></a>COM + SOAP 服務

使用 COM + 1.5，您現在可以將 COM + 應用程式公開為 XML web service。 您也可以使用 COM 元件，以透明的方式使用 XML web service （不論是否使用 COM + 部署）。 這表示您可以輕鬆地從現有的 COM + 應用程式建立新的 XML web service，並輕鬆地將 XML web service 併入新的 COM + 應用程式。 如需詳細資訊，請參閱 [Com + SOAP 服務](com--soap-service.md) 。

## <a name="configurable-isolation-levels"></a>可設定的隔離等級

COM + 開發人員可以使用新的 TxIsolationLevel 內容或 [元件服務] 系統管理工具，根據需求來設定應用程式的隔離等級，以協助增加平行存取、效能和擴充性。 這種彈性可讓具有適當專長的人員，從其應用程式取得每個最後的輸送量。 如需詳細資訊，請參閱設定 [交易隔離等級](configuring-transaction-isolation-levels.md) 。

## <a name="creating-private-components"></a>建立私用元件

如果您在應用程式中有數個協助程式元件，而該應用程式只能從該應用程式內的其他元件呼叫，這一版的 COM + 可讓您使用新的屬性 IsPrivateComponent，將這些元件標示為私用。  (在先前的 COM + 版本中，所有元件都必須是公用的，才能存取 COM + 服務，這表示可以從其他應用程式啟動這些元件。 ) 私用元件只能由相同應用程式中的其他元件來查看和啟動，讓您更充分掌控要公開的功能。 您只需要記錄和維護公用元件，同時使用無法從應用程式外部存取的私用元件，但仍可利用所有 COM + 服務。

## <a name="dtc-security-settings"></a>DTC 安全性設定

已針對 Microsoft Distributed Transaction Coordinator (DTC) 新增了數個新的安全性設定，可讓您自訂管理分散式交易的安全性層級。 請參閱有關這些設定的 DTC 安全性考慮，以及如何執行這些設定。

為了協助進行相互驗證，DTC 會限制為在 NetworkService 帳戶下執行。 如需詳細資訊，請參閱管理帳戶和許可權。

若要使用 XA 資料庫進行復原，建議您提供執行此復原所需的許可權和角色給 NetworkService 帳戶。 執行這項操作的確切方法是每個資料庫特有的方法。 如需詳細資訊，請參閱停用原生分散式交易和停用秘訣和 XA 交易。

為了在使用 xa 交易時提供更安全的系統，Windows Server 2003 平臺包含新的登錄專案，用來指定 xa DLL 檔案。 升級至 Windows Server 2003 時，您可以像之前一樣使用 XA 交易，方法是在 [ **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ MSDTC \\ XADLL**] 底下建立登錄專案，其中值名稱是 dll 的名稱 (格式為 *dllname*.dll) ，而值則是 dll 檔案的完整路徑。 您必須為每個使用中的 XA DLL 檔案建立一個專案。 如果執行 DTC 的電腦是叢集的一部分，則必須為叢集中的每個節點建立登錄專案。 如需詳細資訊，請參閱管理 XA 交易。

## <a name="low-memory-activation-gates"></a>Low-Memory 啟用閘道

在此版本中，COM + 會在建立 COM + 伺服器或物件之前自動檢查記憶體。 如果應用程式可用的虛擬記憶體百分比低於固定閾值，則在建立物件之前啟用會失敗。 藉由容錯移轉通常會執行的啟用， [Com + Low-Memory](com--low-memory-activation-gates.md) 啟動閘道服務可大幅提高系統可靠性。

## <a name="moving-and-copying-com-components"></a>移動和複製 COM 元件

在此版本中，COM + 允許您移動和複製您的元件。 這表示您可以設定元件的單一實體實作為許多不同的時間。 您可以在二進位層級（而不是在原始程式碼層級）上重複使用元件，這會產生較少的程式碼、降低開發成本，並加快上市時間。 如需詳細資訊，請參閱 [移動元件](moving-components.md) 和 [複製元件](copying-components.md) 。

## <a name="network-access"></a>網路存取

預設會停用 Windows Server 2003 上的 com + 網路存取，這表示 com + 預設只能在本機使用。 使用下列程式可啟用網路 COM + 存取。

**啟用網路 COM + 存取**

1.  在 [ **開始** ] 功能表上，指向 [ **主控台**]，然後選取 [ **新增或移除程式**]。

2.  按一下 [**新增/移除 Windows 元件**]。

3.  選取 **[應用程式伺服器]** 並按一下 **[詳細資料]**。

4.  核取 [ **啟用網路 COM + 存取**] 旁的核取方塊，然後按一下 **[確定]**。

5.  按 **[下一步**] 完成 [Windows 元件] wizard。

6.  按一下 **[完成** ] 以關閉嚮導。

預設會停用 Windows Server 2003 上的 DTC 網路交易存取。 在這些平臺上，DTC 預設只能執行本機交易。 使用下列程式來啟用網路 DTC 存取。

> [!NOTE]
> 您也可以使用 [元件服務] 系統管理工具，或透過 COM + 系統管理程式庫以程式設計方式啟用網路 DTC 存取。 如需相關的程式資訊，請參閱元件服務管理說明中的「設定 DTC 安全性」。

**啟用網路 DTC 存取**

1.  在 [ **開始** ] 功能表上，指向 [ **主控台**]，然後選取 [ **新增或移除程式**]。

2.  按一下 [**新增/移除 Windows 元件**]。

3.  選取 **[應用程式伺服器]** 並按一下 **[詳細資料]**。

4.  核取 [ **啟用網路 DTC 存取**] 旁的核取方塊，然後按一下 **[確定]**。

5.  按 **[下一步**] 完成 [Windows 元件] wizard。

6.  按一下 **[完成** ] 以關閉嚮導。

## <a name="pausing-and-disabling-applications"></a>暫停和停用應用程式

COM + 應用程式現在更容易管理。 系統管理員可以暫停和繼續 COM + 伺服器應用程式，或是停用和啟用 COM + 程式庫或伺服器應用程式，甚至是個別設定的元件。 暫停和停用功能會防止未來的啟用，而不會影響現有的元件實例。 如需詳細資訊，請參閱元件服務管理說明中的「管理 COM + 應用程式」。

## <a name="process-dumping"></a>進程傾印

在生產環境中對應用程式進行疑難排解並不容易。 您如何收集問題的相關資訊，而不會干擾執行中的進程？ COM + 現在透過其新的進程傾印功能提供解決方案。 這項功能可讓系統管理員在不終止進程的情況下，傾印整個進程的狀態。 如需詳細資訊，請參閱元件服務管理說明中的「管理程式的進程傾印工具以進行偵錯工具的偵錯工具」。

## <a name="process-initialization"></a>進程初始化

許多伺服器應用程式在啟動和關閉時，都必須進行特定的初始化和清除作業。 在 Windows Server 2003 上執行時，您可以建立可執行 [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer)介面的類別。 當處理常式啟動時，它會呼叫 [**IProcessInitializer：： Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) ，而當關機時，它會呼叫 [**IProcessInitializer：： Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown)。 這可讓您的元件有機會進行需要的工作，例如初始化連接、檔案和快取。

## <a name="running-com-applications-as-nt-services"></a>以 NT 服務的形式執行 COM + 應用程式

COM + 開發人員現在可以使用 [元件服務] 系統管理工具，將 COM + 伺服器應用程式設定及執行為 NT 服務。 這表示，如果您的應用程式一律需要執行，則可以自動啟動或重新開機伺服器;如果您的 COM + 應用程式需要執行特殊許可權的作業，您的 COM + 應用程式可以執行為本機系統帳戶;而且您的應用程式相依服務現在可以自動啟動。 如需詳細資訊，請參閱 [以服務應用程式形式執行的 Com + 應用程式](com--applications-running-as-service-applications.md) 。

## <a name="side-by-side-assemblies"></a>並存元件

並存 (SxS) 元件可讓應用程式指定要使用哪個版本的系統 DLL 或傳統 COM 元件，例如 MDAC、MFS、MSVCRT.LIB 或 MSXML。 例如，如果 ASP 應用程式依賴 MSXML 版本2.0，您可以確保即使在將 service pack 套用到伺服器之後，此應用程式仍會使用 MSXML 2.0 版。 也就是，即使電腦上已安裝新版的 MSXML，仍會保留2.0 版並供您的應用程式使用。

若要設定 SxS 元件，您需要知道 DLL 的路徑，而且每個需要使用 DLL 的虛擬目錄中都有 COM + 資訊清單檔案。 COM + 資訊清單是 XML 檔案，其中包含安裝 DLL 的相關資訊。 資訊清單是用來建立應用程式的啟用內容。 啟用內容可讓應用程式載入特定 DLL 版本、COM 物件實例或自訂視窗版本。 您可以使用 [元件服務] 系統管理工具或 ApplicationDirectory 屬性，輸入包含有效 SxS 組件資訊清單檔的應用程式根目錄的完整路徑。 如需詳細資訊，請參閱 [隔離的應用程式和並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)。

## <a name="windows-error-reporting"></a>Windows 錯誤報告

com + 1.5 包含 Windows 錯誤報告 (WER) 元件的支援，從 Windows XP 開始提供。 WER 可讓使用者將應用程式錯誤、核心錯誤和無回應的代理程式更新 Microsoft。 這些通知可讓 Microsoft 客戶支援小組更有效率地解決技術問題。 此外，Windows 錯誤報告元件可讓 com + 開發人員接收可用來改善其應用程式的資訊。 如需詳細資訊，請參閱 [Windows 錯誤報告](/windows/desktop/wer/windows-error-reporting)。

 

 
