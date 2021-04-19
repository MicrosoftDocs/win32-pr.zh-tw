---
title: COM 詞彙
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969940"
---
# <a name="com-glossary"></a>COM 詞彙

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**啟動**
</dt> <dd>

將物件載入記憶體中的程式，使其進入執行狀態。

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**作用中狀態**
</dt> <dd>

處於執行中狀態且具有可見使用者介面的 COM 物件。

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**絕對標記**
</dt> <dd>

指定物件絕對位置的名字。 絕對的標記類似于完整路徑。

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**諮詢持有者**
</dt> <dd>

COM 物件，可快取、管理和傳送容器應用程式之諮詢接收器的變更通知。

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**諮詢接收**
</dt> <dd>

COM 物件，可接收内嵌物件或連結化物件中之變更的通知，因為它會執行 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) 或 [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) 介面。 需要收到物件變更通知的容器會執行諮詢接收。 通知源自伺服器，其使用諮詢持有者物件來快取和管理容器的通知。

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate 物件**
</dt> <dd>

由一或多個其他 COM 物件所組成的 COM 物件。 匯總中的一個物件會指定控制物件，此物件會控制匯總中的哪些介面會公開，哪些是私用的。 此控制物件具有 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 的特殊實，稱為控制 **iunknown**。 匯總中的所有物件都必須透過控制 **iunknown** 來傳遞對 **IUnknown** 方法的呼叫。

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**聚集**
</dt> <dd>

用來執行 COM 物件的組合技術。 它可讓您藉由重複使用一或多個現有物件的介面執行來建立新的物件。 「匯總」物件會選擇要公開給用戶端的介面，而介面會公開為「匯總」物件所執行的介面。 Aggregate 物件的用戶端只會與 aggregate 物件進行通訊。

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**環境屬性**
</dt> <dd>

由容器所管理和公開的執行時間屬性。 環境屬性通常代表表單的特性，例如背景色彩，必須傳達給控制項，讓控制項可以假設其周圍環境的外觀和風格。

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**反標記**
</dt> <dd>

檔案、專案或指標標記的反向。 反標記會新增至檔案、專案或指標標記的結尾，以使失效它。 反向標記會用於相對的擁有者的結構。

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**人工參考計數**
</dt> <dd>

一種技術，用來在呼叫可能會提前終結的函式或方法之前，協助保護物件。 程式呼叫 **IUnknown：： AddRef** 以遞增物件的參考計數，然後再進行呼叫，以釋放物件。 在函式傳回之後，程式會呼叫 **IUnknown：： Release** 來遞減計數。

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**非同步綁定**
</dt> <dd>

一種系結，在此類型中，必須以非同步方式進行程式，以避免使用者的效能降低。 一般情況下，非同步系結會用於全球 Web 等分散式環境。 OLE 支援非同步標記類別和回呼機制，可讓您在分散式環境中尋找和初始化物件的程式，在執行其他作業時才會發生。

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**非同步呼叫**
</dt> <dd>

呼叫個別執行的函式，讓呼叫端可以繼續處理指示，而不需等待函數傳回。

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**非同步標記**
</dt> <dd>

支援非同步綁定的標記。 例如，系統提供的 URL 標記類別的實例是非同步名字。

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**自動化**
</dt> <dd>

從應用程式外部操作應用程式物件的方法。 Automation 通常用來建立應用程式，以將物件公開至程式設計工具和宏語言、建立和操作另一個應用程式的應用程式物件，或建立用來存取和操作物件的工具。

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**系結內容**
</dt> <dd>

執行 [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) 介面的 COM 物件。 在標記系結時，系結內容會在標記作業中用來保存物件的參考。 系結內容包含在泛型複合標記系結期間套用至所有作業的參數，並提供可存取其環境相關資訊的標記實行。

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**綁定**
</dt> <dd>

