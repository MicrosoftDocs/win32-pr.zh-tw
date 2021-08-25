---
title: ALE 層
description: 應用層強制 (ALE) 是由數個篩選層和許多相符的捨棄層所組成。
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9d13c7b5493171caa7216e8f2991e0350b79dd46dca612f241c9446cafa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901008"
---
# <a name="ale-layers"></a>ALE 層

應用層強制 (ALE) 是由數個篩選層和許多相符的捨棄層所組成。 [**篩選層識別碼**](management-filtering-layer-identifiers-.md)中會描述所有 Windows 篩選平台 (WFP) 篩選引擎層級（包括 ALE）。 本主題包含屬於 ALE 之篩選層的詳細描述。

## <a name="resource_assignment"></a>資源 \_ 指派

針對網路系結作業（明確或隱含），會比對 [**FWPM \_ layer \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層的篩選。

如果此層級的篩選準則符合以授權原始通訊端建立，則會設定 [ [**.Fwp \_ 條件 \_ 旗標 \_ 為 \_ 原始 \_ 端點**](filtering-condition-flags-.md) 旗標]。

如果此層級的篩選準則符合以授權混合模式接收，則 [ [**.Fwp \_ 條件 \_ ALE \_ 混合 \_ 模式]**](filtering-condition-identifiers-.md) 欄位將設定為 [SIO RCVALL] \_ 。 如需 SIO RCVALL 的說明 \_ ，請參閱 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)。

> [!Note]  
> 這是唯一可篩選混合模式的層級。

 

如果系結 **()** 期間未指定埠，也就是埠設定為 0 (零) ，則 tcp/ip 堆疊會從動態埠範圍選取埠 (19152 – 65535) 。 選取的埠會在此層級進行分類，而 [ [**.Fwp \_ 條件] 旗標為 [ \_ \_ \_ 萬用字元 \_**](filtering-condition-flags-.md) 系結旗標]。

如果未在 [**bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) 呼叫中指定本機位址，則 [本機位址] 欄位會設定為 [ [**.fwp \_ 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)]。

## <a name="auth_listen"></a>驗證 \_ 接聽

[**FWPM \_ layer \_ ALE \_ AUTH AUTH \_ 接聽 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選器會與 TCP [**接聽 ()**](/windows/desktop/api/winsock2/nf-winsock2-listen)呼叫進行比對。

## <a name="auth_recv_accept"></a>驗證 \_ 接收 \_ 接受

[**FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選準則符合 TCP [**接受 ()**](/windows/desktop/api/winsock2/nf-winsock2-accept)呼叫、第一個 UDP 封包 (來自唯一遠端位址/埠元組的單點傳送) ，以及針對第一個輸入的非錯誤 ICMP 訊息 (具有唯一 ICMP 類型、代碼和識別碼的單點傳送) 。

> [!Note]  
> 非 TCP 或 ICMP 的通訊協定會視為 UDP。

 

原始通訊端接收的 TCP 封包會以類似 UDP 流量的方式處理。 也就是說，只會篩選第一個 TCP [**傳送 ()**](/windows/desktop/api/winsock2/nf-winsock2-send) 以及透過原始通訊端的第一個 tcp [**接收 ()**](/windows/desktop/api/winsock/nf-winsock-recv) 。

## <a name="auth_connect"></a>驗證 \_ 連接

[**FWPM \_ layer \_ ALE \_ AUTH AUTH \_ CONNECT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選準則會比對 TCP [**CONNECT ()**](/windows/desktop/api/winsock2/nf-winsock2-connect)呼叫、傳送給唯一遠端位址和埠元組的第一封 UDP 封包，以及具有唯一 ICMP 類型、代碼和識別碼的第一個輸出非錯誤 ICMP 訊息。

> [!Note]  
> 非 TCP 或 ICMP 的通訊協定會視為 UDP。

 

原始通訊端傳送的 TCP 封包會以類似 UDP 流量的方式處理。 也就是說，只會篩選第一個 TCP [**傳送 ()**](/windows/desktop/api/winsock2/nf-winsock2-send) 以及透過原始通訊端的第一個 tcp [**接收 ()**](/windows/desktop/api/winsock/nf-winsock-recv) 。

## <a name="flow_established"></a>流程已 \_ 建立

在 TCP 三向交握成功完成後，會比對 [**FWPM 層的 ALE 流程所建立的篩選準則 \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層。 若為非 TCP 流量，篩選準則會在符合 **驗證 \_ 接收 \_ 接受** 或 **驗證 \_ 連接** 層的篩選準則之後立即符合。

這一層的篩選不應傳回區塊或允許。

注標驅動程式會使用此圖層來追蹤連接狀態，如[Windows 驅動程式套件](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)檔中的詳細說明。

## <a name="resource_release"></a>資源 \_ 版本

[**FWPM \_ 圖層 \_ ALE \_ 資源 \_ 版本 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選準則會在已釋放透過 **資源 \_ 指派** 配置的資源之後進行比對。

## <a name="endpoint_closure"></a>\_結束端點

當連接的 TCP 流量或 UDP 通訊端端點關閉時，會比對 [**FWPM \_ 層 \_ ALE \_ 端點 \_ 關閉 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層的篩選。

## <a name="connect_redirect"></a>連接重新 \_ 導向

[**FWPM \_ layer \_ ALE \_ CONNECT 重新 \_ 導向 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選器可讓您修改遠端位址和埠。 輸出連線會在該連線的持續時間內重新導向。

## <a name="bind_redirect"></a>系結重新 \_ 導向

[**FWPM layer ALE 系結 \_ 重新 \_ \_ \_ 導向 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選器可讓您修改基礎通訊端的本機位址和埠。 在通訊端的存留期內，將會重新導向本機通訊端

## <a name="ale-discard-layers"></a>ALE 捨棄層

針對上面所述的每個 ALE 層，篩選引擎包含相符的捨棄層。 基於記錄目的，注解會使用 ALE 捨棄層。 在其中一個 ALE 篩選層中捨棄的封包和指示，會以相符的 ALE 捨棄層表示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用層強制 (ALE) ](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE 具狀態篩選](ale-stateful-filtering.md)
</dt> <dt>

[ALE 多播/廣播流量](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[ALE Flow 自訂](ale-flow-customization.md)
</dt> <dt>

[TCP 封包流程](tcp-packet-flows.md)
</dt> <dt>

[UDP 封包流程](udp-packet-flows.md)
</dt> <dt>

[Winsock 函數](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**篩選準則旗標**](filtering-condition-flags-.md)
</dt> <dt>

[**篩選每個篩選層級的可用條件**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 