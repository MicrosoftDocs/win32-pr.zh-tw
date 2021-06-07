---
description: 所有服務提供者都必須執行基本的電話語音功能。
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: TSPI 基本電話語音功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524152"
---
# <a name="tspi-basic-telephony-functions"></a>TSPI 基本電話語音功能

所有服務提供者都必須執行基本的電話語音功能。 以下是依類別分類的功能清單。 如果函式指出已在應用程式的回復訊息中完成，則會將函數識別為 *非同步* 。 如果函式一律會立即傳回其結果，則函式會被視為 *同步*。

-   [位址](#addresses)
-   [接聽撥入電話](#answering-incoming-calls)
-   [呼叫 Drop 函數](#call-drop-functions)
-   [撥號狀態和事件](#call-states-and-events)
-   [線路狀態和功能](#line-status-and-capabilities)
-   [行版本協商](#line-version-negotiation)
-   [進行呼叫](#making-calls)
-   [開啟和關閉行裝置](#opening-and-closing-line-devices)
-   [電話版本協商](#phone-version-negotiation)
-   [TSP 初始化和關機](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>TSP 初始化和關機



|  函式                                                         |   描述                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | 安裝 TSP。 Synchronous：                              |
| [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | 安裝 TSP。 版本2.0 已淘汰。 Synchronous： |
| [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | 初始化 TSP。 Synchronous：                         |
| [**TSPI \_ providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | 關閉服務提供者。                          |
| [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | 移除 TSP。 Synchronous：                               |
| [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | 移除 TSP。 版本2.0 已淘汰。 Synchronous：    |



 

## <a name="phone-version-negotiation"></a>電話版本協商



|  函式                                                         |   描述                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | 傳回服務提供者在此裝置下可運作的最高 SPI 版本。 |



 

## <a name="line-version-negotiation"></a>行版本協商



|  函式                                                         |   描述                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | 允許應用程式與指定的線路裝置協調使用 TSPI 版本。 Synchronous： |



 

## <a name="line-status-and-capabilities"></a>線路狀態和功能



|  函式                                                         |   描述                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | 傳回指定線路裝置的功能。 Synchronous：                                                                                                  |
| [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | 傳回媒體資料流程裝置的設定。 Synchronous：                                                                                                   |
| [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | 傳回指定之開啟行裝置的目前狀態。 Synchronous：                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | 設定指定媒體串流裝置的設定。 Synchronous：                                                                                      |
| [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | 指定應用程式需要通知的狀態變更。 Synchronous：                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | 抓取與指定的開啟行、位址或呼叫相關聯的裝置識別碼。 Synchronous：                                                                  |
| [**TSPI \_ lineGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | 允許應用程式抓取顯示給使用者的圖示。 Synchronous：                                                                                |
| [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | 使指定行裝置的提供者顯示對話方塊，讓使用者能夠設定與線路裝置相關的參數。 Synchronous： |
| [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | 顯示對話方塊，讓使用者變更線路裝置的設定資訊。 Synchronous：                                                    |



 

## <a name="addresses"></a>位址



|  函式                                                         |   描述                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | 傳回位址的電話語音功能。 Synchronous：                           |
| [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | 傳回指定之位址的目前狀態。 Synchronous：                              |
| [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | 抓取指定行所支援的位址識別碼數目。             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | 使用替代格式抓取指定位址的位址識別碼。 Synchronous： |



 

## <a name="opening-and-closing-line-devices"></a>開啟和關閉行裝置



|  函式                                                         |   描述                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | 開啟指定的線路裝置，以提供後續的監視及/或控制行。 Synchronous： |
| [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | 關閉指定的已開啟行裝置。 Synchronous：                                                        |



 

## <a name="call-states-and-events"></a>撥號狀態和事件



|  函式                                                         |   描述                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | 傳回有關呼叫的固定資訊。 Synchronous：                                |
| [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | 傳回指定之呼叫的完整撥號狀態資訊。 Synchronous：       |
| [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | 設定呼叫資訊結構的應用程式特定欄位。 Synchronous： |



 

## <a name="making-calls"></a>進行呼叫



|  函式                                                         |   描述                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | 進行輸出呼叫，並傳回它的呼叫控制碼。 非同步： |
| [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | 撥打一或多個) 的位址 (部分。 非同步：         |



 

## <a name="answering-incoming-calls"></a>接聽撥入電話



|  函式                                                         |   描述                                                        |
|---------------------------------------------|-----------------------------------------|
| [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | 回答來電。 非同步： |



 

## <a name="call-drop-functions"></a>呼叫 Drop 函數



|  函式                                                         |   描述                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | 中斷通話的連線，或放棄進行中的呼叫嘗試。 非同步： |



 

 

 