將名稱與其引用相關聯。 具體而言，是找出以標記命名的物件，將它放入它的執行中狀態（如果尚未執行），並傳回介面指標給它。 您可以在執行時間系結物件 (也稱為晚期繫結或動態繫結) 或在編譯時期 (也稱為靜態系結) 。

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**緩存**
</dt> <dd>

 (通常是暫時) 的資訊本機存放區。 在 OLE 中，快取包含的資訊可在容器開啟時定義連結或内嵌物件的呈現方式。

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**快取初始化**
</dt> <dd>

以呈現資料填滿連結或内嵌物件的快取。 [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache)介面提供容器可呼叫的方法，以控制為連結或内嵌物件快取的資料。

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**類**
</dt> <dd>

程式碼中物件的定義。 在 c + + 中，物件的類別會定義為資料類型，但在其他語言中則不會發生這種情況。 因為 OLE 可以用任何語言撰寫，所以類別是用來參考一般物件定義。

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**
</dt> <dd>

COM 物件，該物件會執行 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面，並且建立指定類別識別碼所識別之物件的一或多個實例， (CLSID) 。

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**(CLSID) 的類別識別碼**
</dt> <dd>

與 OLE 類別物件相關聯 (GUID) 的全域唯一識別碼。 如果類別物件將用來建立多個物件實例，則相關聯的伺服器應用程式應該在系統登錄中註冊其 CLSID，讓用戶端可以找出並載入與物件 (的) 相關聯的可執行程式碼。 允許連結至其内嵌物件的每個 OLE 伺服器或容器，都必須為每個支援的物件定義註冊一個 CLSID。

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class 物件**
</dt> <dd>

在物件導向程式設計中，物件的狀態會由類別中的所有物件所共用，而且其行為會在該 classwide 狀態資料上運作。 在 COM 中，類別物件稱為 class factory，而且除了建立類別的新實例之外，通常不會有任何行為。

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**客戶**
</dt> <dd>

從另一個物件要求服務的 COM 物件。

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**用戶端網站**
</dt> <dd>

複合檔案中內嵌或連結化物件的顯示網站。 用戶端網站是物件從其容器要求服務的主要方式。

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**Clsid**
</dt> <dd>

與 OLE 類別物件相關聯 (GUID) 的全域唯一識別碼。 如果類別物件將用來建立多個物件實例，則相關聯的伺服器應用程式應該在系統登錄中註冊其 CLSID，讓用戶端可以找出並載入與物件 (的) 相關聯的可執行程式碼。 允許連結至其内嵌物件的每個 OLE 伺服器或容器，都必須為每個支援的物件定義註冊一個 CLSID。

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**提交**
</dt> <dd>

若要持續儲存對儲存體或資料流程物件所做的任何變更，因為它已開啟或上次儲存變更。

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**元件**
</dt> <dd>

封裝資料和程式碼的物件，並提供一組指定的公開可用服務。

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**元件物件模型 (COM)**
</dt> <dd>

OLE 物件導向程式設計模型，定義物件在單一進程內或處理常式之間的互動方式。 在 COM 中，用戶端可以透過在物件上執行的介面存取物件。

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**複合功能表列**
</dt> <dd>

共用的功能表列，由容器應用程式和就地啟動的伺服器應用程式中的功能表群組所組成。

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**複合標記**
</dt> <dd>

由兩個或多個被視為一個單位的標記所組成的標記。 複合的標記可以是非泛型，也就是說，其元件標記具有彼此的特殊知識（或泛型），也就是說，其元件的每個元件都不知道彼此的關係，只不過它們是名字標記

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**複合檔案**
</dt> <dd>

包含連結或内嵌物件的檔，以及其本身的原生資料。

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**複合檔案**
</dt> <dd>

OLE 提供的結構化儲存體實作為。

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM 物件**
</dt> <dd>

符合 OLE 元件物件模型 (COM) 的物件。 COM 物件是物件定義的實例，可指定物件的資料，以及物件上的一或多個介面介面。 用戶端只會透過其介面與 COM 物件互動。

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**可連線物件**
</dt> <dd>

