---
title: SNMP 的系統檔案
description: 下表說明與 SNMP 服務相關的主要檔案。
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462136"
---
# <a name="system-files-for-snmp"></a>SNMP 的系統檔案

下表說明與 SNMP 服務相關的主要檔案。



| 檔案名稱     | 描述                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | 可執行 Microsoft 定義之 DHCP MIB 的擴充代理程式 DLL。 只安裝在 DHCP 伺服器上。                                                                                                                                 |
| EVNTAGNT.DLL | 將事件記錄檔轉譯為 SNMP 陷阱的 SNMP DLL;也稱為 SNMP 事件轉譯程式。                                                                                                                                       |
| HOSTMIB.DLL  | 執行主機資源 MIB 的擴充代理程式 DLL。                                                                                                                                                                         |
| LMMIB2.DLL   | 執行 LAN Manager MIB-II 的擴充代理程式 DLL。                                                                                                                                                                             |
| MGMTAPI.DLL  | Microsoft SNMP 管理 API 程式庫。 此 API 可讓 SNMP 管理員應用程式「接聽」 SNMP 管理員要求，並將要求傳送至 SNMP 代理程式並接收回應。                                                |
| Mib。站      | MGMTAPI.DLL 所使用的已編譯 MIB 資訊。                                                                                                                                                                                       |
| SNMP.EXE     | SNMP 服務。 這是接收 SNMP 要求並將其傳遞至適當擴充代理程式 DLL 的主要代理程式。                                                                                                        |
| SNMPAPI.DLL  | Snmp 公用程式 DLL （snmp）擴充代理程式 Dll 和管理員應用程式所使用的 DLL。 此 DLL 包含開發延伸模組代理程式 Dll 的架構。                                                                                   |
| SNMPSNAP.DLL | SNMP 設定應用程式，也就是 (MMC) 嵌入式管理單元元件的 Microsoft Management Console。 此嵌入式管理單元會將數個頁面新增至 SNMP 服務的 [內容] 工作表。 如需詳細資訊，請參閱 SNMP 服務的線上說明。 |
| SNMPTRAP.EXE | SNMP 陷阱服務。 接收 SNMP 陷阱，並將其轉送到 SNMP 管理員應用程式。                                                                                                                                              |
| WINSMIB.DLL  | 擴充代理程式 DLL，可執行 Microsoft 定義的 WINS MIB。 只安裝在 WINS 伺服器上。                                                                                                                                 |
| WSNMP32.DLL  | Microsoft [WINSNMP API](winsnmp-api.md) 程式庫。 此 API 可讓 SNMP 管理員應用程式「接聽」 SNMP 管理員要求，並將要求傳送至 SNMP 代理程式並接收回應。                                     |



 

如需詳細資訊，請參閱 [SNMP 管理資訊基礎 (MIB) ](the-snmp-management-information-base-mib-.md)。  (您也可以參考 Windows 2000 資源套件。 ) 

 

 




