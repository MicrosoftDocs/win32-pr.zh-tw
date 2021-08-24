---
description: 這是 Microsoft 所提供之四種追蹤技術的每一項所預期的事件端對端旅程： TraceLogging、資訊清單型、WPP 和 MOF 的總覽。
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: 事件中繼資料總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931b8adbdb22cdbf2e0806e2d69c367e64ad92926390825a48a2fa51d50605ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755058"
---
# <a name="event-metadata-overview"></a>事件中繼資料總覽

這是 Microsoft 所提供之四種追蹤技術的每一項所預期的事件端對端旅程： [TraceLogging](../tracelogging/trace-logging-about.md)、 [資訊清單型](writing-manifest-based-events.md)、 [WPP](windows-software-trace-preprocessor.md)和 [MOF](tracing-events.md)的總覽。 它會針對個別事件的裝載和描述其結構的相關中繼資料，進行相關的問題，讓您稍後可以將事件解碼成合理的資料片段。 在選擇適合專案的追蹤技術時，請務必瞭解事件每個部分的旅程。 沒有適用于追蹤的一體適用方案。

## <a name="event-payloads"></a>事件承載

針對任何 Microsoft 提供的追蹤技術，當呼叫 [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite)的寫入命令 (for TraceLoggingWrite for TraceLogging) 的資訊清單型或 [](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite)時，在執行時間為事件提供的資料會折迭成稱為事件承載的連續二進位 blob。 這與事件架構或事件中繼資料不同 (如下所述) ，其中描述此二進位 blob 的版面配置以用於解碼工具。 事件承載的產生方式會根據所使用的追蹤技術，以及最終事件是否為傳統 ([**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) 樣式) 或新式 (**EventWrite** 樣式) 而有所不同。

若為傳統事件， [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) 中的旗標會傳遞至 [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) ，以判斷發生的情況：

\- 如果指定了 **WNODE \_ 旗標 \_ 使用 \_ Mof \_ PTR** ，則 [**mof \_ 欄位**](/windows/win32/api/evntrace/ns-evntrace-mof_field) 的陣列會在記憶體中的 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) 之後。 ETW 執行時間會串連這些欄位中所指定的事件資料，以形成事件裝載。

\- 如果未指定 **WNODE 旗標， \_ \_ \_ \_** 則在 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)之後，使用者會直接在記憶體中建立事件承載。

MOF 和 WPP 都是傳統提供者。 不過，WPP 的執行會為您處理這一切。

針對非傳統事件，會將一些 [**事件 \_ 資料 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) 項傳遞至 [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite)。 ETW 執行時間會串連這些描述項中所指定的事件資料，以形成事件裝載。

以資訊清單為基礎的 TraceLogging 技術通常是新式提供者。 使用以資訊清單為基礎的，如果您讓 mc.exe 為您產生 (um 或公里切換) 的記錄程式碼，則會為您處理承載產生。 承載的產生一律由 TraceLogging 負責處理。

最後的結果是會在執行時間產生事件的承載。 所有裝載基本上都很類似，因為它們是資料的二進位 blob，不論使用的是哪一種追蹤技術，以及該追蹤技術支援哪些欄位類型。 如果沒有事件中繼資料，事件裝載就沒有意義，而且 unintelligable。

接著，ETW 執行時間的職責是將此事件 blob 從提供者傳遞給取用者，然後將其重新關聯至其中繼資料，並變成 decodable。 ETW 執行時間會加入一些額外的中繼資料，指出承載的情況（例如時間戳記、執行緒識別碼和事件的關鍵字）。 這項資訊與事件透過執行時間路由的方式有關，也適用于在解碼時瞭解事件的身分識別和內容。 它最後會顯示為取用者的 [**事件 \_ 追蹤**](/windows/win32/api/evntrace/ns-evntrace-event_trace) 或 [**事件 \_ 記錄**](/windows/win32/api/evntcons/ns-evntcons-event_record) 的一部分。

## <a name="event-metadata"></a>事件中繼資料

事件中繼資料的旅程會根據所使用的追蹤技術而有所不同，而且是比較每項技術時最大的考慮之一。

