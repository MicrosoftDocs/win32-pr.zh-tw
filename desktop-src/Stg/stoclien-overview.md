---
title: StoClien 總覽
description: StoClien 範例會示範用戶端如何使用結構化儲存體，以及它如何指示伺服器元件使用此儲存體。
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- StoClien 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a28c8d0f4740b5a1d5f93934fb055d16e2ed9d843bcb11b210e6cde9589d53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661848"
---
# <a name="stoclien-overview"></a>StoClien 總覽

## <a name="purpose"></a>目的

[StoClien](structured-storage-client-sample--stoclien-.md)範例的主要焦點是用戶端如何使用結構化的儲存體，以及它如何指示伺服器元件使用此儲存體。 StoClien 範例示範結構化儲存體服務的程式設計模型。

## <a name="functionality"></a>功能

[StoClien](structured-storage-client-sample--stoclien-.md)功能類似于某些 Microsoft Visual C++ 版本中的「自由曲線」範例。 StoClien 範例和 [StoServe](structured-storage-server-sample--stoserve-.md) 範例之間的差異在於以 COM 技術為基礎的內部架構。 在 COM 用戶端與 COM 伺服器之間會保持清楚的架構差異。

[StoClien](structured-storage-client-sample--stoclien-.md) 會在 COM 複合檔案的結構化儲存體中載入並儲存其繪圖。

[StoClien](structured-storage-client-sample--stoclien-.md)範例會建立並使用在 \_ [StoServe](structured-storage-server-sample--stoserve-.md)伺服器中提供作為 CLSID DllPaper 元件的可連接 COPaper COM 物件。 StoClien 用戶端會建立 COPaper 物件，並透過該物件公開的 IPaper 介面來控制它。 StoClien 會取得使用者的繪圖資料，並在其管理的視窗中以圖形方式呈現資料。 StoClien 會使用 COPaper IPaper 介面，將繪圖資料儲存在 COPaper 中，並將此資料的檔案儲存作業導向。

COPaper COM 物件只會封裝繪圖紙張資料的伺服器型儲存：伺服器端沒有提供 (GUI) 行為的圖形化使用者介面。 所有 GUI 行為都會在用戶端中隔離。 COPaper 物件的資料管理和儲存功能只可透過 COM 自訂介面 IPaper。

[StoClien](structured-storage-client-sample--stoclien-.md) 會合作與 COPaper，以載入並儲存 COPaper 繪圖資料。 StoClien 會取得複合檔案中儲存物件的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。 在其載入和儲存作業中，StoClien 會將 **IStorage** 介面的指標傳遞到伺服器中的 COPaper。 COPaper 會使用提供的 **IStorage** 在儲存體中建立資料流程。 COPaper 接著可以使用標準 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面，來讀取和寫入其所管理的繪圖資料。

COPaper 只會管理繪圖資料;它不會執行任何 GUI 動作。 [StoClien](structured-storage-client-sample--stoclien-.md) 為繪圖應用程式提供 GUI。 它會將此封裝在中央 CGuiPaper c + + 物件中。

[StoClien](structured-storage-client-sample--stoclien-.md) 也會在 COPaperSink COM 物件中執行自訂 IPaperSink 介面，並將此介面連接至伺服器 COPaper 物件中的適當連接點。 COPaper 會使用連接的 IPaperSink 介面，將通知傳回至 StoClien。 使用 COPaper 的可連線物件技術，在 StoClien 中完成 COPaper 繪圖資料的一般 GUI 重新繪製。

[StoClien](structured-storage-client-sample--stoclien-.md) 是一種應用程式，您可以使用一般方式或從命令提示字元視窗直接執行。 StoClien 會在命令列上接受選擇性的檔案名參數。

在下列範例中，DllPaper 是複合檔案，其中包含繪製資料的相容結構化儲存體。 如果未指定任何命令列檔案名參數，則 [StoClien](structured-storage-client-sample--stoclien-.md) 會使用預設的檔案名 StoClien，並嘗試在與執行中 Stoclien.exe 相同的目錄中開啟該名稱。

**StoClien c： \\ 繪圖 \\ 繪圖。 pap**

## <a name="support-information"></a>支援資訊

如需 [StoClien](structured-storage-client-sample--stoclien-.md)的詳細資訊、功能描述和程式碼教學課程，請參閱 Stoclien.htm 中的程式碼導覽一節。 如需 StoClien 的外部使用者作業的詳細資訊，請參閱 Stoclien.htm 中的 [使用方式] 和 [作業] 區段。 若要讀取 Stoclient.htm，請在主要教學課程目錄中執行 Tutorial.exe，然後按一下課程表中的 StoClien 課程。 或者，在 Windows 檔案總管中尋找主要教學課程目錄之後，請按一下 [Stoclien.htm]。 如需 [**StoServe**](structured-storage-server-sample--stoserve-.md) 的運作方式，以及如何將其服務公開給 StoClien 的詳細資訊，請參閱主要教學課程目錄中的 Stoserve.htm。 請注意，您必須先建立 Stoserve.dll，才能建立 StoClien。 [**StoServe**](structured-storage-server-sample--stoserve-.md)的 makefile 會在系統登錄中註冊該伺服器，因此您必須先建立 [**StoServe**](structured-storage-server-sample--stoserve-.md) ，然後再嘗試執行 StoClien。

如需有關在此 COM 教學課程系列中設定系統以建立和測試程式碼範例的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。 提供的 makefile (MAKEFILE) 與 Microsoft NMAKE 相容。 若要建立 debug 組建，請在 [命令提示字元] 視窗中發出 NMAKE 命令。

為了方便起見，會提供每個範例的專案檔，以用於 Microsoft Visual Studio。 若要載入[StoClien](structured-storage-client-sample--stoclien-.md)範例的專案，請在範例目錄中的命令提示字元執行 Visual Studio，如下所示：

MSDEV STOCLIEN.DSP

您也可以按兩下 Windows 檔案總管中的 Stoclient，將範例專案載入 Visual Studio。 在 Visual Studio 中，您可以流覽範例來源的 c + + 類別，並通常執行其他編輯編譯-編譯-debug 作業。 請注意，在伺服器 SDK 中，從 Visual Studio 編譯這些範例需要在 Visual Studio 中正確設定目錄路徑。 如需詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。

## <a name="remarks"></a>備註

您必須先編譯用戶端範例和其他相關的範例，才能執行用戶端。 如需建立範例的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。 如果您已建立適當的範例，Stoclien.exe 是要針對此範例執行的用戶端可執行檔。

Stoclien.exe 的應用程式會提供此教學課程的使用者介面。 它會執行相關聯但獨立的 Stoserve.dll，以示範在複合檔案中使用 COM 結構化儲存的用戶端和伺服器。

 

 




