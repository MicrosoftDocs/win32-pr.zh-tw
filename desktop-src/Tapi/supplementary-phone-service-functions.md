---
description: 下列主題依類別列出補充電話語音功能。
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: 補充電話服務功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ee0e32260ac3821fd06e7e8962ab2a6186fb42f1140eb6cd8f705709f2dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861416"
---
# <a name="supplementary-phone-service-functions"></a>補充電話服務功能

下列主題依類別列出補充電話語音功能。 如果函式會將回復訊息中的完成指出至應用程式，則會將函式識別為 [*非同步*](a-tapgloss.md) 。 如果函式一律會立即將其結果傳回給應用程式，則會將函數視為 [*同步*](s-tapgloss.md)。

以下是補充電話語音功能的功能群組：

-   [按鈕](#buttons)
-   [資料區域](#data-areas)
-   [顯示器](#display)
-   [Hookswitch 裝置](#hookswitch-devices)
-   [燈](#lamps)
-   [開啟和關閉手機裝置](#opening-and-closing-phone-devices)
-   [電話初始化和關閉](#phone-initialization-and-shutdown)
-   [電話狀態和功能](#phone-status-and-capabilities)
-   [電話版本協商](#phone-version-negotiation)
-   [環形](#ring)
-   [狀態](#status)

## <a name="phone-initialization-and-shutdown"></a>電話初始化和關閉



| 函式                                       | 描述                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | 初始化 TAPI 電話抽象概念，以供叫用應用程式使用。 Synchronous： |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | 關閉應用程式使用 TAPI 的電話抽象概念。 Synchronous：            |



 

## <a name="phone-version-negotiation"></a>電話版本協商



| 函式                                                     | 描述                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | 允許應用程式協調 TAPI 版本以供使用。 Synchronous： |



 

## <a name="opening-and-closing-phone-devices"></a>開啟和關閉電話裝置



| 函式                         | 描述                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | 開啟指定的電話裝置，並為應用程式提供擁有者或監視器許可權。 Synchronous： |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | 關閉指定的 open phone 裝置。 Synchronous：                                                        |



 

## <a name="phone-status-and-capabilities"></a>電話狀態和功能



| 函式                                       | 描述                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | 傳回指定電話裝置的功能。 Synchronous：                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | 傳回與指定的電話裝置相關聯之指定裝置類別的裝置識別碼。 Synchronous：                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | 允許應用程式抓取顯示給使用者的圖示。 Synchronous：                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | 讓指定電話裝置的提供者顯示對話方塊，讓使用者能夠設定電話裝置的相關參數。 Synchronous： |



 

## <a name="hookswitch-devices"></a>Hookswitch 裝置



| 函式                                         | 描述                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | 將開啟的電話 hookswitch 裝置的勾點狀態設定為指定的模式。 非同步：      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | 查詢 open phone 裝置之 hookswitch 裝置的 hookswitch 模式。 Synchronous：          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | 設定 hookswitch 裝置的說話者在開啟的電話裝置上的音量。 非同步：           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | 傳回 open phone 裝置之 hookswitch 裝置喇叭的磁片區設定。 Synchronous： |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | 設定 hookswitch 裝置在開啟的電話裝置上的 mic 增益。 非同步：                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | 傳回 hookswitch 裝置 mic 的 open phone 增益設定。 Synchronous：              |



 

## <a name="display"></a>顯示



| 函式                                   | 描述                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | 將資訊寫入至開啟的電話裝置的顯示。 非同步： |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | 傳回手機顯示的目前內容。 Synchronous：          |



 

## <a name="ring"></a>環形



| 函式                             | 描述                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | 根據指定的響鈴模式響鈴開啟的電話裝置。 非同步： |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | 傳回已開啟之手機裝置的目前響鈴模式。 Synchronous：    |



 

## <a name="buttons"></a>按鈕



| 函式                                         | 描述                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | 設定與手機裝置上的按鈕相關聯的資訊。 非同步： |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | 傳回與手機裝置上的按鈕相關聯的資訊。 Synchronous：   |



 

## <a name="lamps"></a>燈



| 函式                             | 描述                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | 以指定的燈光源模式燈亮著指定的開啟電話裝置上的燈燈。 非同步： |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | 傳回指定燈的目前燈泡模式。 Synchronous：                           |



 

## <a name="data-areas"></a>資料區域



| 函式                             | 描述                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | 將資料緩衝區下載至電話裝置中的指定資料區域。 非同步：      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | 將電話裝置中特定資料區域的內容上傳到緩衝區。 Synchronous： |



 

## <a name="status"></a>狀態



| 函式                                                 | 描述                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | 指定應用程式想要收到通知的狀態變更。 Synchronous： |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | 傳回應用程式想要收到通知的狀態變更。 Synchronous：   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | 傳回開啟的電話裝置的完整狀態。 Synchronous：                         |



 

 

 



