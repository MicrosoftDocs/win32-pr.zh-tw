---
description: 在下表中，基本的電話語音功能是依類別列出。
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: 基本電話語音服務參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974196"
---
# <a name="basic-telephony-services-reference"></a>基本電話語音服務參考

在下表中，基本的電話語音功能是依類別列出。 如果函式指出已在應用程式的回復訊息中完成，則會將函數識別為 [*非同步*](a-tapgloss.md) 。 如果函式一律會立即將其結果傳回給應用程式，則會將函數視為 [*同步*](s-tapgloss.md)。

以下是基本電話語音服務功能的功能群組：

-   [位址格式](#address-formats)
-   [位址](#addresses)
-   [接聽撥入電話](#answering-incoming-calls)
-   [呼叫 Drop 函數](#call-drop-functions)
-   [呼叫控制碼操作](#call-handle-manipulation)
-   [呼叫許可權控制](#call-privilege-control)
-   [撥號狀態和事件](#call-states-and-events)
-   [線路狀態和功能](#line-status-and-capabilities)
-   [行版本協商](#line-version-negotiation)
-   [位置和國家/地區資訊](#location-and-countryregion-information)
-   [進行呼叫](#making-calls)
-   [開啟和關閉行裝置](#opening-and-closing-line-devices)
-   [要求收件者服務](#request-recipient-services)
-   [TAPI 初始化和關機](#tapi-initialization-and-shutdown)
-   [免付費保護支援](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a>TAPI 初始化和關機



| 函式                                     | 描述                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | 初始化 TAPI 行抽象概念，以供叫用應用程式使用。 Synchronous： |
| [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | 關閉應用程式使用 TAPI 的線條抽象化。 Synchronous：               |



 

## <a name="line-version-negotiation"></a>行版本協商



| 函式                                                   | 描述                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | 允許應用程式協調 TAPI 版本以供使用。 Synchronous： |



 

## <a name="line-status-and-capabilities"></a>線路狀態和功能



| 函式                                               | 描述                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | 傳回指定線路裝置的功能。 Synchronous：                                                                                                  |
| [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | 傳回媒體資料流程裝置的設定。 Synchronous：                                                                                                   |
| [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | 傳回指定之開啟行裝置的目前狀態。 Synchronous：                                                                                         |
| [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | 設定指定媒體串流裝置的設定。 Synchronous：                                                                                      |
| [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | 指定應用程式需要通知的狀態變更。 Synchronous：                                                                      |
| [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | 傳回應用程式目前的行和位址狀態訊息設定。 Synchronous：                                                                       |
| [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | 抓取與指定的開啟行、位址或呼叫相關聯的裝置識別碼。 Synchronous：                                                                  |
| [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | 允許應用程式抓取顯示給使用者的圖示。 Synchronous：                                                                                |
| [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | 使指定行裝置的提供者顯示對話方塊，讓使用者能夠設定與線路裝置相關的參數。 Synchronous： |
| [**lineConfigDialogEdit**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | 顯示對話方塊，讓使用者變更線路裝置的設定資訊。 Synchronous：                                                    |



 

## <a name="addresses"></a>位址



| 函式                                             | 描述                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | 傳回位址的電話語音功能。 Synchronous：                           |
| [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | 傳回指定之位址的目前狀態。 Synchronous：                              |
| [**lineGetAddressID**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | 使用替代格式抓取指定位址的位址識別碼。 Synchronous： |



 

## <a name="opening-and-closing-line-devices"></a>開啟和關閉行裝置



| 函式                       | 描述                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | 開啟指定的線路裝置，以提供後續的監視及/或控制行。 Synchronous： |
| [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) | 關閉指定的已開啟行裝置。 Synchronous：                                                        |



 

## <a name="address-formats"></a>位址格式



| 函式                                                 | 描述                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | 轉譯標準格式的位址和可撥出格式的位址。 Synchronous： |
| [**lineSetCurrentLocation**](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | 設定用來做為位址轉譯內容的位置。 Synchronous：                       |
| [**lineSetTollList**](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | 操縱收費清單。 Synchronous：                                                           |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | 傳回位址轉譯功能。 Synchronous：                                            |



 

## <a name="call-states-and-events"></a>撥號狀態和事件



| 函式                                         | 描述                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | 傳回有關呼叫的固定資訊。 Synchronous：                                |
| [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | 傳回指定之呼叫的完整撥號狀態資訊。 Synchronous：       |
| [**lineSetAppSpecific**](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | 設定呼叫資訊結構的應用程式特定欄位。 Synchronous： |



 

## <a name="making-calls"></a>進行呼叫



| 函式                             | 描述                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | 進行輸出呼叫，並傳回它的呼叫控制碼。 非同步： |
| [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)         | 撥打一或多個) 的位址 (部分。 非同步：         |



 

## <a name="answering-incoming-calls"></a>接聽撥入電話



| 函式                         | 描述                             |
|----------------------------------|-----------------------------------------|
| [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | 回答來電。 非同步： |



 

## <a name="toll-saver-support"></a>免付費保護支援



| 函式                                   | 描述                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | 指出來電之前要接聽的環形數。 Synchronous：                   |
| [**lineGetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | 傳回 [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings)要求的最小環形數。 Synchronous： |



 

## <a name="call-privilege-control"></a>呼叫許可權控制



| 函式                                             | 描述                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | 將應用程式的許可權設定為指定的許可權。 Synchronous： |



 

## <a name="call-drop-functions"></a>呼叫 Drop 函數



| 函式                                         | 描述                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | 中斷通話的連線，或放棄進行中的呼叫嘗試。 非同步： |
| [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | 解除配置指定的呼叫控制碼。 Synchronous：                       |



 

## <a name="call-handle-manipulation"></a>呼叫控制碼操作



| 函式                                                   | 描述                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | 交給來電擁有權及/或將應用程式的許可權變更為呼叫。 Synchronous：                                    |
| [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | 將呼叫控制碼傳回給應用程式還沒有控制碼的指定行或位址上的呼叫。 Synchronous： |
| [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | 傳回呼叫控制碼的清單，這些呼叫控制碼屬於與指定為參數的呼叫相同的會議呼叫。 Synchronous：    |



 

## <a name="location-and-countryregion-information"></a>位置和國家/地區資訊



| 函式                                           | 描述                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | 顯示對話方塊，讓使用者變更位置和電話卡資訊。 Synchronous： |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | 抓取撥號規則，以及特定國家/地區的其他相關資訊。 Synchronous：              |



 

## <a name="request-recipient-services"></a>要求收件者服務

下列兩個函式僅用來支援輔助電話語音。



| 函式                                                             | 描述                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | 針對指定的要求模式，將應用程式註冊或取消註冊為要求收件者。 Synchronous： |
| [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | 從電話語音動態連結程式庫取得下一個要求。 Synchronous：                                  |



 

 

 