一種 COM 物件，它至少會為 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 介面執行，以管理連接點物件。 可連線物件支援從伺服器到用戶端的通訊。 可連線物件會建立和管理一個或多個連接點子物件，以從其他物件上所執行的介面接收事件，並將它們傳送至用戶端。

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**連接點物件**
</dt> <dd>

由可連接的物件所管理，並可執行 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 介面的 COM 物件。 可連線物件可以建立和管理一個或多個連接點物件。 每個連接點物件都會管理來自另一個物件上特定介面的傳入事件，並將這些事件傳送至用戶端。

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**容器應用程式**
</dt> <dd>

支援複合檔案的應用程式。 容器應用程式會提供內嵌或連結化物件的儲存體、顯示的網站、對顯示網站的存取，以及接收物件變更通知的諮詢接收。

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**遏制**
</dt> <dd>

用來執行 COM 物件的組合技術。 它可讓一個物件重複使用一個或多個其他物件的部分或所有介面。 外部物件會作為其他物件的用戶端，並在想要使用其中一個包含物件的服務時委派執行。

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**上下文**
</dt> <dd>

在 COM + 中，一組與一或多個 COM 物件相關聯的執行時間屬性，可用來為這些物件提供服務。

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**控制**
</dt> <dd>

最少支援 [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) 介面的可內嵌、可重複使用的 COM 物件。 控制項通常與使用者介面相關聯。 它們也支援與容器的通訊，而且可以由多個用戶端重複使用（視授權準則而定）。

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**控制容器**
</dt> <dd>

藉由執行 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) 介面，支援內嵌控制項的應用程式。

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**控制項屬性**
</dt> <dd>

由控制項本身公開和管理的執行時間屬性。 例如，控制項所使用的字型和文字大小就是控制項屬性。

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**控制物件**
</dt> <dd>

匯總物件內的物件，可控制匯總物件內的哪些介面是公開的，而是私用的。 控制物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面稱為控制 **iunknown**。 對匯總中其他物件的 **IUnknown** 方法的呼叫必須傳遞至控制 **IUnknown**。

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**控制網站**
</dt> <dd>

控制項容器所執行的結構，用於管理控制項的顯示和儲存。 在指定的容器內，每個控制項都有對應的控制網站。

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**資料傳輸物件**
</dt> <dd>

物件，這個物件會執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面，並且包含要透過剪貼簿或拖放作業從某個物件傳送到另一個物件的資料。

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**預設物件處理常式**
</dt> <dd>

以 OLE 提供的 DLL，可作為真實物件之容器應用程式的處理空間中的代理。

您可以使用預設物件處理常式來查看物件的儲存資料，而不需要實際啟用物件。 預設物件處理常式會執行其他工作，例如在物件載入記憶體時，從其快取狀態轉譯物件。

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**相依物件**
</dt> <dd>

COM 物件，通常由另一個物件初始化， (主物件) 。 雖然相依物件的存留期在主物件的存留期內可能只有意義，但主機物件不會做為相依物件的控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 。 相反地，當物件的存留期 (藉由管理物件完全控制) 的參考計數時，物件就是匯總物件。

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**直接存取模式**
</dt> <dd>

可以開啟儲存物件的兩種存取模式之一。 在直接模式中，所有變更都會立即認可至根儲存物件。

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document 物件**
</dt> <dd>

可以在原生或外部的框架（例如瀏覽器）中，顯示其資料的一或多個就地啟用資料檢視，同時保留其使用者介面的完整控制權的 OLE 檔。 除了執行一般的 OLE 檔和就地啟用介面之外，檔物件還必須執行 [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)，而且每一個視圖都 (檔視圖物件的格式，) 必須執行 [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview)。

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**檔物件容器**
</dt> <dd>

容器應用程式，能夠顯示一個或多個檔物件的一或多個視圖，以及管理檔案內所有包含的檔物件。 每個檔物件都與一個檔網站相關聯，而每個檔網站都包含一或多個對應至檔物件所支援之視圖的檔視圖網站。 檔物件容器也包含一個容器框架，可處理功能表和工具列的協商以及所包含物件的列舉。

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**檔物件服務器**
</dt> <dd>

