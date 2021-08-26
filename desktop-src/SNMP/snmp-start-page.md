---
title: SNMP 服務
description: Microsoft Windows 簡易網路管理通訊協定 (SNMP) 用來設定遠端裝置、監視網路效能、審核網路使用狀況，以及偵測網路錯誤或不適當的存取。重要事項： Microsoft Windows SNMP API 僅支援最多 SNMPv2C 的通訊協定版本。 它不支援任何較新版本的通訊協定。
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dfb56450edbb6d5f18daa635e30e08e5914eb48fefb28013a66276dbc9a0a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886388"
---
# <a name="snmp-service"></a>SNMP 服務

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

## <a name="purpose"></a>目的

Microsoft Windows 簡易網路管理通訊協定 (SNMP) 用來設定遠端裝置、監視網路效能、審核網路使用狀況，以及偵測網路錯誤或不適當的存取。

> [!IMPORTANT]
> Microsoft Windows SNMP API 僅支援最多 SNMPv2C 的通訊協定版本。 它不支援任何較新版本的通訊協定。

 

## <a name="where-applicable"></a>適用時

SNMP 使用由管理應用程式和代理程式應用程式所組成的分散式架構。 SNMP 服務會實行 SNMP 代理程式。 若要使用 SNMP 服務所提供的資訊，您必須至少有一部執行 SNMP 管理應用程式的主機。 您可以使用協力廠商 SNMP 管理軟體，也可以開發自己的 SNMP 管理軟體應用程式。 下列 Api 適用于此用途：

-   SNMP 管理 API，這組函式可用來快速開發基本的 SNMP 管理系統
-   WinSNMP API，版本2.0，一組用來編碼、解碼、傳送和接收 SNMP 訊息的函數

此外，SNMP 延伸模組代理程式 API 會定義 SNMP 服務與協力廠商 SNMP 延伸代理程式 Dll 之間的介面。 SNMP 公用程式 API 函數可以用來簡化 SNMP 訊息的處理。

## <a name="developer-audience"></a>開發人員對象

上一節所列的 Api 是設計來供 C/c + + 程式設計人員使用。 您必須熟悉 SNMP 和 SNMPv2C，以及網路和網路管理概念的實用知識。

## <a name="run-time-requirements"></a>執行階段需求求

如需有關使用特定功能所需之作業系統的詳細資訊，請參閱該函式之參考頁面的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                | 描述                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [SNMP 的新功能](new-in-snmp.md)<br/>                                                            | SNMP 更新的資訊。<br/>                                                                                                      |
| [簡易網路管理通訊協定 (SNMP)](simple-network-management-protocol-snmp-.md)<br/> | SNMP 的資訊和 API 參考，包括 SNMP 管理 API、SNMP 延伸模組代理程式 API，以及 SNMP 公用程式 API 函式。<br/> |
| [WinSNMP API](snmp-reference.md)<br/>                                                         | Microsoft Windows SNMP 應用程式開發介面 (WinSNMP API) 的資訊和 API 參考。 <br/>                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態主機設定通訊協定 (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[網路管理](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[路由及遠端存取服務](/windows/desktop/RRAS/portal)
</dt> </dl>

 