### <a name="mof"></a>MOF

事件中繼資料是以 mof 檔案中特殊 MOF 架構的形式，由事件建立者手動撰寫的。 撰寫的架構必須符合記錄的承載，才能讓取用者正確地將事件解碼。 事件解碼器需要使用 [mofcomp.exe](../wmisdk/mofcomp.md)在系統上註冊 mof 檔案。 如需發佈 MOF 架構的詳細資訊，請參閱 [發佈您的傳統提供者的事件架構](publishing-your-event-schema-for-a-classic-provider.md)。

### <a name="wpp"></a>WPP

事件中繼資料會在建立程式期間 tracewpp.exe 自動產生，並儲存在您二進位的 .pdb 中。 您稍後可以使用 tmf 檔案的格式，透過 tracepdb.exe 將此中繼資料解壓縮。 事件解碼器通常需要 .pdb 或 tmf 檔案。 如需 tracepdb.exe 的詳細資訊，請參閱 [Tracepdb 總覽](/windows-hardware/drivers/devtest/tracepdb-overview)，如需 tracewpp.exe 的詳細資訊，請參閱 [TraceWPP task](/windows-hardware/drivers/devtest/tracewpp-task)。

### <a name="manifest-based"></a>以資訊清單為基礎

事件定義是在 man 檔中撰寫的。 事件資訊清單會透過資訊清單編譯器 ([mc.exe](../wes/message-compiler--mc-exe-.md)) ，產生來源編譯所需的標頭，以及數個 bin 二進位資源檔。 然後，您必須將這些資源檔編譯成二進位檔，並將產生的二進位檔編譯成系統，以將來自該資訊清單型提供者的事件解碼。 此外，資訊清單必須在系統上安裝 [wevtutil.exe](../wes/windows-event-log-tools.md) 最重要的是，已安裝事件資訊清單中提供者 XML 元素上的 **resourceFileName** 和 **messageFileName** 屬性必須正確地識別放置資源檔之二進位檔的完整絕對路徑。 請注意，您可以使用 wevtutil.exe 參數/rf 和/mf.，在資訊清單安裝時覆寫這些路徑。 未正確且完全執行這些步驟的系統將無法解碼來自此提供者的事件。 因此，事件的解碼器需要已安裝的資訊清單，並將具有相關聯資源的二進位檔安裝在資源和訊息檔案路徑所指定的位置。 如需發行以資訊清單為基礎之架構的詳細資訊，請參閱 [發佈事件架構以取得以資訊清單為基礎的提供者](publishing-your-event-schema-for-a-manifest-base-provider.md)。

### <a name="tracelogging"></a>TraceLogging

所有 TraceLogging 事件都是自我描述的。 解碼事件所需的事件中繼資料會自動產生，並以精簡的二進位格式連同承載一起傳送。 事件解碼器只需要 TraceLogging 事件並瞭解 TraceLogging 元資料格式。

## <a name="configuring-tdh-for-decoding"></a>設定解碼的 TDH

其中有許多解碼工具。 不過，建議您盡可能使用 TDH，因為它會使用統一的 API 來解碼所有追蹤技術。 根據您對解碼感興趣的追蹤類型而定，TDH 可能需要明確設定。

### <a name="mof"></a>MOF

TDH 利用在系統上使用 mofcomp.exe 註冊的 MOF 解碼資料。 如需詳細資訊，請參閱 [發行傳統提供者的事件架構](publishing-your-event-schema-for-a-classic-provider.md)。

### <a name="wpp"></a>WPP

TDH 必須指向 .pdb 檔案或相關聯的 tmf，以找出您嘗試解碼的 WPP 提供者。 您可以藉由呼叫 [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)來執行此作業。 否則，解碼引擎會回到環境變數追蹤 \_ 格式 \_ 搜尋 \_ 路徑。

### <a name="manifest-based"></a>以資訊清單為基礎

TDH 會利用使用 wevtutil.exe 在系統上註冊的所有以資訊清單為基礎的提供者。

### <a name="tracelogging"></a>TraceLogging

最新版本的 TDH 會自動偵測 TraceLogging 事件並將其解碼，而無需額外的步驟。

 

 
