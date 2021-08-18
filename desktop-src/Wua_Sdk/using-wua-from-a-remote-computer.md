---
description: 遠端電腦上的使用者或遠端電腦上執行的應用程式，都可以使用 Windows Update 代理程式 (WUA) API。 不過，遠端使用者或應用程式必須具備系統管理員許可權。
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: 從遠端電腦使用 WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a3780099f6ff9707893c9f7b5d5f2f18be1f6a97c33d9133fef4d5d3497087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737777"
---
# <a name="using-wua-from-a-remote-computer"></a>從遠端電腦使用 WUA

遠端電腦上的使用者或遠端電腦上執行的應用程式，都可以使用 Windows Update 代理程式 (WUA) API。 不過，遠端使用者或應用程式必須具備系統管理員許可權。

下列清單包含遠端使用者和應用程式可用的介面：

-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**ISearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [**IUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [**IUpdateIdentity**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [**IImageInformation**](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [**IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [**ICategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [**IUpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [**IUpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [**IUpdateDownloadContentCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [**IUpdateDownloadContent**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

下列清單包含遠端使用者和應用程式無法使用的介面和屬性：

-   [**IUpdateSession::CreateUpdateDownloader**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [**IUpdateSession::CreateUpdateInstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [**IUpdateSession 的 WebProxy 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   IUpdate (**IsHidden** [**的 IsHidden 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)在遠端呼叫時是唯讀的。 ) 
-   [**IUpdate：： AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [**IWindowsDriverUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [**IUpdateServiceManager：： AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [**IUpdateServiceManager::RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [**IUpdateServiceManager::UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [**IAutomaticUpdate：:P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates：： Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::ShowSettingsDialog**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [**設定IAutomaticUpdates 的屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [**IAutomaticUpdates 的 ServiceEnabled 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

您必須將下列埠和例外狀況新增至 Windows Vista 和 Windows Server 2008 Windows 防火牆設定，才能從遠端呼叫 WUA API。

<dl> <dt>

<span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>例外狀況1
</dt> <dd> <dl> <dd>本機埠：135</dd> <dd>遠端埠：全部</dd> <dd>通訊協定編號：6</dd> <dd>可執行檔：% windir% \\ system32 \\svchost.exe</dd> <dd>服務： rpcss</dd> <dd>遠端許可權：系統管理員</dd> </dl> </dd> <dt>

<span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>例外狀況2
</dt> <dd> <dl> <dd>本機埠：動態 RPC</dd> <dd>遠端埠：全部</dd> <dd>通訊協定編號：6</dd> <dd>可執行檔：% windir% \\ system32 \\dllhost.exe</dd> <dd>遠端許可權：系統管理員</dd> </dl> </dd> </dl>

下列清單包含可用來設定 Windows 防火牆設定的工具：

-   [具有進階安全性的 Windows 防火牆] 嵌入式管理單元
-   群組原則
-   Netsh advfirewall 命令列工具

如需有關如何使用工具來設定 Windows 防火牆設定的詳細資訊，請參閱[使用具有 Advanced Security Windows 防火牆的開始使用](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10))。

 

 