能夠提供檔物件的伺服器應用程式。

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**檔網站**
</dt> <dd>

由檔物件容器所執行的用戶端網站，用來管理檔物件的顯示和儲存。 容器中的每個檔物件都有對應的檔網站。

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**檔網站物件**
</dt> <dd>

除了一般的用戶端網站介面 (（例如 [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)) ）之外，還會執行 [**IOLEDOCUMENTSITE**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite)介面的 COM 物件。

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**檔視圖**
</dt> <dd>

檔資料的特定標記法。 單一檔物件可以有一或多個視圖，但是單一檔視圖只能屬於一個檔物件。

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view 物件**
</dt> <dd>

COM 物件，它會執行 [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) 介面並對應至特定的檔查看。 具有多個檔視圖的物件會匯總每個視圖的個別檔視圖物件。

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**檔視圖網站**
</dt> <dd>

由檔網站物件匯總的物件，用於管理檔物件之特定視圖的顯示空間。 在給定的檔網站內，每個檔視圖都有對應的檔視圖網站。

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**檔視圖網站物件**
</dt> <dd>

在檔網站物件中匯總的 COM 物件，並可執行 [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) 介面和（選擇性） [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) 介面。

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**拖放**
</dt> <dd>

使用者使用滑鼠或其他指標裝置將資料移至相同視窗或另一個視窗中的另一個位置的操作。

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**嵌入**
</dt> <dd>

將物件插入複合檔案中，以保留該物件的原生資料格式，並使用其伺服器所公開的工具，在其容器內進行編輯。

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded 物件**
</dt> <dd>

物件，其資料會儲存在複合檔案中，但物件會在其伺服器的進程空間中執行。 預設物件處理常式會在容器應用程式的處理空間中提供實際物件的代理。

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**擴充屬性**
</dt> <dd>

執行時間屬性，例如控制項的位置和大小，使用者會假設該控制項會由控制項公開，但會由容器公開和管理。

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**檔案標記**
</dt> <dd>

以檔案系統中的路徑為基礎的名字。 檔案標記可以用來識別儲存在自己檔案中的物件。 檔案標記是一種 COM 物件，可針對檔案的標記類別支援 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的系統提供的實作為。

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**字型物件**
</dt> <dd>

COM 物件，可透過實 [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) 介面，提供對圖形裝置介面 (GDI) 字型的存取權。

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**格式識別碼**
</dt> <dd>

識別持續性屬性集的 GUID。 也稱為 FMTID。

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**框架**
</dt> <dd>

容器應用程式的一部分，負責以內嵌的 COM 物件或檔物件來協調功能表、快速鍵、工具列和其他共用的使用者介面元素。

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame 物件**
</dt> <dd>

COM 物件，它會執行 [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) 介面和（選擇性） [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) 介面。

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**泛型複合標記**
</dt> <dd>

依序排序的標記集合，開頭為檔案的標記，以提供檔層級路徑，並繼續進行一或多個以整體方式執行的專案名字標記，以唯一的方式識別物件。

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper 函式**
</dt> <dd>

此函式會將呼叫封裝至 OLE SDK 中公開提供的其他函式和介面方法。 Helper 函式是一種便利的方式，可呼叫用來完成一般工作的常用函數和方法呼叫序列。

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**主機物件**
</dt> <dd>

COM 物件，與一或多個其他 COM 物件形成階層式關聯性，稱為相依物件。 通常，主機物件會將相依物件具現化，而且其存在只有在主機物件的存留期內才有意義。 但是，主機物件不會做為相依物件的控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ，也不會直接委派給這些物件的介面實現。

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**
</dt> <dd>

從函式成功傳回時，定義為零的不透明結果控制碼，如果傳回錯誤或狀態資訊，則為非零。

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink 物件**
</dt> <dd>

