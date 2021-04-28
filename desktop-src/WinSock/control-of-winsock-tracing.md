---
description: Winsock 追蹤的控制權
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Winsock 追蹤的控制權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f256c4e3927672bc13b14bfb72ca3b02c22bde
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110546"
---
# <a name="control-of-winsock-tracing"></a>Winsock 追蹤的控制權

您可以使用下列其中一種方法來控制 Winsock 追蹤：

-   命令列工具

    Windows Vista 和 Windows Server 2008 中包含兩個命令列工具，可用來控制追蹤並將二進位追蹤記錄檔轉換為可讀取的文字。

    **logman.exe** 工具是用來啟動或停止 Winsock 追蹤。

    **tracerpt.exe** 工具是用來將二進位追蹤記錄檔轉換成可讀取的文字檔。

-   事件檢視器

    Windows Vista 和更新版本上的事件檢視器也可以用來啟用 Winsock 追蹤。 事件檢視器可從 [開始] 功能表的系統管理工具存取。

## <a name="using-logman-and-tracert"></a>使用 logman 和 tracert

在 Windows Vista 和更新版本上，預設會停用 Winsock 網路事件追蹤。

下列命令會啟動電腦上的 Winsock 網路事件追蹤、將事件追蹤會話的名稱設定為 mywinsocksession，然後將輸出傳送至名為 winsocklogfile 的二進位記錄檔：

**logman start-ets mywinsocksession-o winsocklogfile .etl-p Microsoft-Windows-Winsock-AFD**

記錄檔是在目前的目錄中建立，其中包含 winsocklogfile 000001 格式的檔案名 \_ 。

下列命令會針對名為 mywinsocksession 的會話，在電腦上停止上述的 Winsock 追蹤：

**logman stop-ets mywinsocksession**

二進位記錄檔將會寫入– o 參數所指定的位置。 若要將二進位檔案轉譯成可讀取的文字檔，請使用 **tracerpt.exe** ：

**tracerpt.exe 的 .etl 檔案 <名稱> – o winsocktracelog.txt**

如果偏好包含 xml 而非純文字的輸出檔，則會使用下列命令：

**tracerpt.exe etl 檔的 <名稱> – o winsocktracelog.xml of xml**

在 Windows Vista 和更新版本上，預設會啟用 Winsock 目錄變更追蹤。

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

下列命令會針對在電腦上 (Lsp) 的多層式服務提供者啟動 Winsock 目錄變更追蹤、將事件追蹤會話的名稱設定為 mywinsockcatalogsession，然後將輸出傳送至名為 winsockcataloglogfile 的二進位記錄檔：

**logman start-ets mywinsockcatalogsession-o winsockcataloglogfile .etl-p Microsoft-Windows-Winsock-WS2HELP**

記錄檔是在目前的目錄中建立，其中包含 winsockcataloglogfile 000001 格式的檔案名 \_ 。

下列命令會針對名為 mysession 的會話，在電腦上停止上述的 Winsock 追蹤：

**logman stop-ets mywinsockcatalogsession**

二進位記錄檔將會寫入– o 參數所指定的位置。 若要將二進位檔案轉譯成可讀取的文字檔，請使用 **tracerpt.exe** ：

**tracerpt.exe 的 .etl 檔案 <名稱> – o winsockcatalogtracelog.txt**

如果偏好包含 xml 而非純文字的輸出檔，則會使用下列命令：

**tracerpt.exe etl 檔的 <名稱> – o winsockcatalogtracelog.xml of xml**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>使用事件檢視器啟動 Winsock 網路事件追蹤

當您開啟事件檢視器時，左窗格會包含事件的清單。 開啟 [ **應用程式及服務記錄** 檔]，並流覽至 [ **Microsoft \\ Windows \\ Winsock 網路事件** ] 作為來源，然後選取 [ **操作**]。

在 [動作] 窗格中，選取 [ **記錄** 內容]，然後選取 [ **啟用記錄** ] 核取方塊。 啟用記錄之後，您也可以變更記錄檔的大小（如果需要的話）。

Winsock 網路事件追蹤現在已啟用，您只需要重新整理動作，即可更新已記錄的事件清單。 若要停止記錄，只要取消選取相同的選項按鈕即可。

