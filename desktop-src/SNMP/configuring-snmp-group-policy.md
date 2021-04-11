---
title: 設定 SNMP 群組原則
description: 如果您使用 Microsoft Management Console (MMC) 嵌入式管理單元來進行群組原則管理適用于 SNMP 的登錄原則設定，則可能存在下列一或多個子機碼。
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093072"
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

 

 