至少會執行 [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) 介面的 COM 物件，做為目標)  (位於另一個位置的物件連結。 超連結是由四個部分所組成：識別目標位置的標記：目標內位置的字串;目標的易記或可顯示名稱;以及可以包含其他參數的字串。

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**超連結流覽內容**
</dt> <dd>

COM 物件，它會執行 [**IHlinkBrowseCoNtext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) 介面並維護超連結導覽堆疊。 流覽內容物件會管理超連結框架視窗和超連結目標物件的視窗。

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**超連結容器**
</dt> <dd>

藉由執行 [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) 介面，以及容器的物件可以是其他超連結（ [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) 介面）的目標，來支援超連結的容器應用程式。

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**超連結框架物件**
</dt> <dd>

COM 物件，該物件會執行 [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) 介面，並控制框架容器和超連結目標伺服器的超連結的最上層導覽和顯示。

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**超連結網站物件**
</dt> <dd>

COM 物件，它會執行 [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) 介面並提供其超連結容器的標記或介面識別碼。 其中一個超連結網站可以提供多個超連結。

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**超連結目標物件**
</dt> <dd>

COM 物件，它會執行 [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) 介面並提供其標記、易記名稱，以及其他超連結物件將用來導覽的其他資訊。

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in 參數**
</dt> <dd>

由函式或介面方法的呼叫端所配置、設定和釋放的參數。 呼叫的函式不會修改 in 參數。

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out 參數**
</dt> <dd>

一開始由函式或介面方法的呼叫端配置的參數，並視需要由呼叫的進程進行設定、釋放和重新配置。

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**就地啟用**
</dt> <dd>

使用伺服器所提供的工具，在其容器的視窗內編輯內嵌的物件。 連結化物件不支援就地啟用;它們一律是在伺服器的視窗中進行編輯。

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**同進程伺服器**
</dt> <dd>

實作為 DLL 的伺服器，會在用戶端的進程空間中執行。

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**實例**
</dt> <dd>

配置給其記憶體或持續性的物件。

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**介面**
</dt> <dd>

一組語義相關的函式，可提供 COM 物件的存取權。 每個 OLE 介面都會定義一個合約，讓物件可以根據元件物件模型 (COM) 進行互動。 雖然 OLE 提供許多介面，但大部分的介面也可以由開發人員設計 OLE 應用程式的開發人員來實行。

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**(IID 的介面識別碼)**
</dt> <dd>

全域唯一識別碼 (GUID) 與介面相關聯。 有些函式會接受 Iid 做為參數，以允許呼叫端指定應該傳回的介面指標。

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**專案標記**
</dt> <dd>

以識別容器中物件的字串為基礎的標記。 專案專案識別碼可以識別出小於檔案的物件（包括複合檔案中的内嵌物件）或虛擬物件 (例如試算表中的資料格範圍) 。

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**發 牌**
</dt> <dd>

COM 的功能，可控制物件的建立。 授權物件只能由獲得授權使用的用戶端建立。 授權是透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 介面在 COM 中執行，並支援可在執行時間傳遞的授權金鑰。

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**連結化物件**
</dt> <dd>

建立或載入連結的 COM 物件時，所建立的 COM 物件。 Link 物件是由 OLE 提供，並會執行 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) 介面。

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**連結化物件**
</dt> <dd>

其來來源資料實際上位於其最初建立位置的 COM 物件。 只有表示來源資料的標記法和適當的呈現資料會保存在複合檔案中。 對連結來源所做的變更會自動反映在連結的物件中。

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**連結來源**
</dt> <dd>

連結化物件來源的資料。 連結來源可能是檔案或檔案的一部分，例如檔案內選取的儲存格範圍 (也稱為虛擬物件) 。

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**載入狀態**
</dt> <dd>

物件的資料結構載入至記憶體並可供用戶端進程存取之後的狀態。

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**本機伺服器**
</dt> <dd>

實作為的跨進程伺服器。EXE 應用程式在與用戶端應用程式相同的電腦上執行。

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**鎖**
</dt> <dd>

