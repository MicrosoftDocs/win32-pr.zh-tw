---
title: 建立並執行 StoClien 範例
description: StoClien 可與 COM 伺服器中的 COPaper 物件合作，以在 COM 複合檔案中達成繪圖的持續性儲存。
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- 建立並執行 StoClien 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f00274293c05e21e660dc8e9448ca95946cab8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965977"
---
# <a name="create-and-run-stoclien-sample"></a>建立並執行 StoClien 範例

**StoClien** 可與 com 伺服器中的 COPaper 物件合作，以在 com 複合檔案中達成繪圖的持續性儲存。 如需 COPaper 在提供給 COPaper by **StoClien** 的複合檔案中使用資料流程的詳細資訊，請參閱 [**StoServe**](structured-storage-server-sample--stoserve-.md) 範例和 STOSERVE.HTM。 **StoServe** 範例也涵蓋了 COPaper 的結構及其 IPaper 介面。

## <a name="code-tour"></a>程式碼導覽

本程式碼教學課程中涵蓋的主要主題如下：

-   **CGuiPaper** 如何封裝 **StoClien** 的電子繪圖紙張的 GUI 行為
-   **StoClien** 如何捕捉及顯示互動式繪圖活動
-   **CGuiPaper** 物件如何使用 COPaper 來記錄繪圖資料
-   IPaperSink 連接在重新繪製中的使用方式
-   CPapFile **載入** 和 **儲存** 方法如何使用複合檔案中的結構化儲存體

因為 FRECLIEN 和 CONCLIEN 範例中使用的 **CGuiBall** 類別封裝了彈跳球的行為，所以 **StoClien** 會使用 **CGuiPaper** c + + 類別來封裝電子繪圖紙的資料和 GUI 行為。

下表列出與 **StoClien** 範例相關的檔案。



| 檔案        | Description                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | 簡短範例描述。                                                                                                        |
| 生成     | 用來建立程式碼範例的一般 makefile。                                                                               |
| STOCLIEN.H   | **StoClien** 應用程式的 include 檔。 包含類別宣告、函數原型和資源識別碼。   |
| STOCLIEN.Cpp | STOCLIEN.EXE 的主要執行檔。 具有 WinMain 和 CMainWindow 的執行，以及主功能表分派。 |
| STOCLIEN.鋼筋混凝土  | 應用程式資源定義檔。                                                                                        |
| STOCLIEN..ICO | 應用程式圖示資源。                                                                                                   |
| STOCLIEN.Pap | 應用程式的預設檔繪圖檔案。                                                                                |
| 鉛筆。當前   | 用戶端視窗資料指標的鉛筆影像。                                                                                     |
| 下沉。H       | COPaperSink COM 物件類別的類別宣告。                                                                      |
| 下沉。Cpp     | COPaperSink COM 物件類別的實檔案名。                                                                        |
| PAPFILE.H    | **CPapFile** c + + 類別的類別宣告。                                                                            |
| PAPFILE.Cpp  | **CPapFile** c + + 類別的實檔案。                                                                              |
| GUIPAPER.H   | **CGuiPaper** c + + 類別的類別宣告。                                                                           |
| GUIPAPER.Cpp | **CGuiPaper** c + + 類別的實檔案。                                                                             |
| STOCLIEN.Dsp | Microsoft Visual Studio 專案檔。                                                                                            |



 

## <a name="compound-files"></a>複合檔案

**StoClien** 依賴 COPaper 來記錄繪圖資料。 它也依賴 COPaper 將資料儲存在複合檔案中。 不過，在 COM 用戶端與伺服器之間的一般人力部門中， **StoClien** 會共用檔案儲存體的部分責任。 在用戶端為容器且伺服器為内嵌物件的 COM 應用程式中，這項工作相當重要。 在這種安排中，用戶端會負責建立或開啟結構化儲存體檔案，而伺服器物件則負責將該儲存體用於自己的資料儲存用途。 這可能牽涉到伺服器物件在提供給它的儲存體中建立 substorages。 它通常涉及在儲存體中建立資料流程物件的伺服器物件。 COPaper 使用儲存體串流的詳細資訊請見 **StoClien** 範例。

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)介面是由用戶端和伺服器物件用來執行檔案作業。 使用結構化儲存架構的複合檔案執行。 標準服務函數用於複合檔案的作業。 例如， [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 函式一開始會建立複合檔案，並傳回可用於操作檔案的 **IStorage** 指標。 這個特定的函式會在 **StoClien** 中呼叫。 它取得的 **IStorage** 介面會以參數的形式傳遞給 COPaper，以供使用。 COPaper 物件不會自行建立或開啟複合檔案：它會使用 **IStorage** 和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面，在提供給它的複合檔案中運作。

這些 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面不會在 **StoClien** 或 **StoServe** 中執行。 它們是在 COM 程式庫中執行。 當取得其中一個介面的指標時，它們的方法基本上會用來做為複合檔案上操作的一組服務。

 

 




