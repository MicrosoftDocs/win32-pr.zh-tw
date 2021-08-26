---
title: 'SNMP 管理資訊基礎 (MIB) '
description: 管理資訊基底 (MIB) 描述一組受管理的物件。 SNMP 管理主控台應用程式可以操控特定電腦上的物件（如果 SNMP 服務具有支援 MIB 的擴充代理程式 DLL）。
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf3fac2e24b79da3ea7277010da5a3f96e3664416809bc440097f4ec0b1384e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127598"
---
# <a name="the-snmp-management-information-base-mib"></a>SNMP 管理資訊基礎 (MIB) 

管理資訊基底 (MIB) 描述一組受管理的物件。 SNMP 管理主控台應用程式可以操控特定電腦上的物件（如果 SNMP 服務具有支援 MIB 的擴充代理程式 DLL）。

MIB 中的每個受管理物件都有唯一的識別碼。 識別碼包含物件的類型 (例如計數器、string、量測計或位址) 、物件的存取層級 (例如讀取或讀取/寫入) 、大小限制和範圍資訊。

下表包含系統隨附的 Mib 部分清單。 它們會與 SNMP 服務一起安裝在% systemroot% \\ system32 目錄中。 如需 mib 的完整清單，請參閱 Windows 資源套件。



| MIB         | 描述                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCP。MIB    | 包含物件類型的 Microsoft 定義 MIB，可監視遠端主機與 DHCP 伺服器之間的網路流量                        |
| HOSTMIB.MIB | 包含用於監視和管理主機資源的物件類型                                                                                 |
| LMMIB2.MIB  | 涵蓋工作站和伺服器服務                                                                                                           |
| MIB \_ II. MIB | 包含 Management Information Base (MIB-II) ，其提供簡單、可運作的架構和系統來管理以 TCP/IP 為基礎的網際網路 |
| 贏。MIB    | Windows 網際網路名稱服務的 Microsoft 定義 MIB (WINS)                                                                                |



 

**Windows NT：** 一般而言，您可以從支援特定 MIB 的 SNMP 延伸模組代理程式複製 MIB。 Windows NT 4.0 資源套件提供一些額外的 mib。

適用于 MIB 的擴充代理程式 Dll、LAN Manager MIB-II 和主機資源 MIB 會與 SNMP 服務一起安裝。 當安裝其他 Mib 的擴充代理程式 Dll 時，會安裝其個別的服務。 在服務啟動時，SNMP 服務會載入登錄中列出的所有擴充代理程式 Dll。

使用者可以新增其他擴充代理程式 Dll 來執行額外的 Mib。 若要這樣做，他們必須為 SNMP 服務下的新 DLL 新增登錄專案。 他們也必須向 SNMP 管理主控台應用程式註冊新的 MIB。 如需詳細資訊，請參閱管理主控台應用程式隨附的檔。

如需詳細資訊，請參閱 [MIB 名稱樹狀目錄](mib-name-tree.md)。

 

 




