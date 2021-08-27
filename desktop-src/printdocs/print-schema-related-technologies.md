---
description: 探索與列印架構相關的技術。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: 列印 Schema-Related 技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2948108b8bd6f581608471c9646fe135f83cb91561dc3c4cca97ac4df10560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112268"
---
# <a name="print-schema-related-technologies"></a>列印 Schema-Related 技術

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

在 .NET Framework 3.0、Windows Vista 和更新版本中，PrintCapabilities 和 PrintTicket 技術會擴充列印架構的功能，以提供更豐富的列印體驗。

## <a name="printcapabilities"></a>PrintCapabilities

PrintCapabilities 技術是一種方式，可發佈使用者可控制的每個工作屬性和設定的設定描述。 PrintCapabilities 是以可延伸的標記語言發佈 (XML) 檔，稱為 PrintCapabilities 檔，其中包含在 Print Schema 關鍵字和私用延伸模組中定義的詞彙。 PrintCapabilities 檔可以視為使用者可設定狀態目前裝置設定的「快照集」，以及可能設定的描述。 裝置 (或設備磁碟機) 在用戶端（可以是應用程式或列印子系統）進行查詢時，產生一份 PrintCapabilities 檔 (其目前可設定選項組的快照) 。 本檔說明裝置上目前可用的所有可設定 PrintCapabilities，例如裝訂選項和頁面配置選項。 PrintCapabilities 檔會明確描述裝置的所有屬性和每個屬性允許的設定。 透過使用列印架構架構，可以精確地描述和有效率地比較裝置屬性。 藉由使用 Print Schema 關鍵字檔中包含的關鍵字和列印架構架構中定義的結構，裝置可讓用戶端更有效地使用 PrintCapabilities。 如需詳細資訊，請參閱 [PrintCapabilities 架構和檔結構](printcapabilities-schema-and-document-construction.md)。

相對於 Microsoft Windows Server 2003 及更早版本中的列印子系統，PrintCapabilities 技術可讓用戶端和列印子系統元件以透明的方式，查看目前 Win32 系統二進位 PrintCapabilities 中包含的資訊。 如此一來，用戶端就可以查詢 PrintCapabilities、接收一致且易懂的 XML 快照集，並使用它來建立裝置的 PrintTicket，而不需要叫用驅動程式使用者介面 (UI) 。

## <a name="printticket"></a>PrintTicket

PrintTicket 技術是目前 DEVMODE 結構的後續。 它是一種可擴充的標記語言檔，可指定和保存作業格式設定和列印工作設定的相關資訊。 PrintTicket 實例會指派特定的裝置設定，並傳達使用者意圖。 有兩種類型的 PrintTickets：不會針對特定裝置產生的一般 PrintTickets;以及針對特定裝置所建立的裝置特定 PrintTickets。 一般 PrintTickets （可在不同裝置上移植），只要針對列印架構關鍵字中所述的每個裝置屬性選取設定，即可衍生其內容。 裝置特定 PrintTickets 會從 PrintCapabilities 檔衍生其內容，並針對本檔所公告的每個裝置屬性選取設定。 這些 PrintTickets 也可能包含單一裝置型號或裝置型號系列專屬的私用延伸模組。 如需詳細資訊，請參閱 [PrintTicket 架構和檔結構](printticket-schema-and-document-construction.md)。

相對於目前的列印子系統，PrintTicket 技術可讓列印子系統的所有元件和用戶端，以透明的方式存取目前儲存在 DEVMODE 結構之公用和私用部分中的資訊，並使用定義完善的 XML 格式。 這項設計解決了驅動程式升級或降級，以及針對 PrintTicket 技術設計的驅動程式中的驅動程式不符案例的目前問題。 這些案例目前可能會導致設定遺失，因而導致客戶體驗負面。 PrintTicket 也啟用了新的案例，例如啟用印表機驅動程式，以一致且明確的方式，將其私用的 DEVMODE 設定公開給應用程式和自訂外掛程式。 這可讓列印元件更透明，並更明確地處理設定。 您可以透過 managed 程式碼物件上的方法，將 PrintTicket 介面公開給應用程式，這些方法也可供腳本使用。 在 .NET Framework 3.0 中的 managed 程式碼物件上建的新應用程式架構中，PrintTicket 是描述檔設定的標準方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



