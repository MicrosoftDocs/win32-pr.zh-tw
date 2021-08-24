---
description: 下列函式只會在沒有 &0034 的泛型版本中提供 \# ;&\# 0034; 或 &\# 0034;W&\# 0034; 尾碼。
ms.assetid: 0e51b7a6-53a0-4e92-9bed-f8e4f8ffd5a1
title: 沒有 Unicode 版本的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a5b2444aa32a6ad5b7825c17b31ea66eaacf91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472894"
---
# <a name="functions-without-unicode-versions"></a>沒有 Unicode 版本的函式

下列函式只會在沒有 "A" 或 "W" 尾碼的泛型版本中提供。




| TAPI 函數 | 註解 | 
|---------------|----------|
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaccept"><strong>lineAccept</strong></a> | <em>LpsUserUserInfo</em>所指向的記憶體會被假設為包含用於端對端傳輸的二進位資料。 應用程式必須以準備好傳輸的形式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference"><strong>lineAddToConference</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineagentspecific"><strong>lineAgentSpecific</strong></a> | <em>LpParams</em>所指向的記憶體在應用程式和代理程式處理常式之間是私用的。 應用程式必須以代理程式處理常式延伸模組定義中指定的格式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineanswer"><strong>lineAnswer</strong></a> | <em>LpsUserUserInfo</em>所指向的記憶體會被假設為包含用於端對端傳輸的二進位資料。 應用程式必須以準備好傳輸的形式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineclose"><strong>lineClose</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linecompletecall"><strong>lineCompleteCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer"><strong>lineCompleteTransfer</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider"><strong>lineConfigProvider</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall"><strong>lineDeallocateCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedevspecific"><strong>lineDevSpecific</strong></a> | <em>LpParams</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者延伸模組定義中指定的格式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature"><strong>lineDevSpecificFeature</strong></a> | <em>LpParams</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者延伸模組定義中指定的格式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedrop"><strong>lineDrop</strong></a> | <em>LpsUserUserInfo</em>所指向的記憶體會被假設為包含用於端對端傳輸的二進位資料。 應用程式必須以準備好傳輸的形式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegeneratetone"><strong>lineGenerateTone</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus"><strong>lineGetCallStatus</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls"><strong>lineGetConfRelatedCalls</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls"><strong>lineGetNewCalls</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetmessage"><strong>lineGetMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetnumrings"><strong>lineGetNumRings</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages"><strong>lineGetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linehold"><strong>lineHold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitordigits"><strong>lineMonitorDigits</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitormedia"><strong>lineMonitorMedia</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitortones"><strong>lineMonitorTones</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion"><strong>lineNegotiateAPIVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion"><strong>lineNegotiateExtVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineproxymessage"><strong>lineProxyMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse"><strong>lineProxyResponse</strong></a> | <a href="/windows/win32/api/tapi/ns-tapi-lineproxyrequest"><strong>LINEPROXYREQUEST</strong></a>結構中的欄位一律為 Unicode。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient"><strong>lineRegisterRequestRecipient</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo"><strong>lineReleaseUserUserInfo</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference"><strong>lineRemoveFromConference</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider"><strong>lineRemoveProvider</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesecurecall"><strong>lineSecureCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo"><strong>lineSendUserUserInfo</strong></a> | <em>LpsUserUserInfo</em>所指向的記憶體會被假設為包含用於端對端傳輸的二進位資料。 應用程式必須以準備好傳輸的形式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity"><strong>lineSetAgentActivity</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup"><strong>lineSetAgentGroup</strong></a> | <blockquote>[!Note]<br />系統會忽略組名。</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentstate"><strong>lineSetAgentState</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetappspecific"><strong>lineSetAppSpecific</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcalldata"><strong>lineSetCallData</strong></a> | <em>LpCallData</em>所指向的記憶體是由應用程式所指定的格式或一組協同合作的應用程式所指定。 資料的格式超出 TAPI 的範圍，且不會由 TAPI 轉換。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallparams"><strong>lineSetCallParams</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege"><strong>lineSetCallPrivilege</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice"><strong>lineSetCallQualityOfService</strong></a> | QOS 結構的提供者特定部分中的資料格式已超出 TAPI 的範圍，且不是由 TAPI 轉換。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment"><strong>lineSetCallTreatment</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation"><strong>lineSetCurrentLocation</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus"><strong>lineSetLineDevStatus</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol"><strong>lineSetMediaControl</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetmediamode"><strong>lineSetMediaMode</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetnumrings"><strong>lineSetNumRings</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages"><strong>lineSetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetterminal"><strong>lineSetTerminal</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineshutdown"><strong>lineShutdown</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineswaphold"><strong>lineSwapHold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall"><strong>lineUncompleteCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineunhold"><strong>lineUnhold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneclose"><strong>phoneClose</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonedevspecific"><strong>phoneDevSpecific</strong></a> | <em>LpParams</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者延伸模組定義中指定的格式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdata"><strong>phoneGetData</strong></a> | <em>LpData</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者定義中指定的形式處理資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay"><strong>phoneGetDisplay</strong></a> | <em>LpDisplay</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者定義中指定的形式處理資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetgain"><strong>phoneGetGain</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch"><strong>phoneGetHookSwitch</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetlamp"><strong>phoneGetLamp</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetmessage"><strong>phoneGetMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetring"><strong>phoneGetRing</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages"><strong>phoneGetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetvolume"><strong>phoneGetVolume</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion"><strong>phoneNegotiateAPIVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion"><strong>phoneNegotiateExtVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneopen"><strong>phoneOpen</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetdata"><strong>phoneSetData</strong></a> | <em>LpParams</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者定義中指定的格式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay"><strong>phoneSetDisplay</strong></a> | <em>LpDisplay</em>所指向的記憶體在應用程式與服務提供者之間是私用的。 應用程式必須以服務提供者定義中指定的格式提供資料。 | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetgain"><strong>phoneSetGain</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch"><strong>phoneSetHookSwitch</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetlamp"><strong>phoneSetLamp</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetring"><strong>phoneSetRing</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages"><strong>phoneSetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetvolume"><strong>phoneSetVolume</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneshutdown"><strong>phoneShutdown</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-tapirequestdrop"><strong>tapiRequestDrop</strong></a> | 此函式已過時，無法供應用程式使用。 | 
| <a href="tapirequestmediacall.md"><strong>tapiRequestMediaCall</strong></a> | 此函式已過時，無法供應用程式使用。 | 




 

 

 




