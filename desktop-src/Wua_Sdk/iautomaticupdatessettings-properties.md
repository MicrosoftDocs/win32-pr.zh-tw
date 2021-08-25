---
description: IAutomaticUpdatesSettings 介面會定義下列屬性。
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: IAutomaticUpdatesSettings 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6995264aebed44e8cb21e3880268a1488157ed5085645e5232feaa94a8786eed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897148"
---
# <a name="iautomaticupdatessettings-properties"></a>IAutomaticUpdatesSettings 屬性

[**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)介面會定義下列屬性。



| 屬性                                                                                 | 描述                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | 取得和設定如何通知使用者有關自動更新事件的通知。                              |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | 取得布林值，指出自動更新設定是否為唯讀。         |
| [**必要**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | 取得布林值，指出群組原則是否需要自動更新服務。 |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | 取得和設定自動更新安裝或卸載更新的星期幾。    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | 取得和設定自動更新安裝或卸載更新的時間。                |



 

> [!Note]  
> Windows 8、Windows 8.1、Windows Server 2012 和 Windows Server 2012 R2 僅提供有限的 [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)和 [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)支援。 如果電腦已透過群組原則設定為使用排程的安裝日期和時間，則 **ScheduledInstallationDay** 和 **ScheduledInstallationTime** 屬性會傳回此排程的日期和時間。 如果電腦尚未透過群組原則設定， **ScheduledInstallationDay** 和 **ScheduledInstallationTime** 屬性會傳回預設值和不可靠的值。 如果您嘗試修改這些作業系統上的排程安裝日期和時間， **ScheduledInstallationDay** 和 **ScheduledInstallationTime** 似乎會成功，但是沒有任何作用。

 

 

 



