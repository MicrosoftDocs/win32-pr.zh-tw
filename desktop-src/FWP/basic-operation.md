---
title: WFP 操作
description: Windows篩選 Platform (WFP) 透過整合下列基底實體層、篩選器、填充碼和標注來執行其工作。
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254ed468b856392477a643ce13f2b609245031f7363865b8c93ccfda64ba9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015386"
---
# <a name="wfp-operation"></a>WFP 操作

Windows篩選 Platform (WFP) 透過整合下列基底實體來執行其工作：*圖層*、*篩選*、*填充* 碼和 *標注*。

## <a name="layers"></a>圖層

*圖層* 是篩選引擎所管理的容器，其函式是用來將篩選組織成集合。 圖層不是網路堆疊中的模組。 每一層都有一個架構，可定義可以加入的篩選器類型。 如需詳細資訊，請參閱 [每個篩選層級可用的篩選準則](filtering-conditions-available-at-each-filtering-layer.md) 。

圖層可能會包含子層以管理衝突的篩選準則需求，例如「封鎖超過1024的 TCP 埠」和「開啟埠1080」。 用於管理篩選衝突的規則是由 [篩選仲裁](filter-arbitration.md)所決定。

WFP 包含一組 [內建的子層](management-filtering-sublayer-identifiers.md)。 每一層都會繼承所有內建的子層。 使用者也可以新增自己的子層。

篩選引擎圖層的清單是在 [**篩選層識別碼**](management-filtering-layer-identifiers-.md)的參考區段主題中提供。

## <a name="filters"></a>篩選

*篩選準則* 是與傳入或傳出封包相符的規則。 此規則會告知篩選引擎要如何處理封包，包括呼叫用來進行深層封包或資料流程檢查的標注模組。 例如，篩選可能會指定「封鎖 TCP 埠大於1024的流量」或「針對未受保護的所有流量呼叫識別碼」。

開機時間篩選器是一種篩選準則，當 TCP/IP 堆疊驅動程式 (tcpip.sys) 啟動時，就會在開機時強制執行。 當 BFE 啟動時，會停用開機時間篩選器。 當叫用 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)時，會設定 [**FWPM \_ 篩選 \_ 旗標 \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)旗標，將篩選標示為開機時間。

執行時間篩選準則是在 BFE 開始之後強制執行的篩選。 執行時間篩選準則可以是靜態、動態或持續性，取決於建立的方式。 如需不同類型的執行時間篩選和其存留期的詳細資訊，請參閱 [物件管理](object-management.md) 。

## <a name="shims"></a>墊片

*填充碼* 是一種核心模式元件，可根據篩選引擎層分類來進行篩選決定。 每個填充碼會針對一或多個圖層進行分類。 例如，傳輸層模組填充碼會根據輸入傳輸層、輸出傳輸層和 ALE 連線以及流程第一個封包的 Receive-Accept 層進行分類。

當封包、資料流程和事件跨越網路堆疊時，填充碼會將它們剖析以解壓縮資料條件和值，然後呼叫篩選引擎以針對指定層中的篩選進行評估。 篩選引擎可能會叫用一或多個標注做為分類的一部分。 填充碼會根據篩選引擎所執行的分類結果，執行實際的封包、資料流程和事件的卸載。

## <a name="callouts"></a>圖說文字

注 *標是驅動* 程式所公開的一組函式，用於特製化篩選。 它們是用來執行封包的分析和操作，例如病毒掃描、家長監護掃描是否有不當的內容，以及用於監視工具的封包資料剖析。 某些標注（例如網路位址轉譯 (NAT) 驅動程式）已內建在作業系統中。 其他（例如 HTTP 家長監護）或入侵偵測系統 (識別碼) 注標，可由獨立軟體廠商 (Isv) 提供。 當對應的標注篩選準則在指定的圖層符合時，篩選引擎會叫用注標函數。

您可以在任何核心模式的 WFP 層註冊標注。 標注可以傳回 ( 「封鎖」、「允許」的動作，以及在執行資料流程檢查時「延遲」、「需要更多資料」、「卸載連線」 ) ，而且可以修改和保護輸入和輸出網路流量。

