---
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: COM + 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468165"
---
# <a name="com-glossary"></a>COM + 詞彙

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**存取權杖**
</dt> <dd>

物件，描述進程或執行緒的安全性內容。 權杖中的資訊包括與進程或執行緒相關聯之使用者帳戶的身分識別和許可權。 當使用者登入時，系統會將使用者的密碼與儲存在安全性資料庫中的資訊進行比較，以驗證該使用者的密碼。 如果密碼經過驗證，系統會產生存取權杖。 代表此使用者執行的每個處理常式都有此存取權杖的複本。

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID 屬性**
</dt> <dd>

以不可部分完成、一致、隔離且持久的交易處理先鋒創造的縮寫。 這些屬性可確保可預測的行為，將交易的角色強化為全或無的主張，其設計目的是為了在分散式環境中提供一致且可預測的結果，而且可能發生獨立失敗。

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**啟動**
</dt> <dd>

導致建立 COM 物件，以及將有效指標傳回給該物件介面的事件鏈。 在 COM + 中，物件會在其自己的內容中啟動，或在其建立者 (已要求啟始物件) 的物件中啟用。 COM + 服務會根據物件的設定，依賴適當的物件啟用。 在啟用過程中，系統會判斷物件執行所在的內容、初始化內容屬性、檢查存取權限，以及建立安全性身分識別。

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**啟用安全性**
</dt> <dd>

一種安全性保護形式，可決定誰可以啟動伺服器。 「服務控制管理員」會自動套用「啟用安全性」 (特定電腦的 SCM) 。 當收到來自用戶端的要求以啟始物件時，SCM 會根據儲存在登錄中的啟用安全性資訊來檢查要求。 也會檢查是否有相同電腦啟用的啟用安全性。 也稱為 *啟動安全性*。

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**啟用類型**
</dt> <dd>

