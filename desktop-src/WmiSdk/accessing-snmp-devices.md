---
description: 允許用戶端應用程式透過 WMI 存取 SNMP 資訊。
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: 存取 SNMP 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988479"
---
# <a name="accessing-snmp-devices"></a>存取 SNMP 裝置

簡易網路管理通訊協定 (SNMP) 提供者，可讓用戶端應用程式透過 WMI 存取 SNMP 資訊。 [Snmp 提供者](snmp-provider.md)可作為使用 SNMP 進行管理之系統與裝置的閘道。 只有管理或監視電腦必須執行 WMI，因為它可以從任何已啟用 SNMP 的裝置讀取。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

SNMP 管理資訊基底 (MIB) 物件變數可以從中讀取和寫入，而且 SNMP 陷阱可以自動對應至 WMI 事件，這些事件可以針對任何在 MIB 定義的陷阱以外的資料進行任意建立、刪除或更新作業而定義。 WMI 功能的這項功能是標準 SNMP 功能的延伸。 如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。

下列主題中所述的工具是設計來供 Windows 腳本和 C/c + + 程式設計人員使用。 建議您熟悉 WMI、SNMPv1 和 SNMPv2C，以及網路和網路管理概念的實用知識。

如需有關搭配 SNMP 使用 WMI 的詳細資訊，請參閱 [設定 WMI Snmp 環境](setting-up-the-wmi-snmp-environment.md)。

 

 



