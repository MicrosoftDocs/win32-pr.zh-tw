---
description: 當 WUA 偵測到呼叫端沒有存取介面、方法或屬性的許可權時， \_ 就會傳回 HRESULT E ACCESSDENIED。
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: 在 WUA API 中保護介面、方法和屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973486"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>在 WUA API 中保護介面、方法和屬性

只有屬於下列 Windows 安全性群組的呼叫者，才能存取 Windows Update 代理程式 (WUA) 的某些介面、方法和屬性：

-   系統管理員
-   User
-   進階使用者

當 WUA 偵測到呼叫端沒有存取介面、方法或屬性的許可權時，  \_ 就會傳回 HRESULT E ACCESSDENIED。

系統管理員、使用者和 Power User 安全性群組可以使用下列介面：

-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)和 [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> 如果下列條件成立，則搜尋會失敗：
>
> -   不是系統管理員的使用者，會將 [**IUpdateSession2 介面的 UserLocale 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) 設定為對應于電腦上未安裝之語言的地區設定。
> -   搜尋會使用從 UpdateSession 物件建立的 UpdateSearch 物件。

 

下列下載介面和方法可供系統管理員和 Power 使用者群組使用：

-   [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > 系統管理員、使用者和 power users 都可以呼叫 [**IAutomaticUpdatesSettings2：： CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)。

     

下列安裝介面、方法和屬性可供系統管理員群組使用：

-   [**IAutomaticUpdates：:P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates：： Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**IUpdate 的 IsHidden 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > 系統管理員、使用者和 power users 可以取出 [**IUpdate 的 IsHidden 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)值。 不過，只有系統管理員和 power users 可以設定這些值。

     

-   [**IUpdate：： AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > 系統管理員和 power users 可以呼叫 [**IUpdate 的 AcceptEula 方法**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)。

     

-   [**IAutomaticUpdatesSettings：： Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**IAutomaticUpdatesSettings 的 NotificationLevel 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > 系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings 的 NotificationLevel 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)值。 不過，只有系統管理員可以設定這些值。

     

-   [**IAutomaticUpdatesSettings 的 ScheduledInstallationDay 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > 系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings 的 ScheduledInstallationDay 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)值。 不過，只有系統管理員可以設定這些值。

     

-   [**IAutomaticUpdatesSettings 的 ScheduledInstallationTime 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > 系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings 的 ScheduledInstallationTime 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)值。 不過，只有系統管理員可以設定這些值。

     

-   [**IAutomaticUpdatesSettings2 的 IncludeRecommendedUpdates 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > 系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings2 的 IncludeRecommendedUpdates 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)值。 不過，只有系統管理員可以設定這些值。

     

 

 



