---
title: 設定 SNMP 群組原則
description: 如果您使用 Microsoft Management Console (MMC) 嵌入式管理單元來進行群組原則管理適用于 SNMP 的登錄原則設定，則可能存在下列一或多個子機碼。
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e17bc3b1bac886a19791f57903920a11062072a81577a0a78ab01d461709ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009656"
---
# <a name="configuring-snmp-group-policy"></a>設定 SNMP 群組原則

如果您使用 Microsoft Management Console (MMC) 嵌入式管理單元來進行群組原則管理適用于 SNMP 的登錄原則設定，則可能存在下列一或多個子機碼。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **SNMP** \\ **參數** \\ **ValidCommunities**

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **SNMP** \\ **參數** \\ **PermittedManagers**

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **SNMP** \\ **參數** \\ **TrapConfiguration**

一般來說，只有系統管理員本機群組的成員可以存取下列登錄子機碼，以儲存 SNMP 服務的設定資料：

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP** \\ **參數** \\ **ValidCommunities**

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **SNMP** \\ **參數** \\ **PermittedManagers**

如需以登錄為基礎之原則設定的詳細資訊，請參閱 [關於群組原則](/previous-versions/windows/desktop/Policy/about-group-policy)。

 

 