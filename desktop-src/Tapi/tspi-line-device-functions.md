---
description: 本章節包含電話語音 SPI 中可用線路裝置功能的字母順序清單。
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: TSPI 線路裝置函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849575"
---
# <a name="tspi-line-device-functions"></a>TSPI 線路裝置函式

本章節包含電話語音 SPI 中可用線路裝置功能的字母順序清單。 每個函數的資訊包括下列各項：

-   函數用途的陳述。
-   函數的正確語法。
-   函數參數的描述，包括有效的撥號狀態。
-   函數傳回值的描述。
-   可以包含下列任一項或所有專案的備註區段：當要求完成時，函式和一般撥號狀態轉換的有效撥號狀態清單;服務提供者必須填寫哪些大型資料結構成員的描述，以及哪些成員必須保持不變的值。以及與 TAPI 內的對應函式進行比較。
-   其他函數、訊息或資料結構的參考。
    > [!Note]  
    > 可以執行函式的實際狀態可能會受限於服務提供者的功能。 服務提供者必須在 [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus)結構中設定 **DwCallFeatures** 成員、 [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus)結構中的 **dwAddressFeatures** 成員，以及 [**dwLineFeatures**](/windows/win32/api/tapi/ns-tapi-linedevstatus)結構中的 **LINEDEVSTATUS** 成員，以指示應用程式在該時間點是否允許函數。

     

本節包含下列 TSPI 行裝置函式：

-   [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**TSPI \_ lineAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**TSPI \_ lineBlindTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [TSPI \_ lineDropNoOwner](tspi-linedropnoowner.md)
-   [TSPI \_ lineDropOnClose](tspi-linedroponclose.md)
-   [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ lineGatherDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**TSPI \_ lineGenerateTone**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**TSPI \_ lineGetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**TSPI \_ lineGetCallIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**TSPI \_ lineGetExtensionID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**TSPI \_ lineGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**TSPI \_ lineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**TSPI \_ lineMonitorMedia**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**TSPI \_ lineMonitorTones**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**TSPI \_ linePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**TSPI \_ lineRedirect**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**TSPI \_ lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**TSPI \_ lineRemoveFromConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**TSPI \_ lineSecureCall**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**TSPI \_ lineSendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**TSPI \_ lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI \_ lineSetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**TSPI \_ lineSetCallParams**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**TSPI \_ lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI \_ lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [TSPI \_ lineSetCurrentLocation](tspi-linesetcurrentlocation.md)
-   [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**TSPI \_ lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI \_ lineSetMediaControl**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**TSPI \_ lineSetMediaMode**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineSwapHold**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**TSPI \_ lineUncompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**TSPI \_ lineUnhold**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
