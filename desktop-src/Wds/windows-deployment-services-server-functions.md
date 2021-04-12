---
title: Windows 部署服務伺服器函數
description: 下列函式會與 Windows 部署服務 PXE 伺服器 API 搭配使用。
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3852ecfd3e51d6375ca8d566f78d019e733808ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372535"
---
# <a name="windows-deployment-services-server-functions"></a>Windows 部署服務伺服器函數

下列函式會與 Windows 部署服務 PXE 伺服器 API 搭配使用。



| 函式                                                           | 描述                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | 傳回用戶端要求的非同步結果。                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | 將 DHCP 選項附加至回復封包。                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | 將 DHCP 選項附加至回復封包。                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | 從 DHCP 封包捕獲選項值。                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | 從 DHCP 封包的 [廠商專屬資訊] 欄位中，抓取 (43) 的選項值。                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | 將回應封包初始化為 DHCP 回復封包。                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | 驗證封包是否為 DHCP 封包。                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | 傳回 PXE 伺服器的相關資訊。                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | 配置要與 [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) 函數傳送的封包。                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | 釋放 [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) 函式所配置的封包。                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | 關閉 [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) 函數所開啟之提供者的列舉。               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | 啟動已註冊之提供者的列舉。                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | 列舉已註冊的提供者。                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | 釋放 [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) 函式所配置的記憶體。                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | 從提供者動態連結程式庫匯出 (DLL) ，它會初始化提供者，並讓它準備好接收用戶端要求。 |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | 傳回已註冊之提供者清單中所指定提供者的索引。                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | 從用戶端收到要求時呼叫。                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | 向系統註冊提供者。                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | 當 WDS 服務收到服務控制程式代碼時呼叫。                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | 指定提供者的屬性。                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | 呼叫以關閉提供者。                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | 從已註冊的提供者清單中移除提供者。                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | 針對不同的通知事件註冊回呼函數。                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | 將封包傳送至用戶端要求。                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | 將追蹤專案加入至 PXE 記錄檔。                                                                                             |



 

從 Windows 8 和 Windows Server 2012 開始提供下列各項。

| 函式                                                               | 描述                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | 附加 DHCPv6 選項至回復封包。                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | 附加 DHCPv6 選項至回復封包。                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | 從 DHCPv6 封包捕獲選項值。                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | 從選項廠商選擇的選項值抓取 \_ \_ DHCPv6 封包 (17) 欄位。          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | 將回應封包初始化為 DHCPv6 回復封包。                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | 驗證封包是否為有效的 DHCPv6 封包。                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | 傳回 PXE 伺服器的相關資訊。                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | 可讓提供者剖析轉送 FORW 訊息及其嵌套的選項 \_ 轉送訊息 \_ 訊息。 |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | 產生轉送複寫訊息。                                                               |



 

 

 




