---
description: 補充線服務函式依類別列于下列主題中。
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: 補充線服務功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992456"
---
# <a name="supplementary-line-service-functions"></a>補充線服務功能

補充線服務函式依類別列于下列主題中。 如果函式會將回復訊息中的完成指出至應用程式，則會將函式識別為 [*非同步*](a-tapgloss.md) 。 如果函式一律會立即將其結果傳回給應用程式，則會將函數視為 [*同步*](s-tapgloss.md)。

以下是補充行服務功能的功能群組：

-   [代理程式](#agents)
-   [應用程式優先順序](#application-priority)
-   [持有人模式和費率](#bearer-mode-and-rate)
-   [呼叫接受和重新導向](#call-accept-and-redirect)
-   [呼叫完成](#call-completion)
-   [通話會議](#call-conference)
-   [來電轉接](#call-forwarding)
-   [通話保留](#call-hold)
-   [撥打公園](#call-park)
-   [撥打取貨](#call-pickup)
-   [拒絕呼叫](#call-reject)
-   [來電轉接](#call-transfer)
-   [數位監視和收集](#digit-monitoring-and-gathering)
-   [產生 inband 數位和音調](#generating-inband-digits-and-tones)
-   [進行呼叫](basic-telephony-services-reference.md)
-   [媒體控制項](#media-control)
-   [媒體監視](#media-monitoring)
-   [代理](#proxies)
-   [服務品質](#quality-of-service)
-   [將資訊傳送給遠端當事人](#sending-information-to-remote-party)
-   [服務提供者管理](#service-provider-management)
-   [設定電話通話的終端機](#setting-a-terminal-for-phone-conversations)
-   [語氣監視](#tone-monitoring)

另外還有 [其他](#miscellaneous) 補充線服務功能。

## <a name="bearer-mode-and-rate"></a>持有人模式和費率



| 函式                                       | 描述                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | 要求現有呼叫的呼叫參數變更。 Synchronous： |



 

## <a name="media-monitoring"></a>媒體監視



| 函式                                     | 描述                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | 啟用或停用指定之呼叫的媒體模式通知。 Synchronous： |



 

## <a name="digit-monitoring-and-gathering"></a>數位監視和收集



| 函式                                       | 描述                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | 啟用或停用指定之呼叫的數位偵測通知。 Synchronous： |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | 在呼叫上執行已緩衝的數位收集。 Synchronous：                  |



 

## <a name="tone-monitoring"></a>語氣監視



| 函式                                     | 描述                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | 指定要在指定的呼叫上偵測的色調。 Synchronous： |



 

## <a name="media-control"></a>媒體控制項



| 函式                                           | 描述                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | 設定 media control 的呼叫媒體資料流程。 Synchronous：                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | 在 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) 結構中，設定指定之呼叫的媒體模式 (s) 。 Synchronous： |



 

## <a name="generating-inband-digits-and-tones"></a>產生 Inband 數位和音調



| 函式                                         | 描述                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | 在呼叫上產生 inband 位數。 Synchronous：               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | 在呼叫上產生一組指定的聲 inband。 Synchronous： |



 

## <a name="call-accept-and-redirect"></a>呼叫接受和重新導向



| 函式                             | 描述                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | 接受提供的呼叫，並開始發出兩個呼叫者 (回電) 和呼叫方 (環形) 的警示。 非同步： |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | 將供應專案呼叫重新導向至另一個位址。 非同步：                                              |



 

## <a name="call-reject"></a>拒絕呼叫



| 函式                     | 描述                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | 中斷通話的連線，或放棄進行中的呼叫嘗試。 非同步： |



 

## <a name="call-hold"></a>通話保留



| 函式                         | 描述                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | 放置指定的呼叫以進行硬保留。 非同步： |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | 抓取保留的呼叫。 非同步：                  |



 

## <a name="securing-calls"></a>保護呼叫的安全



| 函式                                 | 描述                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | 保護現有的呼叫免于受到其他事件的干擾，例如資料連線上的呼叫等候嗶聲。 非同步： |



 

## <a name="call-transfer"></a>來電轉接



| 函式                                             | 描述                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | 準備指定的呼叫，以傳送至其他位址。 非同步：                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | 傳送針對傳送到另一個呼叫所設定的呼叫，或進入三向會議。 非同步： |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | 將來電轉接給另一方。 非同步：                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | 使用目前在諮詢上的呼叫來交換主動呼叫。 非同步：                              |



 

## <a name="call-conference"></a>通話會議



| 函式                                                         | 描述                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | 準備指定的呼叫，以新增另一個合作物件。 非同步：                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | 準備新增合作物件到現有的會議通話，方法是將會議通話置於保存狀態，然後建立可稍後新增至會議通話的諮詢通話。 非同步： |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | 將諮詢通話新增至現有的會議通話。 非同步：                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | 從會議通話中移除合作物件。 非同步：                                                                                                                                                |



 

## <a name="call-park"></a>撥打公園



| 函式                         | 描述                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | 在另一個位址公園指定的來電。 非同步： |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | 抓取暫停的呼叫。 非同步：               |



 

## <a name="call-forwarding"></a>呼叫轉送



| 函式                           | 描述                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | 設定或取消呼叫轉送要求。 非同步： |



 

## <a name="call-pickup"></a>撥打取貨



| 函式                         | 描述                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | 在指定的目的地位址收取通話警示，並傳回所挑選呼叫的呼叫控制碼 ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) 也可用於呼叫等候) 。 非同步： |



 

## <a name="sending-information-to-remote-party"></a>將資訊傳送給遠端當事人



| 函式                                                   | 描述                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | 釋出使用者的使用者資訊，允許系統以新資訊覆寫此儲存體。 非同步： |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | 在指定的呼叫上，將使用者資訊傳送給遠端方。 非同步：                                |



 

## <a name="call-completion"></a>呼叫完成



| 函式                                         | 描述                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | 放置通話完成要求。 非同步：  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | 取消通話完成要求。 非同步： |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>設定電話通話的終端機



| 函式                                   | 描述                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | 指定要路由指定之行、位址事件或呼叫媒體串流事件的終端機裝置。 非同步： |



 

## <a name="application-priority"></a>應用程式優先順序



| 函式                                         | 描述                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | 抓取應用程式的遞交及/或輔助電話語音優先順序資訊。 Synchronous： |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | 設定應用程式的遞交及/或輔助電話語音優先順序。 Synchronous：              |



 

## <a name="service-provider-management"></a>服務提供者管理



| 函式                                           | 描述                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | 安裝電話語音服務提供者。 Synchronous：                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | 顯示服務提供者的 [設定] 對話方塊。 Synchronous： |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | 移除現有的電話語音服務提供者。 Synchronous：          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | 抓取已安裝的服務提供者清單。 Synchronous：         |



 

## <a name="agents"></a>代理程式



| 函式                                                     | 描述                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | 允許應用程式存取與位址相關聯之代理程式處理常式的專屬處理常式特定函式。 非同步： |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | 取得活動清單，應用程式會從該清單中選取代理程式所執行的函式。 非同步：                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | 取得指定線路裝置上支援的代理程式相關功能。 非同步：                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | 取得代理程式群組的清單，代理程式可以在此清單中登入自動呼叫散發者。 非同步：                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | 取得指定位址上代理程式相關的狀態。 非同步：                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | 設定與特定位址相關聯的代理程式活動代碼。 非同步：                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | 設定代理程式用來登入特定位址的代理程式群組。 非同步：                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | 設定與特定位址相關聯的代理程式狀態。 非同步：                                                                |



 

## <a name="proxies"></a>Proxy



| 函式                                       | 描述                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | 由已註冊的 proxy 要求處理常式用來產生 TAPI 訊息。 Synchronous：  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | 表示已註冊的 proxy 處理常式完成 proxy 要求。 Synchronous： |



 

## <a name="quality-of-service"></a>服務品質



| 函式                                                           | 描述                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | 要求現有呼叫的服務參數品質變更。 非同步： |



 

## <a name="miscellaneous"></a>其他



| 函式                                             | 描述                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | 設定 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)結構的 **CallData** 成員。 非同步： |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | 設定當來電未接聽或保留時，使用者所聽到的聲音。 非同步：               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | 設定線路裝置狀態。 非同步：                                                            |



 

 

 



