---
title: 關於 SNMP
description: SNMP 使用由管理員和代理程式所組成的分散式架構。
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9b43fe4c6b297f0a6973be425239453bb2f03f551f217f4baf7ed0c55099b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009906"
---
# <a name="about-snmp"></a>關於 SNMP

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

SNMP 使用由管理員和代理程式所組成的分散式架構。 代理程式是從 SNMP 管理員應用程式回應查詢的 SNMP 應用程式。 SNMP 代理程式負責根據 SNMP 管理程式的要求，擷取與更新本機管理資訊。 當發生重大事件或陷阱被觸發時，代理程式也會通知已登錄的管理程式。 管理員是 SNMP 應用程式，可產生 SNMP 代理程式應用程式的查詢，並接收來自 SNMP 代理程式應用程式的陷阱。

在執行 Microsoft Windows XP/Windows 2000/Windows NT 的電腦上，snmp 代理程式是由 snmp 服務 (SNMP.EXE) 所執行。 SNMP 管理員通常是協力廠商 SNMP 管理主控台應用程式。 管理主控台應用程式不需要在與 SNMP 代理程式相同的主機上執行。 若要使用 Microsoft SNMP 服務所提供的資訊，您至少需要一個 SNMP 管理主控台應用程式。 系統包含支援 SNMP 管理主控台應用程式的程式庫，但目前不包含 SNMP 管理主控台應用程式。

 

 