當標注已向篩選引擎註冊之後，它就可以接收要處理的網路流量。 流量可能是封包、串流或事件，視層而定。 應用程式或防火牆代理程式會藉由新增動作為「標注」且其標注識別碼為該注標識別碼的篩選，來將流量傳遞至標注。 標注可以指示篩選引擎將「區塊」或「允許」傳回填充碼。 標注也可以傳回「繼續」，以允許其他篩選器處理封包。

一個注標驅動程式可能會公開多個標注。

您必須使用 [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) 將標注新增 (，並使用 [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) 註冊 (，才能使用它。 在建立參考標注的篩選之前，必須先呼叫 **FwpmCalloutAdd0** 。 必須先呼叫 FwpsCalloutRegister，然後 WFP 才能在符合標注篩選準則時叫用標注。 依預設，篩選器會將已加入但尚未向篩選引擎註冊的參考標注視為「封鎖」篩選準則。 呼叫 **FwpmCalloutAdd0** 和 FwpsCalloutRegister 的順序並不重要。 持續性的注標只需要加入一次，而且必須在每次執行標注的驅動程式開始時註冊 (例如，在重新開機) 之後。

## <a name="classification"></a>分類

分類是將篩選套用到網路流量 (封包、串流或事件) 的程式，以便判斷該流量的「允許」或「封鎖」結果。 針對一個封包、串流或事件，每一層都有一個分類呼叫。

在分類期間， (的屬性（例如，封包、串流或事件的來源位址) ）會與在叫用分類的層級篩選準則上設定的篩選準則進行比較。 找到相符專案時，就會使用 [篩選仲裁](filter-arbitration.md) 演算法來判斷分類程式的結果。

由填充碼觸發分類要求。

分類動作可以是：

-   允許
-   封鎖
-   圖說文字
    -   允許
    -   封鎖
    -   繼續
    -   推遲
    -   需要更多資料
    -   捨棄連接

## <a name="wfp-operation"></a>WFP 操作

在開機時，只要 TCP/IP 堆疊驅動程式 (tcpip.sys) 啟動，核心模式篩選引擎就會透過開機時間篩選器強制執行系統的安全性原則。

當基礎篩選引擎 (BFE) 在使用者模式中啟動時，系統會將持續性篩選新增至平臺、停用開機時間篩選器，並將通知傳送至使用 [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0)訂閱的這些標注驅動程式。 當 BFE 初始化完成之後，就會立即分派通知。 平臺現在已準備好要註冊的標注，以及要加入的執行時間物件。

從開機到持續篩選的轉換可能會有數秒或甚至更長的時間在緩慢的電腦上。 它是不可部分完成的，因此，如果提供者同時具有開機時間和持續性篩選，則沒有任何作用中的視窗將永遠不會出現。

BFE 啟動之後，防火牆代理程式或自訂防火牆解決方案可以新增執行時間篩選器。 BFE 會處理這些篩選，並將它們傳送至適當的篩選引擎層以進行強制。 BFE 也接受驗證設定，並將這些設定傳送至 (IKE/AuthIP) 的 IPsec 加密模組。 如需詳細資訊，請參閱 [IPsec](ipsec-configuration.md) 設定。

在任何時間，您都可以透過 BFE 所公開的 RPC 介面，在系統中新增、移除或變更篩選和驗證設定。 您可以同樣地新增或移除子層和標注模組。

資料流程：

1.  封包會進入網路堆疊。
2.  網路堆疊會尋找並呼叫填充碼。
3.  填充碼會在特定層級叫用分類進程。
4.  在分類期間，會比對篩選，並採取結果動作。  (參閱 [篩選準則仲裁](filter-arbitration.md)。 ) 
5.  如果在分類程式期間符合任何標注篩選準則，則會叫用對應的標注。
6.  填充碼會作用於最終的篩選決策 (例如，卸載封包) 。

輸出資料流程會遵循類似的模式。

下列主題將進一步描述 WFP 的操作。

-   [TCP 封包流程](tcp-packet-flows.md)
-   [UDP 封包流程](udp-packet-flows.md)
-   [篩選仲裁](filter-arbitration.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件模型](object-model.md)
</dt> <dt>

[物件管理](object-management.md)
</dt> </dl>

 

 