指標，也可能是在執行中的物件上遞增的參考計數。 OLE 定義了兩種類型的鎖定，可保留在物件上：強式和弱式。 若要執行強式鎖定，伺服器必須同時維持指標和參考計數，如此一來，物件才會在記憶體中保持「鎖定」狀態，直到伺服器呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)為止。 若要執行弱式鎖定，伺服器只會維護物件的指標，讓其他進程可以終結物件。

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**編組**
</dt> <dd>

跨執行緒或進程界限封裝和傳送介面方法呼叫。

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**媒體類型**
</dt> <dd>

MIME 的延伸模組，可在用戶端與物件之間進行資料格式的協商。

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME 內容類型**
</dt> <dd>

MIME 的延伸模組，可在用戶端與物件之間進行資料格式的協商。

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**多用途網際網路郵件延伸 (MIME)**
</dt> <dd>

一種網際網路通訊協定，最初開發的目的是為了允許跨異類網路、電腦和電子郵件環境的豐富內容交換電子郵件訊息。 在實務上，MIME 也是由非郵件應用程式採用和延伸。

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**綽號**
</dt> <dd>

實 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的物件。 標記可做為唯一識別 COM 物件的名稱。 與路徑在檔案系統中識別檔案的方式相同，標記會識別目錄命名空間中的 COM 物件。

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**標記類別**
</dt> <dd>

[**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker)介面的實作為。 系統提供的標記類別包括檔案的名字、專案的名字、泛型複合標記、反標記、指標的標記，以及 URL 的名字。

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**標記用戶端**
</dt> <dd>

使用標記來取得其他應用程式所管理之物件的介面指標的應用程式。

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**標記提供者**
</dt> <dd>

此應用程式可讓提供者識別其所管理的物件，讓其他應用程式可以存取這些物件。

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**命名空間延伸模組**
</dt> <dd>

處理 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)、 [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)和 [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview)的同進程 COM 物件，有時稱為命名空間延伸模組介面。 您可以使用命名空間延伸模組來擴充 shell 的命名空間，或建立個別的命名空間。 [主要使用者] 是 [Windows 檔案總管] 和 [一般檔案] 對話方塊。

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**原生資料**
</dt> <dd>

OLE 伺服器應用程式在編輯内嵌物件時所使用的資料。

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**物件**
</dt> <dd>

在 OLE 中，程式設計結構會將定義和配置的資料和功能，同時封裝成單一單位，而且只會透過程式設計結構的介面來進行公用存取。 COM 物件至少必須支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面，此介面會在使用時維持物件的存在，並提供物件其他介面的存取權。

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**物件狀態** 
</dt> <dd>

其容器中的複合檔案物件和負責物件建立的應用程式之間的關聯性：主動、被動、已載入或執行中。 被動式物件儲存在磁片上或資料庫中，且物件未選取或作用中。 在載入狀態中，物件的資料結構已載入至記憶體中，但無法供編輯等作業使用。 執行中的物件都已載入，並可供所有作業使用。 現用物件正在執行具有可見使用者介面的物件。

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**物件類型名稱**
</dt> <dd>

儲存為註冊資料庫中物件之可用資訊一部分的唯一識別碼字串。

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**Ole**
</dt> <dd>

Microsoft 以物件為基礎的技術，可跨進程與電腦界限共用資訊與服務。

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**跨進程伺服器**
</dt> <dd>

實作為的伺服器。EXE 應用程式，它會在其用戶端的進程之外執行，不論是在同一部電腦或遠端電腦上。

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out 參數**
</dt> <dd>

Out 參數是由呼叫的函式所配置，且由呼叫端釋放。

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**被動狀態**
</dt> <dd>

當 COM 物件儲存 (磁片或資料庫) 中時，該物件的狀態。 未選取或使用中的物件。

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**持續性屬性**
</dt> <dd>

可以持續儲存為儲存物件（例如檔案或目錄）一部分的資訊。 持續性屬性會分組為可顯示及編輯的屬性集。

