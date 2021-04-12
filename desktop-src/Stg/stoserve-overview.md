---
title: StoServe 總覽
description: StoServe 程式碼範例示範如何使用複合檔案執行所提供的結構化儲存體服務。 描述使用標準 IStorage 和 IStream 介面。
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315931"
---
# <a name="stoserve-overview"></a>StoServe 總覽

## <a name="purpose"></a>目的

這個程式碼範例的主要焦點是使用複合檔案執行所提供的結構化儲存體服務。 描述使用標準 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面。 **StoServe** 可與 [StoClien](structured-storage-client-sample--stoclien-.md) 程式碼範例搭配使用，以說明用戶端和伺服器對複合檔案儲存體的聯合使用。

## <a name="functionality"></a>功能

**StoServe** 範例引進 COPaper COM 物件，它幾乎代表一張紙紙的空白工作表。

COPaper 物件會公開一組功能，以使用指定之色彩和寬度的 "筆墨"，在紙張表面上自由形式的繪圖。 這項功能的外表方式類似于許多 Microsoft Visual C++ 版本中的「自由曲線」教學課程範例。 **StoServe** / **StoClien** 範例中的差異在於，主要是以 COM 技術為基礎的架構。 COPaper 物件的電子繪圖檔案功能可透過自訂 [**IPaper**](ipaper-methods.md) 介面提供給用戶端使用。 COPaper 會實 **IPaper** 介面。 用戶端與伺服器之間會保持清楚的架構差異。 COPaper 不會提供 (GUI) 的圖形化使用者介面。 COPaper 物件的設計依賴用戶端進行所有 GUI 行為。 COPaper 只會封裝繪製筆墨資料的伺服器型捕獲和儲存。

在 COPaper 介面上繪製的筆墨資料可以儲存在複合檔案中，也可以從複合檔案載入。 [**IPaper**](ipaper-methods.md)、 [**Save**](ipaper--save.md)和 [**Load**](ipaper--load.md)方法都會接受 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)介面指標。 COPaper 會使用此用戶端提供的 **IStorage** 介面來儲存繪圖資料。

COPaper 是存放在同進程伺服器中，而且會公開提供作為自訂 COM 元件。 與本教學課程系列中的其他伺服器類似，StoServe 是自我註冊的 COM 伺服器。 它會使用登錄中的 CLSID DllPaper 註冊，讓用戶端使用 COPaper 物件類型作為 DllPaper 元件 \_ 。

如同先前的節省伺服器，COPaper 支援可連線物件功能。 [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)介面會公開，並執行適當的連接點。 在此內容中，會宣告外寄自訂 IPaperSink 介面，以便在傳送通知給用戶端時使用。

這兩個 [**IPaper**](ipaper-methods.md) 和 [**IPaperSink**](ipapersink-methods.md) 自訂介面是在 IPaper 中宣告的。H 位於一般的共屬 \\ inc. 目錄。 介面和物件的 Guid 是在 PAPGUIDS 中定義。H 位於相同的一般 include 目錄。

**StoServe** 會使用 APPUTIL 中的 CThreaded 設備來達成執行緒安全性，如同 FRESERVE 範例中所述。 COPaper 物件衍生自 CThreaded 類別，並繼承其 OwnThis 和 UnOwnThis 方法。 這些方法一次只允許一個執行緒存取 **StoServe** 伺服器，以及 COPaper 由伺服器管理的物件。

## <a name="copaper-com-object"></a>COPaper COM 物件

COPaper COM 物件是由此 **StoServe** 同進程伺服器管理的單一物件類型。 COPaper 是以可連接的 COM 物件來建立，並採用標準 [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) 介面和自訂 [**IPaper**](ipaper-methods.md) 介面的實作為。 COPaper 會公開 **IPaper** 介面，讓用戶端可以在 COPaper 的實例上執行一組小型的電子檔作業。 基本作業是啟動筆墨繪圖序列、在 COPaper 虛擬紙張表面上繪製筆墨資料，以及結束筆墨繪圖順序。 在此配置中，會假設用戶端是由滑鼠或平板電腦裝置驅動的 GUI 應用程式。 用戶端負責將滑鼠移動轉譯為 COPaper 的要求，以將這些要求儲存為筆墨資料。

