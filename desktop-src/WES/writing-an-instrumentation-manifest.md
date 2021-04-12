---
title: 撰寫檢測資訊清單
description: 應用程式和 Dll 會使用檢測資訊清單來識別其檢測提供者和提供者寫入的事件。
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375389"
---
# <a name="writing-an-instrumentation-manifest"></a>撰寫檢測資訊清單

應用程式和 Dll 會使用檢測資訊清單來識別其檢測提供者和提供者寫入的事件。 資訊清單是 XML 檔案，其中包含識別提供者的元素。 慣例是使用. man 做為您的資訊清單的延伸模組。 資訊清單必須符合事件資訊清單 XSD。 如需架構的詳細資訊，請參閱 [EventManifest 架構](eventmanifestschema-schema.md)。

檢測提供者是呼叫 [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)、 [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)或 [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) 函數的任何應用程式或 DLL，以將事件寫入 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) 追蹤會話或事件記錄檔通道。 應用程式可以定義單一檢測提供者來涵蓋它寫入的所有事件，或是定義應用程式的提供者，以及其每個 Dll 的提供者。 應用程式在資訊清單中定義的提供者數目，完全取決於應用程式要如何組織其所寫入的事件。

為每個 DLL 指定提供者的優點是，您接著可以啟用和停用個別提供者，以及它們所產生的事件。 只有當 ETW 追蹤會話啟用提供者時，才適用這項優點。 指定事件記錄檔通道的任何事件一律會寫入至該通道。

資訊清單必須識別提供者和它所寫入的事件，但其他中繼資料（例如通道、層級和關鍵字）是選擇性的;您是否要定義選擇性的中繼資料，取決於將取用事件的物件。 例如，如果系統管理員或支援人員使用從事件記錄通道讀取事件的 Windows 事件檢視器之類的工具來取用事件，則您必須定義要寫入事件的通道。 不過，如果提供者只會由 ETW 追蹤會話啟用，則您不需要定義通道。

雖然層級、工作、opcode 和關鍵字中繼資料都是選擇性的，但您應該使用它們來以邏輯方式分組或區出事件。 分組事件可協助取用者只取用感興趣的事件。 例如，取用者可以查詢層級為「重大」且關鍵字為「寫入」的所有事件，或查詢特定工作所寫入的所有事件。

除了使用 level 和關鍵字來取用特定類型事件的取用者之外，ETW 追蹤會話還可以使用層級和關鍵字中繼資料來告訴 ETW，以限制寫入事件追蹤記錄檔的事件。 例如，會話可能會將事件限制為只有層級為 "error" 或 "critical" 且關鍵字為 "read" 的事件。

提供者可以定義篩選器，讓會話用來根據事件資料篩選事件。 使用層級和關鍵字時，ETW 會判斷是否將事件寫入記錄檔，但使用篩選準則，提供者會使用篩選資料準則來判斷它是否會將事件寫入該會話。 只有當 ETW 追蹤會話啟用您的提供者時，篩選才適用。

下列各節說明如何定義資訊清單的元件：

-   [識別提供者](identifying-the-provider.md)
-   [定義寫入事件的通道](defining-channels.md)
-   [定義提供者所寫入事件的嚴重性層級](defining-severity-levels.md)
-   [定義您的提供者所執行的工作和作業](defining-tasks-and-opcodes.md)
-   [定義分類提供者所寫入之事件的關鍵字](defining-keywords-used-to-classify-types-of-events.md)
-   [定義提供者用來篩選所寫入之事件的篩選準則](defining-filters.md)
-   [定義您的範本資料參考的名稱/值對應](defining-name-value-mappings.md)
-   [定義定義事件特定資料的範本](defining-event-data-templates.md)
-   [定義提供者寫入的事件](defining-events.md)

雖然您可以手動撰寫檢測資訊清單，但您應該考慮使用 Windows SDK Bin 資料夾中包含的 ECManGen.exe 工具 \\ 。 ECManGen.exe 工具會使用 GUI，引導您從頭開始建立資訊清單，而不需要使用 XML 標記。 在使用此工具時，知道本節和 [EventManifest 架構](eventmanifestschema-schema.md) 區段中的資訊將有所説明。

如果您使用 Visual Studio 做為 XML 編輯器，則可以將 [EventManifest](eventmanifestschema-schema.md) 架構加入至專案 (請參閱 XML 功能表) 以利用 Intellisense、內嵌架構驗證及其他功能，讓您更輕鬆且精確地撰寫資訊清單。

寫入資訊清單之後，請使用訊息編譯器來驗證資訊清單，並產生您在提供者中包含的資源和標頭檔。 如需詳細資訊，請參閱 [編譯檢測資訊清單](compiling-an-instrumentation-manifest.md)。

下列範例顯示完整定義之事件資訊清單的基本架構。


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 