持續性屬性與使用 OLE 控制項和自動化技術建立之物件的執行時間屬性不同，它們可用來影響系統行為。 [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant)結構會定義所有有效的持續性屬性類型，而 **VARIANT** 結構會定義所有有效的執行時間屬性類型。

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**持續性儲存體**
</dt> <dd>

將檔案或物件儲存在像是檔案系統或資料庫等媒體中，如此一來，當檔案關閉之後再重新開啟時，物件和其資料就會保存下來。

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**圖片物件**
</dt> <dd>

COM 物件，可透過執行 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 介面，提供對 GDI 影像的存取。

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**指標標記**
</dt> <dd>

將介面指標對應至記憶體中之物件的標記。 大部分的名字標記會識別可持續儲存的物件，而指標標記會識別無法進行的物件。 它們允許這類物件參與標記系結作業。

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**簡報資料**
</dt> <dd>

容器用來顯示內嵌或連結化物件的資料。

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**主要動詞**
</dt> <dd>

與使用者在物件上執行的最常見或慣用操作相關聯的動作。 主要動詞一律定義為系統註冊資料庫中的動詞零。 在物件上按兩下，即可執行物件的主要動詞。

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**財產**
</dt> <dd>

與物件相關聯的資訊。 在 OLE 中，屬性分為兩種類別：執行時間屬性和持續性屬性。 執行時間屬性通常會與控制項物件或其容器相關聯。 例如，背景色彩是由控制項容器所設定的執行時間屬性。 持續性屬性與儲存的物件相關聯。

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**屬性框架**
</dt> <dd>