COPaper 中有兩種層級的筆墨資料儲存。 COPaper 會將筆墨資料儲存在代表目前繪圖的 RAM 型陣列中，而 COPaper 會持續將整個繪圖儲存成複合檔案。 [**IPaper**](ipaper-methods.md)介面中的方法會執行兩者。

因為用戶端不會管理繪製的紙張資料，而是負責將它轉譯為螢幕上的影像，所以 COPaper 中的 [**IPaper**](ipaper-methods.md) 執行必須公開方法，讓用戶端可以取得繪圖資料。 COPaper 中的可連線物件技術可用於此用途。 CONNPOINT \_ PAPERSINK 連接點是由 COPaper 所執行，因此用戶端可以連接到 COPaper 來接收筆墨資料以進行繪製。 用戶端會先在 COPaper 物件上呼叫 [IPaper：：重繪](ipaper--redraw.md) 方法，以要求目前繪圖的所有筆墨資料。 重繪的 COPaper 執行會使用 [**IPaperSink**](ipapersink-methods.md) 的用戶端執行，將資料傳遞給用戶端。

當使用者以互動方式在用戶端中繪製時，它會立即將資料繪製到螢幕，同時也會將資料傳送到 COPaper 進行儲存。 當用戶端需要重新繪製畫面時，它會呼叫 COPaper 重新 [繪製](ipaper--redraw.md) 方法。 這類重新繪製在應用程式中是很常見的。 例如，當用戶端視窗與另一個應用程式視窗重迭時，就會發生重新繪製。 用戶端有繪製影像的點陣圖轉譯，但點陣圖很容易遺失，且通常必須重新繪製。 用戶端會依賴伺服器中的 COPaper，以取得重畫所需的筆墨資料。

這是一項常見的用戶端/伺服器的人力。 當有多個用戶端需要共用資料時，特別適合。 COPaper 會進行編碼以啟用此功能。 它會使用 APPUTIL CThreaded 設備來達成執行緒安全。 可能會利用這項設計的應用程式是共用的白板應用程式，可讓多個用戶端參與經常觀看的繪圖。 COM 支援分散式 COM (DCOM) 支援這種類型的工作組應用程式在網路上的使用方式。 如需詳細資訊，請參閱先前的 REMCLIEN 範例。

COPaper 用戶端/伺服器配置更適度的使用方式，就是針對在同一部電腦上不同應用程式中所執行的物件，整合其行為。 在此情況下，用戶端可能是個別應用程式中，共用相同物件所管理之資料的 ActiveX 容器。 此資料可能不是 DllPaper 元件支援的筆墨繪圖資料。 **StoServe** 可做為管理其他共用資料類型之程式設計元件的起始架構。

## <a name="support-information"></a>支援資訊

**StoServe** makefile 會在登錄中註冊 **StoServe** DllPaper COM 元件。 此元件必須在 **StoServe** 可供外部 COM 用戶端作為該元件的伺服器之前註冊。 這項自我註冊是使用內建于註冊範例的 Register.exe 公用程式來完成。 若要建立或執行 **StoServe**，請先建立註冊程式碼範例。

如需有關設定系統以建立和測試此 COM 教學課程系列中程式碼範例的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。 提供的 makefile (MAKEFILE) 與 Microsoft NMAKE 相容。 若要建立 debug 組建，請在 [命令提示字元] 視窗中發出 NMAKE 命令。

為了方便使用 Microsoft Visual Studio，會針對每個範例提供專案檔。 若要載入 **StoServe** 範例的專案，您可以在範例目錄的命令提示字元中執行 Visual Studio，如下所示：

MSDEV STOSERVE.Dsp

您也可以按兩下 Windows 檔案總管中的 Stoserve，將範例專案載入 Visual Studio。 在 Visual Studio 您可以流覽範例來源的 c + + 類別，並通常執行其他編輯編譯-編譯-debug 作業。

> [!Note]  
> 作為平臺軟體發展工具組的一部分 (SDK) ，在 Visual Studio 中編譯這些範例需要 Visual Studio 中正確設定目錄路徑。 如需詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。

 

 

 