COM + 應用程式的啟動類別) ，指出應用程式是否會在其用戶端的進程空間中執行 (，取決於它是程式庫或伺服器應用程式，以及應用程式是否以服務的形式執行。

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**活動**
</dt> <dd>

在 COM + 中，包含一或多個交易的邏輯執行緒，並包含組成 COM + 應用程式的元件集合。 每個 COM 物件都屬於一個活動。 物件與活動之間的關聯無法變更。

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**單元模型進程**
</dt> <dd>

具有兩個或多個單一執行緒單元且沒有多執行緒單元的進程。

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**應用程式 proxy**
</dt> <dd>

一組檔案，其中包含可讓用戶端從遠端存取 COM + 伺服器應用程式的註冊資訊。 在用戶端電腦上安裝時，應用程式 proxy 檔案會將伺服器應用程式的相關資訊寫入用戶端電腦。然後，用戶端可以從遠端存取服務器應用程式。

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**認證**
</dt> <dd>

判斷應用程式的呼叫者實際上是誰指出的安全性程式，就是驗證身分識別宣告的真實性。 針對 COM + 應用程式，可以開啟並設定系統管理員的驗證，之後它會以透明的方式在應用程式中運作。

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**授權**
</dt> <dd>

判斷應用程式的呼叫端是否已獲授權可進行要求之動作的安全性程式。

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**快取 resource manager**
</dt> <dd>

資源管理員，可作為另一個 resource manager 的前端，並在本機快取資訊，降低存取基礎資源的成本。 不同于傳統的資源管理員，快取資源管理員不會參與復原，因為它永遠不會永久儲存基礎資料。

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**呼叫安全性**
</dt> <dd>

一種安全性保護形式，可在伺服器啟動之後協助控制伺服器物件方法的存取。

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**COM)  (類別**
</dt> <dd>

一或多個介面的已命名、具體實作為。 COM 類別是以 CLSID 識別，有時也是 ProgID。

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**隱形**
</dt> <dd>

伺服器在代表用戶端進行呼叫時，能夠遮罩自己的身分識別。 啟用「遮蓋」時，您可以透過用戶端的身分識別，在模擬用戶端的伺服器上進行呼叫。 停用遮蓋時，伺服器的呼叫會在伺服器的身分識別下進行。

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM + 應用程式**
</dt> <dd>

元件服務的管理和安全性主要單位。 COM + 應用程式是一組 COM 元件，通常會執行相關的函數。 這些元件會進一步包含 COM 介面和方法。

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM + 應用程式共用**
</dt> <dd>

一種元件服務功能，可讓單一執行緒進程進行調整，也可以協助您藉由提供可處理啟用的其他執行中進程，從單一進程中的失敗中復原。

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM + 應用程式回收**
</dt> <dd>

元件服務功能，可讓您正常關閉與應用程式相關聯的程式並重新啟動，以大幅提升應用程式的整體穩定性。

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM + 類別目錄** 
</dt> <dd>

保存 COM + 設定資料的資料存放區。 COM + 系統管理工作的效能需要讀取和寫入儲存在目錄中的資料。 您只能透過 [元件服務] 系統管理工具或透過 COMAdmin 程式庫來存取目錄。

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM + 事件**
</dt> <dd>

COM + 事件會比對發行者和訂閱者，並透過鬆散結合的事件系統來連接。 發行者會進行方法呼叫來起始事件，而訂閱者會透過事件系統（而不是直接從發行者）接收這些呼叫。 COM + 事件服務會維護接收呼叫的有興趣的訂閱者清單，並在不需要發行者知識的情況下指示這些呼叫。

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM + 程式庫應用程式**
</dt> <dd>

COM + 應用程式，會在建立該應用程式的用戶端進程中執行。 程式庫應用程式可以使用以角色為基礎的安全性，但不支援遠端存取或已排入佇列的元件。

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM + 物件共用**
</dt> <dd>

COM + 提供的自動服務，可讓您將元件的實例設定為在集區中保持作用中狀態，以供任何要求元件的用戶端使用。

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM + 磁碟分割**
</dt> <dd>

一種 COM + 服務，可在單一電腦上建立應用程式的個別執行空間。

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM + 分割集**
</dt> <dd>

在 Active Directory 中對應至特定使用者識別碼的 COM + 分割群組。

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM + 佇列元件**
</dt> <dd>

以 Microsoft Message Queuing 為基礎的 COM + 服務，可提供簡單的方法，以非同步方式叫用和執行元件。 訊息處理可能會發生，而不考慮傳送者或接收者的可用性或可存取性。

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM + 伺服器應用程式**
</dt> <dd>

在其本身的進程中執行的 COM + 應用程式。 伺服器應用程式可支援所有 COM + 服務。

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM + SOAP**
</dt> <dd>

元件服務功能，可讓您將 COM + 應用程式公開為 XML web service。 COM + SOAP 也可讓您使用 XML web service 做為 COM 元件。

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM 元件**
</dt> <dd>

程式碼的二進位單位，其中包含封裝和註冊程式碼，並且會建立 COM 物件。 所有 COM + 應用程式都是由一或多個 COM 元件所組成。

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**認可樹狀結構**
</dt> <dd>

在分散式交易系統中，交易的概念表示，會根據參與分散式交易的個別交易管理員之間的階層式關聯性而定。 包含在該階層中的是與交易管理員相關聯的已登記資源管理員。

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM 物件**
</dt> <dd>

在 COM 程式設計模型中，程式設計結構會同時封裝資料和功能，而這些資料和功能是以單一單位來定義和配置，而只有公用存取是透過程式設計結構的介面。 COM 物件至少必須支援 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面，此介面會在使用時維持物件的存在，並提供物件其他介面的存取權。

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Resource Manager (CRM) 補償**
</dt> <dd>

一種 COM + 功能，可讓非交易式資源參與具有 Microsoft Distributed Transaction Coordinator (DTC) 的兩階段認可交易。 一般而言，Crm 並不提供完整資源管理員的隔離功能，但會寫入記錄檔，以提供交易式不可部分完成性和持久性。

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**元件服務系統管理工具**
</dt> <dd>

使用者介面嵌入式管理單元，可讓系統管理員和開發人員建立、設定和維護 COM + 應用程式，以及管理分散式交易和記憶體常駐資料庫。 [元件服務] 系統管理工具也可以用來在安裝工具的電腦上，用來查看系統事件及管理本機系統服務。

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**概念模型**
</dt> <dd>

COM + 應用程式設計階段的第一個步驟，就是開發人員定義要解決的商務問題，並決定需要哪些元件和服務。

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**併發**
</dt> <dd>

一個以上的交易或進程同時存取相同資料的能力。 COM + 通常會透過同步處理來管理並行。

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**設定的元件**
</dt> <dd>

已安裝至 COM + 應用程式的 COM 元件。 安裝之後，元件會在 COM + 類別目錄內設定，以利用可用的 COM + 服務。

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**上下文**
</dt> <dd>

一組與一或多個 COM 物件相關聯的執行時間屬性，可用來為這些物件提供服務。 每個 COM 物件都會在啟動的單一內容中執行，而不是在相同的公寓) 內 (一律停用。 當物件啟動時初始化、內容屬性，例如資訊安全內容屬性，代表物件的執行時間需求。

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**資料層**
</dt> <dd>

在商務應用程式的三層式架構模型中，可透過仲介層或商務服務層存取的 DBMS 存取層，以及有時透過展示層或使用者服務層來存取的 DBMS 存取層。 資料層是由 (的資料存取元件所組成，而不是原始的 DBMS 連接) 協助資源分享，並允許設定用戶端，而不需要在每個用戶端上安裝 DBMS 程式庫和 ODBC 驅動程式。 也稱為 *資料服務層*。

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**僵局**
</dt> <dd>

在多執行緒應用程式中，當一組執行緒的每個成員正在等候集合的另一個成員時，就會發生執行緒問題。

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**代表團**
</dt> <dd>

一種模擬形式，可授權伺服器代表用戶端進行動作，讓伺服器能夠透過網路模擬用戶端。

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**分散式交易**
</dt> <dd>

牽涉到多個資源管理員的交易，可位於相同或不同的電腦上。

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**分散式交易協調器 (DTC)**
</dt> <dd>

一種系統服務，可管理一或多個系統上分散于兩個或多個資源管理員的交易和交易相關通訊，以確保 ACID 交易的正確性。

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**動態掩蓋**
</dt> <dd>

一種掩蓋形式，其中原始用戶端身分識別會在每次對下游伺服器的方法呼叫上探索為伺服器執行緒存取權杖。 雖然提供的身分識別可動態判斷，但進行這項作業所需的額外負荷可能會大幅增加。 針對 COM + 應用程式，預設設定適用于動態擬呼功能，因為它提供了通常需要在一開始使用模擬的情況下所需的彈性。

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**列舉值物件**
</dt> <dd>

啟用集合中項目的列舉。

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**事件**
</dt> <dd>

物件所辨識的動作，例如按一下滑鼠或按下按鍵，以及您可以撰寫程式碼來回應的動作。

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**事件類別物件**
</dt> <dd>

在 COM + 事件系統中提供持續性記錄的已設定元件，用以描述與這些發行者相關聯的發行者和引發介面。

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**事件方法**
</dt> <dd>

COM + 介面中識別 COM + 事件的方法。 事件方法必須是唯一的名稱，而且只能包含輸入參數。 傳回值必須是 **HRESULT**。

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**事件物件**
</dt> <dd>

COM 物件，可通知一個或多個發生事件的執行緒。 進程內的任何執行緒都可以建立事件物件。

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**例外**
</dt> <dd>

在程式執行期間發生的異常狀況或錯誤，需要在正常控制流程之外執行軟體。

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**故障**
</dt> <dd>

在叢集網路系統中，將超載或失敗的資源（例如伺服器、磁片磁碟機或網路）重新放置到其備份元件的程式。

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**無限制執行緒進程**
</dt> <dd>

具有多執行緒單元且沒有單一執行緒單元的進程。

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**全域認可協調器**
</dt> <dd>

在以 Microsoft Windows 為基礎的分散式交易系統上，認可樹狀結構的根交易管理員。 此協調器會決定要認可或中止指定的交易，而且永遠不會有任何疑慮。

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**類比**
</dt> <dd>

執行緒在安全性內容中執行的能力，與擁有線程的進程不同。 伺服器執行緒會使用代表用戶端認證的存取權杖，並透過此存取權杖存取用戶端可以存取的資源。

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**模擬等級**
</dt> <dd>

用戶端用來授與伺服器特定授權層級的設定，以代表用戶端執行動作。 在 COM + 中，這只能針對 COM + 伺服器應用程式設定。

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**攔截**
</dt> <dd>

針對在給定內容中啟動的物件，處理從內容界限呼叫該物件的程式。 跨內容的呼叫會使用輕量介面 proxy 來處理，而這些 proxy 會處理任何需要的中繼工作，將執行時間環境從容納呼叫者的執行時間環境調整為容納被呼叫端的伺服器。

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**介面**
</dt> <dd>

在以 COM 為基礎的程式設計中，提供 COM 物件存取權的相關公用函式集合。 COM 物件上的介面集合會撰寫一個合約，以指定程式和其他物件如何與 COM 物件互動。

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**介面 proxy**
</dt> <dd>

封裝 (的介面特定物件會封送處理該介面的) 參數，以準備遠端方法呼叫，並 unpackages (拆收) 來自介面存根的傳回值。 Proxy 會在寄件者的位址空間中執行，並與接收者位址空間中的對應存根進行通訊。

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**介面存根**
</dt> <dd>

介面特定的物件，可 unpackages 封送處理的參數、呼叫所需的方法和封裝， (封送處理來自所呼叫方法的) 傳回值。 Stub 會在接收者的位址空間中執行，並與寄件者位址空間中的對應介面 proxy 進行通訊。

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**內建物件**
</dt> <dd>

在交易式階層中，根物件下的任何物件。

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**及時 (JIT) 啟用**
</dt> <dd>

COM + 提供的自動服務，可讓閒置的伺服器資源更有效率地使用。 當元件設定為 JIT 啟用時，COM + 可以停用它的實例，而用戶端仍保留物件的使用中參考。 下次用戶端在物件上呼叫方法時，COM + 會以透明的方式將物件重新開機至用戶端。

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**舊版元件**
</dt> <dd>

已安裝至 COM + 應用程式的未設定元件。

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**聽眾**
</dt> <dd>

COM + 佇列元件服務的架構元素。 接聽程式是 COM 物件，它會開啟與其主機應用程式相關聯的訊息佇列，並等候訊息到達。 當訊息抵達時，接聽程式會分派處理訊息的執行緒。

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**邏輯模型**
</dt> <dd>

COM + 應用程式設計程式中的第二個步驟，概念模型會分成三層架構的邏輯層，如下所示：展示層或使用者服務。中介層或商務服務;和資料層，或資料服務。

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**鬆散結合的事件**
</dt> <dd>

傳送者 (發行者) 和接收者 (訂閱者) 未緊密系結的事件。 在鬆散結合的事件系統中（例如 COM + 事件），來自不同發行者的事件資訊會保存在事件存放區中。 訂閱者會查詢此存放區，並選取要接收的事件。 從事件存放區選取事件資訊會建立訂用帳戶。 當事件發生時，事件系統會在此資料庫中尋找，並尋找感興趣的訂閱者、建立每個感興趣類別的新物件，並在該物件上呼叫方法。

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**編組**
</dt> <dd>

跨執行緒或進程界限封裝和解除封裝介面方法參數的程式，讓遠端程序呼叫得以進行。

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**訊息移動器**
</dt> <dd>

COM + 佇列元件服務的架構元素，會將失敗的訊息移回其輸入佇列，以便重試。

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**中繼事件**
</dt> <dd>

當建立、修改或移除事件類別物件或訂用帳戶時，COM + 事件系統用來通知有興趣的訂閱者的事件種類。

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**方法**
</dt> <dd>

在以 COM 為基礎的程式設計中，COM 物件在接收訊息時所執行的處理常式。

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**中介層**
</dt> <dd>

在商務應用程式的三層式架構模型中，包含商務邏輯和資料規則的圖層。 組成仲介層的元件可以用來強制執行商務規則，例如商務演算法、法律或政府法規，以及資料規則，這些規則是設計用來在特定或多個資料庫中保持一致的資料結構。 因為這些中介層元件未系結至特定的用戶端，所以可供所有應用程式使用，並可隨著回應時間和其他規則的需求移至不同的位置。 也稱為「 *商務服務層* 」或「 *商務邏輯層*」。

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**混合模型進程**
</dt> <dd>

具有多執行緒單元的進程，以及一或多個單一執行緒單元。

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**綽號**
</dt> <dd>

可唯一識別 COM 物件的名稱。 與路徑在檔案系統中識別檔案的方式相同，標記會識別目錄命名空間中的 COM 物件。

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi 檔案**
</dt> <dd>

當您匯出 COM + 應用程式或應用程式 proxy 以便在另一部電腦上安裝時，由 [元件服務] 系統管理工具所建立的檔案。 您可以使用 Windows Installer 將 .msi 檔案安裝在任何 Windows 型用戶端上。

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**多執行緒單元模型**
</dt> <dd>

一個單元模型，在此模型中，進程中已初始化為自由執行緒的所有線程都位於單一單元中。 因此，不需要線上程之間進行封送處理。 執行緒不需要取得和分派訊息，因為 COM 不會在此模型中使用視窗訊息。

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**嵌套交易**
</dt> <dd>

從現有的主要或父系交易界限內起始的次要交易。 在其所有從屬或嵌套交易認可之前，不會認可主要交易。 COM + 不支援嵌套交易。

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**中立的單元模型**
</dt> <dd>

執行緒模型，其中的物件會遵循多執行緒單元的指導方針，但可以在任何類型的執行緒上執行。 中立的單元模型是適用于 COM 元件和 COM + 應用程式的建議執行緒模型。

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**持續性物件**
</dt> <dd>

COM 物件，可在用戶端要求用戶端時儲存其內部狀態，且符合 COM 定義的標準，用戶端可以要求物件在資料存放區之間進行初始化、載入和儲存， (例如一般檔案、結構化儲存體或記憶體) 。 用戶端負責管理物件的持續性資料的儲存位置，而非資料的格式。

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**持續性物件介面**
</dt> <dd>

由持續性物件所執行的 COM 介面。 用戶端會使用持續性物件介面，來告知這些持續性物件的儲存狀態和位置。

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**階段零通知介面**
</dt> <dd>

COM + 介面，可讓應用程式偵測交易何時準備好繼續進行兩階段認可通訊協定，讓它可以執行必要的通知作業，並在作業完成時與交易管理員進行通訊。

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**實體模型**
</dt> <dd>

COM + 應用程式設計程式中的第三個和最後一個步驟，可讓開發人員判斷元件的實際位置，以及如何編寫程式碼。

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**球員**
</dt> <dd>

COM + 佇列元件服務的架構專案，會從佇列中取出訊息，然後載入伺服器物件和標準介面存根，以 unmarshal 資料並叫用伺服器方法。 播放程式會在伺服器端拆收用戶端的安全性內容，然後再叫用伺服器元件，並進行相同的方法呼叫。 除非用戶端元件完成，而且記錄方法的交易呼叫認可，否則播放程式不會播放方法呼叫。

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**展示層**
</dt> <dd>

在商務應用程式的三層式架構模型中，將資料呈現給使用者，並選擇性地允許資料操作和資料輸入的圖層。 展示層的兩個主要使用者介面類別型是傳統的應用程式和 Web 應用程式。 也稱為 *使用者服務層*。

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**主要存取權杖**
</dt> <dd>

描述與進程相關聯之使用者帳戶的安全性內容。

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy 管理員**
</dt> <dd>

在標準封送處理中，管理單一物件之所有介面 proxy 的元件。

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**虛擬物件**
</dt> <dd>

包含的物件類型，例如檔中的使用者選取專案、試算表中的資料格範圍，或文字檔中的字元範圍。 這種類型的物件稱為虛擬物件，因為它不會被視為相異物件，直到使用者標示選取範圍為止。

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**出版商**
</dt> <dd>

事件的寄件者。 在 COM + 事件架構中，發行者會進行方法呼叫來起始事件。

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**佇列標記**
</dt> <dd>

用來啟動已排入佇列之元件的標記。

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**競爭條件**
</dt> <dd>

在多執行緒應用程式中，當多個執行緒存取資料項目但沒有協調時所發生的狀況，可能會導致不一致的結果，視哪個執行緒先到達資料項目而定。 COM 提供一些特別設計來協助避免跨進程伺服器發生競爭情況的函式。

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**答錄機**
</dt> <dd>

COM + 佇列元件服務的架構專案，會將用戶端的安全性內容封送處理到訊息中，並記錄物件的所有方法呼叫。 錄製器是系統提供的 proxy 管理員，可從 COM + 目錄中的 queuable 介面選取介面。

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**資源配置器**
</dt> <dd>

在 COM + 程式設計模型中，會代表進程內的應用程式元件來管理非持久性共用狀態的元件。 資源機類似于資源管理員，但不保證持久性。

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**資源管理員**
</dt> <dd>

管理資料庫、持久訊息佇列或交易式檔案系統中的持續性或持久性資料的服務。 它是知道如何儲存資料並執行嚴重損壞修復的資源管理員。 COM + 伺服器應用程式會使用資源管理員來維護應用程式的持久狀態，例如庫存手邊的記錄、待處理的訂單，以及應收帳款的帳戶。 資源管理員與 Microsoft Distributed Transaction Coordinator (DTC) 合作，以確保應用程式的不可部分完成性和隔離。

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**以角色為基礎的安全性**
</dt> <dd>

Com + 應用程式所提供的 COM + 安全性服務。 角色代表針對 COM + 應用程式所定義的使用者類別，目的是要判斷應用程式資源的存取權限。 開發人員將角色指派給元件、介面和方法。 系統管理員會將使用者指派給適當的角色，讓指定角色內的使用者可以存取指派該角色的任何資源。

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**根物件**
</dt> <dd>

交易的第一個物件，稱為交易的根目錄，且一律放置在新的交易界限內。 交易中只能有一個根物件。 在根物件下，交易式階層中的所有其他物件都稱為內建物件。

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**根交易管理員**
</dt> <dd>

啟動交易之系統上的交易管理員。 在根交易管理員判斷交易狀態 (認可或中止) 之前，交易不會完成。

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**信號**
</dt> <dd>

用來仲裁共用資源存取權的核心物件。

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**服務控制管理員 (SCM)**
</dt> <dd>

管理 Windows 登錄中所有服務的 Microsoft Windows server 進程。

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**共用屬性管理員 (SPM)**
</dt> <dd>

在 Com + 中，您可以用來在伺服器進程內的多個物件之間共用非持續狀態的資源配置器。

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**單一執行緒進程**
</dt> <dd>

只由一個單一執行緒的單元組成的進程，其中只包含一個執行緒。 存留于單一執行緒單元中的所有 COM 物件都只能從屬於該單元的一個執行緒接收方法呼叫。

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**肥皂**
</dt> <dd>

以 XML 為基礎的簡易通訊協定，可在網路上交換結構化和類型資訊。 此通訊協定不包含任何應用程式或傳輸語義，使其具有高度模組化和可擴充性。

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**分割註冊**
</dt> <dd>

對於已經存在的 COM 元件，並在 COM + 服務環境中使用的元件，註冊的註冊相片順序是將註冊的基本 COM 部分儲存在 Windows 登錄中，並使用新的 COM + 服務和屬性 (例如，已排入佇列的元件) 會儲存在 COM + 註冊資料庫中。 每個元件屬性都會儲存在 Windows 登錄或 COM + 註冊資料庫中。 新的 COM 元件會以獨佔方式在 COM + 註冊資料庫中註冊，並在 Windows 登錄中進行一些重複，讓現有的工具可以使用這些元件。

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**狀態**
</dt> <dd>

或相關的系統或進程，可監視它所參與的活動狀態的所有詳細資料。

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**無 國籍**
</dt> <dd>

或相關于參與活動的系統或進程，而不監視其狀態的所有詳細資料。

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**靜態掩蓋**
</dt> <dd>

一種掩蓋形式，其中原始用戶端身分識別可以向下游伺服器呈現一次，並在 proxy 上設定一次原始用戶端身分識別。 此用戶端身分識別會以伺服器執行緒標記的形式呈現，將用於後續的方法呼叫。

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**使用者**
</dt> <dd>

事件的接收者。 在 COM + 事件架構中，訂閱者會收到發行者所發出的呼叫。

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**訂用帳戶物件**
</dt> <dd>

在 COM + 事件系統中，訂閱者所建立的物件，用來要求和管理事件的傳遞。

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**同步**
</dt> <dd>

在 COM + 中，一項服務會從元件流至元件，並禁止多個呼叫者在任何指定時間輸入元件。 同步處理會決定執行緒可以將呼叫分派給物件的時間。

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**三層架構模型**
</dt> <dd>

邏輯設計模型的基本架構，將應用程式的元件分成三個服務層級，如下所示：展示層或使用者服務。中介層或商務服務;和資料層，或資料服務。 這些層級不一定會對應到網路上不同電腦上的實體位置，而是對應到應用程式的邏輯層。

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**緊密結合的活動**
</dt> <dd>

其傳送者 (發行者) 和接收者 (訂閱者) 緊密系結的事件。 在緊密結合的事件系統中，發行者提供了一個介面，可在變更發生時呼叫方法。 訂閱者知道要要求通知的發行者，以及公開的介面。 緊密結合的事件系統需要發行者和訂閱者隨時都在執行。

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**追蹤記錄檔**
</dt> <dd>

由 Microsoft Distributed Transaction Coordinator 自動產生的記錄檔，可顯示與一或多個分散式交易相關的資料。 追蹤記錄檔中的資料範例包括交易識別碼、交易時間和指出交易結果的訊息。

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**交易**
</dt> <dd>

在應用程式處理期間發生一連串相關作業的工作單位。 交易只會執行一次，而且是不可部分完成的，可能是所有工作都已完成，或者都不是。

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**交易網際網路通訊協定 (提示)**
</dt> <dd>

交易網際網路通訊協定是標準的兩階段認可通訊協定，可讓異類交易管理員協調分散式交易，尤其是透過網際網路。 秘訣兩階段認可通訊協定很容易執行，而且獨立于應用程式對應用程式的通訊協定，因此可用於任何應用程式協定，但特別是 HTTP。

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**交易管理員**
</dt> <dd>

在參與分散式交易的每一部電腦上執行的 Microsoft Distributed Transaction Coordinator (DTC) 的一部分，並且管理與認可或中止交易交易相關的活動。

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**交易處理應用程式**
</dt> <dd>

將指定的商務工作自動化的交易作業集合。

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**交易處理系統**
</dt> <dd>

包含電腦硬體和軟體的完整系統，可裝載交易處理應用程式，以執行執行業務所需的例行交易。

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**兩階段認可通訊協定**
</dt> <dd>

只有在分散式交易中使用的通訊協定，可確保交易的結果會在參與交易的所有交易管理員之間保持一致。 通訊協定會在兩個不同的階段中運作，以最後認可或中止交易：第一個階段會評估每個資源管理員的條件，而第二階段則會完成交易。

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**未設定的元件**
</dt> <dd>

尚未在 COM + 目錄中設定的 COM 元件。 未配置的元件無法利用 COM + 服務。

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**下落**
</dt> <dd>

對於 DTC 交易而言，這是一個不透明的資料結構，代表資源管理員的交易管理員位址。

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA 介面**
</dt> <dd>

一組標準的程式設計介面，可讓 COM + 應用程式開發人員存取 XA 相容的資料庫，並建立可與關係資料庫、訊息佇列、交易式檔案和麵向物件資料庫操作的資源管理員。 雖然 Microsoft 不直接支援 XA 通訊協定，但是 Microsoft 支援 OLE 交易與 XA 之間的翻譯工具。

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web service**
</dt> <dd>

為其他應用程式提供資料和服務的應用程式邏輯單位。 應用程式會透過標準 Web 通訊協定（例如 SOAP）存取 XML web service。

</dd> </dl>

 

 
