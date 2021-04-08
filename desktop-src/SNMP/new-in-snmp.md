---
title: SNMP 的新功能
description: 從 Windows Vista 開始，SNMP 支援使用 IPv6。
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682978"
---
# <a name="new-in-snmp"></a>SNMP 的新功能

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

從 Windows Vista 開始，SNMP 支援使用 IPv6。 不過，SNMP 僅針對執行 Windows Server 2008 和 Windows Vista 的網路支援 IPv6。 這是因為 SNMP 需要在這些作業系統中提供更新的通訊協定堆疊，才能支援其 IPv6。

除非您的網路只是 Windows Server 2008 網路，否則 IPv6 通訊會失敗，即使在執行舊版 Windows 的電腦上個別安裝 IPv6 通訊協定堆疊也是如此。 例如，在 Windows Server 2003、Windows XP 或 Windows 2000 上執行的 SNMP 代理程式，只會回應對其 IPv4 位址所做的查詢。

 

 