顯示控制項一或多個屬性頁的使用者介面機制。 OLE 控制項執行時間系統會提供屬性框架的標準實作為，可使用 [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper 函數進行存取。

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**屬性識別碼**
</dt> <dd>

四位元組帶正負號的整數，識別屬性集內的持續性屬性。

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**屬性頁**
</dt> <dd>

COM 物件，其具有屬於使用者介面一部分、由控制項實作為一部分的 CLSID，並且可讓您查看和設定控制項的屬性。 屬性頁物件會執行 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 介面。

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**屬性頁面網站**
</dt> <dd>

顯示內容頁的屬性框架內的位置。 屬性框架會執行 [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) 介面，其中包含的方法可管理控制項所提供的每個屬性頁的網站。

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**屬性集**
</dt> <dd>

與持續儲存之物件相關聯之屬性的邏輯相關群組。 若要建立、開啟、刪除或列舉一或多個屬性集，請執行 [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) 介面。 如果您使用複合檔案，您可以使用 OLE 的此介面執行，而不是自行執行。

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**屬性集儲存體**
</dt> <dd>

保存屬性集的 COM 儲存物件。 屬性集儲存區是與儲存物件相關聯和管理的相依物件。

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**屬性工作表**
</dt> <dd>

一或多個物件的一組屬性頁。

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**代理**
</dt> <dd>

介面特定物件，可封裝該介面的參數，以準備遠端方法呼叫。 Proxy 會在寄件者的位址空間中執行，並與接收者位址空間中的對應存根進行通訊。

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy 管理員**
</dt> <dd>

在標準封送處理中，管理單一物件之所有介面 proxy 的 proxy。

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**虛擬物件**
</dt> <dd>

檔或内嵌物件的一部分，例如試算表中的資料格範圍，可以是 COM 物件的來源。

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**參考計數**
</dt> <dd>

保留物件的每個介面指標的計數，以確保在釋放物件的所有參考之前，不會終結物件。

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**相對的名字**
</dt> <dd>

指定物件相對於另一個物件之位置的指定位置的名字。 相對的標記類似于相對路徑，例如。 \\備份 \\ 報表。舊的。

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**遠端伺服器**
</dt> <dd>

從用戶端應用程式使用它在不同電腦上執行的伺服器應用程式，它會實作為 EXE。

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**恢復**
</dt> <dd>

捨棄自上次認可變更或開啟物件的儲存體之後，對物件所做的任何變更。

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**根儲存物件**
</dt> <dd>

檔中最外層的儲存物件。 根儲存物件可以包含其他的嵌套儲存和資料流程物件。 例如，複合檔案會儲存在磁片上，作為根儲存物件內的一系列儲存體和資料流程物件。

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**正在執行狀態**
</dt> <dd>

COM 物件的伺服器應用程式執行時的狀態，而且可以存取其介面並接收變更的通知。

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**正在執行物件資料表 (的 ROT)**
</dt> <dd>

每一部電腦上可全域存取的資料表，這些資料表會追蹤處於執行中狀態的所有 COM 物件（可由標記識別）。 在資料表中，「標記提供者」會將物件註冊，以遞增物件的參考計數。 在可以終結物件之前，必須先從資料表釋放其標記。

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**執行時間屬性**
</dt> <dd>

與控制項物件或其容器相關聯的離散狀態資訊。 執行時間屬性有三種類型：環境屬性、控制項屬性和擴充屬性。

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**自我註冊**
</dt> <dd>

伺服器可以執行自己的登錄作業的進程。

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**伺服器應用程式**
</dt> <dd>

可以建立 COM 物件的應用程式。 容器應用程式接著可以內嵌或連結至這些物件。

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**靜態物件**
</dt> <dd>

物件，其中只包含標記法，沒有原生資料。 容器可以將靜態物件視為連結或內嵌的物件，但不可能編輯靜態物件。

例如，可能會導致靜態物件中斷連結化物件的連結（也就是伺服器應用程式無法使用），或使用者不想再更新連結化物件。

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**儲存物件**
</dt> <dd>

執行 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 介面的 COM 物件。 儲存體物件包含嵌套的儲存物件或資料流程物件，它會在單一檔案中產生相當於目錄/檔案結構的專案。

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream 物件**
</dt> <dd>

實作為 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 介面的 COM 物件。 資料流程物件類似于目錄/檔案系統中的檔案。

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**結構化儲存體**
</dt> <dd>

OLE 的技術，可將複合檔案儲存在原生檔案系統中。

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**存根**
</dt> <dd>

當函式或介面方法的參數跨進程界限封送處理時，存根是介面特定的物件，可 unpackages 已封送處理的參數並呼叫所需的方法。 Stub 會在接收者的位址空間中執行，並與寄件者位址空間中的對應 proxy 進行通訊。

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**存根管理員**
</dt> <dd>

管理單一物件的所有介面存根。

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**同步呼叫**
</dt> <dd>

函式呼叫，在函式傳回之前，不允許執行呼叫進程中的進一步指示。

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**系統登錄**
</dt> <dd>

Windows 所支援資訊的全系統儲存機制，其中包含有關系統和其應用程式（包括 OLE 用戶端和伺服器）的資訊。

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**交易存取模式**
</dt> <dd>

可以開啟儲存物件的兩種存取模式之一。 在交易模式中開啟時，變更會儲存在緩衝區中，直到根儲存物件認可其變更為止。

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**類型資訊**
</dt> <dd>

類型程式庫所提供之物件類別的相關資訊。 為了提供型別資訊，COM 物件會實 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面。

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**制式資料傳輸**
</dt> <dd>

透過「剪貼簿」、「拖放」或「自動化」來傳送資料的模型。 符合此模型的物件會執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面。 此模型取代了 DDE (動態資料交換) 。

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**送**
</dt> <dd>

將已傳送至跨進程界限的 proxy 解壓縮參數。

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**(URL) 的通用資源定位器**
</dt> <dd>

萬維網的識別碼，用於網際網路上的物件名稱和位置。 OLE 提供一個標記類別，也就是一個 URL 名字，可使用它來將用戶端系結至 URL 所識別的物件。

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL 標記**
</dt> <dd>

以通用資源定位器為基礎的名字， (URL) 。 用戶端可以使用 URL 標記系系結至位於網際網路上的物件。 系統提供的 URL 標記類別支援同步和非同步系結。

</dd> </dl>

 

 