---
title: 關於 Windows 篩選平台
description: Windows 篩選平台 (WFP) 是一種網路流量處理平臺，其設計目的是取代 Windows XP 和 Windows Server 2003 網路流量篩選介面。
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969903"
---
# <a name="about-windows-filtering-platform"></a>關於 Windows 篩選平台

Windows 篩選平台 (WFP) 是一種網路流量處理平臺，其設計目的是取代 Windows XP 和 Windows Server 2003 網路流量篩選介面。 WFP 是由一組網路堆疊的勾點所組成，以及一個可協調網路堆疊互動的篩選引擎。

## <a name="the-wfp-components"></a>WFP 元件

### <a name="filter-engine"></a>篩選引擎

核心多層篩選基礎結構（裝載于核心模式和使用者模式）會取代 Windows XP 和 Windows Server 2003 網路子系統中的多個篩選模組。

-   針對填充碼可以提供的任何資料欄位，篩選系統中任何層級的網路流量。
-   藉由在分類期間叫用標注來執行「標注」篩選。
-   將「允許」或「封鎖」動作傳回給叫用它以強制執行的填充碼。
-   提供不同原則來源之間的仲裁。 例如，當應用程式設定為保護任何與其相關的網路流量時，會決定優先順序，但會設定本機防火牆以防止應用程式安全的流量。<br/>

### <a name="base-filtering-engine-bfe"></a>基礎篩選引擎 (BFE) 

控制 Windows 篩選平台操作的服務。 它會執行下列工作。

-   接受平臺的篩選器和其他設定。
-   報告系統目前的狀態，包括統計資料。
-   強制執行在平臺中接受設定的安全性模型。 例如，本機系統管理員可以新增篩選器，但其他使用者只能查看這些篩選器。<br/>
-   將 configuration 設定連接至系統中的其他模組。 例如，IPsec 協商原則會移至 IKE/AuthIP 加密模組，篩選器會移至篩選引擎。<br/>

### <a name="shims"></a>墊片

位於網路堆疊與篩選引擎之間的核心模式元件。 填充碼會對篩選引擎進行分類，藉以進行篩選決定。 以下是可用的填充碼清單。

-   應用層強制 (ALE) 填充碼。
-   傳輸層模組填充碼。
-   網路層模組填充碼。
-   網際網路控制訊息通訊協定 (ICMP) 錯誤填充碼。
-   捨棄填充碼。
-   串流填充碼。

### <a name="callouts"></a>圖說文字

驅動程式所公開並用於特殊篩選的函式集合。 除了「允許」和「封鎖」的基本動作之外，標注還可以修改和保護輸入和輸出網路流量。 如需有關注解的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 檔中的 [Windows 篩選平台標注驅動程式](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) 主題。 WFP 提供內建的標注，可完成下列工作。<br/>

-   執行 IPsec 處理。
-   調整具狀態的篩選行為。
-   執行隱形模式篩選 (不會) 所要求的封包的無訊息放置。
-   控制 TCP 煙囪卸載。
-   與 Teredo 服務互動。

<br/> 篩選引擎可讓協力廠商的標注在其每個核心模式層級進行註冊。<br/>

### <a name="application-programming-interface"></a>應用程式設計介面

一組可供開發人員用來建立和管理網路篩選應用程式的資料類型和函式。 這些資料類型和函式會分組為多個 [API 集合](api-sets.md)。

## <a name="wfp-features"></a>WFP 功能

-   提供封包篩選基礎結構，其中的獨立軟體廠商 (Isv) 可以外掛程式特殊化的篩選模組。
-   適用于 IPv4 和 IPv6。
-   允許資料篩選、修改和重新插入。
-   執行封包和串流處理。
-   除了每個網路介面或每個埠之外，還允許針對每個應用程式、每個使用者和每個連線啟用封包篩選。
-   提供開機時間安全性，直到基礎篩選引擎 (BFE) 可以啟動為止。
-   啟用可設定狀態的連接篩選。
-   處理預先和之後 IPsec 加密的資料。
-   允許整合 IPsec 和防火牆篩選原則。
-   提供原則管理基礎結構，以判斷何時應啟用特定篩選。 這包括來自不同廠商所提供的多個篩選準則的調節衝突需求。
-   處理大部分的封包重組和狀態追蹤。
-   包含一般使用者通知系統，可通知訂閱者對篩選系統的變更。
-   執行可報告系統狀態的列舉函數。
-   使用 net 事件來記錄 IPsec 錯誤和封包卸載。
-   支援網路診斷架構 [ (NDF) helper 類別](/windows/desktop/NDF/extensible-helper-classes)。
-   支援 Winsock API 的 [安全通訊端延伸](/windows/desktop/WinSock/winsock-secure-socket-extensions) 模組，可讓網路應用程式藉由設定 WFP 來保護其流量。
-   在應用層強制執行 (ALE) 層級，只會處理連接中的第一個封包，以最少的方式影響網路效能。
-   整合硬體卸載，其中核心模式注標模組可以使用硬體來執行特定的封包檢查。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WFP 架構](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[WFP 操作](basic-operation.md)
</dt> <dt>

[應用層強制 (ALE) ](application-layer-enforcement--ale-.md)
</dt> <dt>

[IPsec 設定](ipsec-configuration.md)
</dt> <dt>

[WFP 設定](wfp-configuration.md)
</dt> <dt>

[WFP 監視](wfp-monitoring.md)
</dt> <dt>

[WFP API](api-sets.md)
</dt> </dl>

 