您可能需要根據您想要查看的事件數目來增加記錄檔大小。 使用事件檢視器進行 Winsock 追蹤的一個缺點是，它不會載入所有字串資源，因此在您選取事件) 時，[描述] 欄位中所顯示的訊息 (，有時很難讀取 (必須格式化為十六進位的引數會以十進位顯示，例如) 。 不過，您可以在 [事件描述] 中選取 [ **詳細資料** ] 索引標籤，以顯示原始 XML 記錄專案，這通常會更容易瞭解引數。

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>使用事件檢視器啟動 Winsock 類別目錄變更追蹤

當您開啟事件檢視器時，左窗格會包含事件的清單。 開啟 [ **應用程式及服務記錄** 檔]，並流覽至 [ **Microsoft \\ Windows \\ Winsock 目錄變更** ] 作為來源，然後選取 [ **操作**]。

在 [動作] 窗格中，選取 [ **記錄** 內容]，然後選取 [ **啟用記錄** ] 核取方塊。 啟用記錄之後，您也可以變更記錄檔的大小（如果需要的話）。

Winsock 目錄變更追蹤現在已啟用，您只需要重新整理動作，即可更新已記錄的事件清單。 若要停止記錄，只要取消選取相同的選項按鈕即可。

您可能需要根據您想要查看的事件數目來增加記錄檔大小。 使用事件檢視器進行 Winsock 追蹤的一個缺點是，它不會載入所有字串資源，因此在您選取事件) 時，[描述] 欄位中所顯示的訊息 (，有時很難讀取 (必須格式化為十六進位的引數會以十進位顯示，例如) 。 不過，您可以在 [事件描述] 中選取 [ **詳細資料** ] 索引標籤，以顯示原始 XML 記錄專案，這通常會更容易瞭解引數。

## <a name="interpreting-winsock-tracing-logs"></a>解讀 Winsock 追蹤記錄

記錄檔中的所有 Winsock 追蹤事件都包含兩種類型的資訊：

-   系統
-   EventData

系統資訊包含記錄層級、記錄專案的建立時間、代表事件種類的事件識別碼、執行處理常式識別碼、執行執行緒識別碼，以及其他系統資訊。 Winsock 追蹤中的記錄層級4表示資訊事件記錄。 Winsock 追蹤中的記錄層級5表示詳細的事件記錄。

系統資訊中的執行程式識別碼和執行緒識別碼，表示發生事件時正在執行的進程和執行緒。 在許多情況下，這將代表核心或背景工作執行緒和進程，而不是使用者模式執行緒和或應用程式的處理常式。 因此，此欄位通常不太實用。

每個 Winsock 追蹤事件種類在記錄資料的系統區段中都有唯一的事件識別碼。 這些事件識別碼很容易用來篩選特定 Winsock 追蹤事件的記錄檔。

Eventdata 包含事件種類的特定資訊。

Eventdata 資訊中的 Process 參數是進程的核心 EPROCESS 結構位址，而不是實際的 PID。 若要比對事件與使用者模式 PID，請從任何記錄專案的 eventdata 資訊中取得處理常式值，然後在記錄檔中查看具有處理常式值的通訊端建立事件。 找到相符專案之後，通訊端建立事件資料中的最後一個參數就是建立通訊端的使用者模式處理序識別碼。

在某些 Winsock 追蹤事件中，會傳回 eventdata 資訊中的位址參數。 Address 參數代表 IP 位址，但會顯示在 **tracerpt.exe** 工具所建立的文字檔中，或是以原始位元組或數位事件檢視器。 IPv6 位址會以十六進位顯示，因此更容易瞭解。 IPv4 位址會顯示為大十進位數。 開發人員必須以手動方式將 IPv4 位址的未經處理位元組轉換成較熟悉的 IPv4 小數點位址標記法，以便更容易解讀此值。

在某些 Winsock 追蹤事件中，會傳回 eventdata 中的錯誤參數。 錯誤參數的格式為 NTSTATUS 或 HRESULT 錯誤碼。 這個錯誤參數會顯示在 **tracerpt.exe** 工具所建立的文字檔中，或事件檢視器為十進位數。 開發人員必須手動將十進位數轉換成十六進位數位，以便在某些情況下更清楚地解讀錯誤碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Winsock 網路事件追蹤詳細資料](winsock-tracing-event-details.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> </dl>

 

 
