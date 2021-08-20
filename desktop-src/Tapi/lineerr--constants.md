---
description: 以下是當叫用線路、位址或呼叫上的作業時，TAPI 可以傳回的錯誤碼清單。
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: 'LINEERR_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e362e942f7819b0e15fcd7e8359c308e931868d57cc9da84acd62fe9e531d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254631"
---
# <a name="lineerr_-constants"></a>LINEERR \_ 常數

以下是當叫用線路、位址或呼叫上的作業時，TAPI 可以傳回的錯誤碼清單。 如需如何判斷特定函式可以傳回哪些錯誤碼的詳細資訊，請參閱個別的函數描述。

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



無法在指定的呼叫上撥打指定的位址。


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



目標呼叫位址已啟用呼叫封鎖。


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ 已配置**
</dt> <dd> <dl> <dt>



因為持續性狀況，導致無法開啟這一行，例如，其他進程會以獨佔方式開啟序列埠。


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



指定的裝置識別碼或線路裝置識別碼，例如在 *dwDeviceID* 參數中無效或超出範圍。


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**
</dt> <dd> <dl> <dt>



[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)中的持有人模式成員無效、在 **LINECALLPARAMS** 中指定的持有人模式無法使用，或呼叫持有人模式無法變更為指定的持有人模式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**
</dt> <dd> <dl> <dt>



已拒絕通話的計費模式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**
</dt> <dd> <dl> <dt>



指定位址上的所有呼叫外觀目前都在使用中。


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**
</dt> <dd> <dl> <dt>



已超過未完成通話完成的最大數目。


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**
</dt> <dd> <dl> <dt>



已達到會議合作物件的最大數目，或無法滿足要求的合作物件數目。


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**
</dt> <dd> <dl> <dt>



可以撥出的位址參數包含服務提供者未處理的撥號控制字元。


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



可以撥出的位址參數包含服務提供者未處理的撥號控制字元。


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



可以撥出的位址參數包含服務提供者未處理的撥號控制字元。


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**
</dt> <dd> <dl> <dt>



可以撥出的位址參數包含服務提供者未處理的撥號控制字元。


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**
</dt> <dd> <dl> <dt>



不支援使用撥號修飾詞 (： ) 。 此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR 已 \_ 中斷連線**
</dt> <dd> <dl> <dt>



呼叫已中斷連線。 此值只會公開給協調 TAPI 2.2 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



應用程式要求的 TAPI 版本或版本範圍，與電話語音 API 的執行和對應的服務提供者不相容或不支援。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



應用程式要求的延伸模組版本範圍可能無效，或對應的服務提供者無法支援此範圍。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



因為內部不一致或格式化問題，所以 TAPI 無法正確讀取或瞭解 Telephon.ini 檔案。 例如，Telephon.ini 檔案的 [ \[ 位置]、[卡片] 或 [ \] \[ \] 國家（地區）] \[ \] 區段可能已損毀或不一致。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ INUSE**
</dt> <dd> <dl> <dt>



線路裝置正在使用中，且目前無法設定、允許加入合作物件、允許呼叫、允許呼叫，或允許傳送呼叫的功能。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**
</dt> <dd> <dl> <dt>



指定的位址無效或不允許。 如果無效，位址包含不正確字元或數位，或目的地位址包含服務提供者不支援的撥號控制字元 (W、@、$ 或？ ) 。 如果不允許，指定的位址可能未指派給指定的行，或對位址重新導向而言無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**
</dt> <dd> <dl> <dt>



指定的位址識別碼無效或超出範圍。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**
</dt> <dd> <dl> <dt>



指定的位址模式無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**
</dt> <dd> <dl> <dt>



指定的位址狀態包含一或多個不是 [**LINEADDRESSSTATE \_ 常數**](lineaddressstate--constants.md)的位。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**
</dt> <dd> <dl> <dt>



應用程式參考的網址類別型無效。 此值只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



指定的代理程式活動無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



叫用這項作業的應用程式是間接交付的目標。 也就是說，TAPI 判斷呼叫的應用程式也是指定媒體類型的最高優先順序應用程式。 此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



指定的代理程式群組資訊無效或包含錯誤。 尚未執行要求的動作。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



應用程式參考了不正確代理程式群組。 此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



指定的代理程式識別碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



使用的代理程式識別碼無效。 此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



代理程式會話狀態無效。 此值只會公開給協調 TAPI 2.2 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



指定的代理程式狀態無效或包含錯誤。 指定之位址的代理程式狀態未進行任何變更。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



應用程式參考的代理程式狀態無效。 此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



應用程式處理 (如 *hLineApp* 參數所指定) 或應用程式註冊控制碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



指定的應用程式名稱無效。 如果應用程式名稱是由應用程式所指定，則會假設字串不包含任何不可顯示的字元，而且會以零結束。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**
</dt> <dd> <dl> <dt>



指定的持有人模式無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**
</dt> <dd> <dl> <dt>



指定的完成無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**
</dt> <dd> <dl> <dt>



指定的呼叫控制碼無效。 例如，控制碼不是 **Null** ，但不屬於指定的行。 在某些情況下，指定的撥號裝置控制碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**
</dt> <dd> <dl> <dt>



指定的呼叫參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**
</dt> <dd> <dl> <dt>



指定的呼叫許可權參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**
</dt> <dd> <dl> <dt>



指定的 select 參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**
</dt> <dd> <dl> <dt>



呼叫的目前狀態不是所要求作業的有效狀態。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**
</dt> <dd> <dl> <dt>



指定的撥號狀態清單無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**
</dt> <dd> <dl> <dt>



在登錄的 [卡片] 區段中的任何專案中，找不到在 *dwCard* 中指定的永久卡識別碼 \[ \] 。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**
</dt> <dd> <dl> <dt>



完成識別碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**
</dt> <dd> <dl> <dt>



會議通話的指定呼叫控制碼無效，或不是會議通話的控制碼。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**
</dt> <dd> <dl> <dt>



指定的諮詢呼叫控制碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**
</dt> <dd> <dl> <dt>



指定的國家或地區代碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



線路裝置對於指定的裝置類別沒有相關聯的裝置，或指定的行不支援指定的裝置類別。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**
</dt> <dd> <dl> <dt>



線路裝置控制碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**
</dt> <dd> <dl> <dt>



撥號參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**
</dt> <dd> <dl> <dt>



指定的數位清單無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**
</dt> <dd> <dl> <dt>



指定的位數模式無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**
</dt> <dd> <dl> <dt>



指定的終止位數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



服務提供者延伸模組版本號碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



*DwFeature* 參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



應用程式叫用了這一行未提供的功能。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**
</dt> <dd> <dl> <dt>



指定的群組識別碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**
</dt> <dd> <dl> <dt>



指定的呼叫、裝置、行裝置或線條控制碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**
</dt> <dd> <dl> <dt>



裝置設定在目前的線路狀態中可能不會變更。 該行可能正由另一個應用程式使用中，或 *dwLineStates* 參數包含一或多個非 [LINEDEVSTATE \_ 常數](linedevstate--constants.md)的位。 **LINEERR \_ INVALLINESTATE** 值也可以指出裝置已中斷連線或服務中斷。 這些狀態是藉由在 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)函式所傳回之 [**LineGetLineDevStatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)結構的 **dwDevStatusFlags** 成員中，將對應于 *LINEDEVSTATUSFLAGS \_ CONNECTED* 和 *LINEDEVSTATUSFLAGS \_ INSERVICE* 值的位設定為0來表示。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**
</dt> <dd> <dl> <dt>



在登錄的 [位置] 區段中的任何專案中，找不到在 *dwLocation* 中指定的永久位置識別碼 \[ \] 。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**
</dt> <dd> <dl> <dt>



指定的媒體清單無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**
</dt> <dd> <dl> <dt>



要監視)  (模式的媒體類型清單包含不正確資訊、指定的媒體類型參數無效，或服務提供者不支援指定的媒體類型。 這一行所支援的媒體類型會列在 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**
</dt> <dd> <dl> <dt>



在 *dwMessageID* 中指定的數位超出 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)結構中 **dwNumCompletionMessages** 成員所指定的範圍。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



參數所指向的參數或結構包含不正確資訊、國家或地區代碼無效、視窗控制碼無效，或指定的轉送清單參數包含不正確資訊。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**
</dt> <dd> <dl> <dt>



公園識別碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**
</dt> <dd> <dl> <dt>



指定的公園模式無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



指定的密碼不正確，而且尚未執行要求的動作。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



應用程式使用了不正確密碼。 此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



一或多個指定的指標參數 (例如 *lpCallList*、 *lpdwAPIVersion*、 *lpExtensionID*、 *lpdwExtVersion*、 *lphIcon*、 *lpLineDevCaps* 和 *lpToneList*) 無效，或 output 參數的必要指標為 **Null**。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**
</dt> <dd> <dl> <dt>



為 *dwPrivileges* 參數設定了不正確旗標或旗標組合。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**
</dt> <dd> <dl> <dt>



指定的速率無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**
</dt> <dd> <dl> <dt>



[**LINEREQUESTMODE**](linerequestmode--constants.md)指標無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**
</dt> <dd> <dl> <dt>



指定的終端機識別碼無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**
</dt> <dd> <dl> <dt>



指定的終端模式參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**
</dt> <dd> <dl> <dt>



不支援超時，或值落在 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)中指定的有效範圍之外。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**
</dt> <dd> <dl> <dt>



指定的自訂色調不代表有效的色調，或由太多頻率所組成，或指定的色調結構未描述有效的色調。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**
</dt> <dd> <dl> <dt>



指定的音調清單無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**
</dt> <dd> <dl> <dt>



指定的色調模式參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**
</dt> <dd> <dl> <dt>



指定的傳輸模式參數無效。


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**
</dt> <dd> <dl> <dt>



LINEMAPPER 是傳入 *dwDeviceID* 參數的值，但是找不到符合 *lpCallParams* 參數中所指定之需求的行。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOCONFERENCE**
</dt> <dd> <dl> <dt>



指定的呼叫不是會議呼叫控制碼或參與者呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NODEVICE**
</dt> <dd> <dl> <dt>



因為自從上一次初始化 TAPI 之後，已從系統移除相關聯的裝置，所以不再接受指定的裝置識別碼（先前為有效的裝置識別碼）。 或者，線路裝置對於指定的裝置類別沒有相關聯的裝置。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NODRIVER**
</dt> <dd> <dl> <dt>



找不到 Tapiaddr.dll 找不到，或指定裝置的電話服務提供者發現其中一個元件遺失或損毀，無法在初始化時偵測到。 應建議使用者使用電話語音主控台修正問題。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



記憶體不足，無法執行操作或無法鎖定記憶體。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



不支援多個實例的電話語音服務提供者在登錄的 [提供者] 區段中列出了一次以上 \[ \] 。 應用程式應通知使用者使用電話語音主控台移除重複的驅動程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



不允許此服務提供者的多個實例。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOREQUEST**
</dt> <dd> <dl> <dt>



目前沒有任何要求暫止于指定的模式，或應用程式不再是指定要求模式的最高優先順序應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOTOWNER**
</dt> <dd> <dl> <dt>



應用程式沒有指定之呼叫的擁有者許可權。


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ NOTREGISTERED**
</dt> <dd> <dl> <dt>



應用程式未註冊為指定要求模式的要求收件者。


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



因為未指定或未知的原因，導致作業失敗。


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



無法使用作業，例如指定的裝置或指定的行。


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**
</dt> <dd> <dl> <dt>



服務提供者目前沒有足夠的頻寬可達指定的速率。


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ 重新初始化**
</dt> <dd> <dl> <dt>



如果已要求 TAPI 重新初始化（例如新增或移除電話語音服務提供者的結果），則 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)、 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)或 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) 要求會因為此錯誤而被拒絕，直到最後一個應用程式使用 [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)) 來關閉其 API (為止，此時新的設定就會生效，而應用程式會再次被允許呼叫 **lineInitialize** 或 **lineInitializeEx**。


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ 重新初始化**
</dt> <dd> <dl> <dt>



應用程式嘗試初始化 TAPI 兩次。


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



有更多的要求擱置中，而不是裝置可以處理的要求。


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



資源不足，無法完成操作。 例如，因為動態資源 overcommitment，所以無法開啟一行。


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



結構的 **dwTotalSize** 成員未指定足夠的記憶體來包含指定結構的固定部分。


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**
</dt> <dd> <dl> <dt>



找不到呼叫切換的目標。 如果命名的應用程式未 \_ 在 [**LineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)的 *DWPRIVILEGES* 參數中以 LINECALLPRIVILEGE 擁有者位開啟同一行，就會發生這種情況。 或者，在媒體模式的提交案例中，沒有任何應用程式在 \_ [**LineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)的 *DWPRIVILEGES* 參數中以 LINECALLPRIVILEGE 擁有者位開啟同一行，而 *dwMediaMode* 參數中指定的媒體類型已在 [**dwMediaModes**](/windows/desktop/api/Tapi/nf-tapi-lineopen)的 *lineOpen* 參數中指定。


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**
</dt> <dd> <dl> <dt>



叫用這項作業的應用程式是間接交付的目標。 也就是說，TAPI 判斷呼叫的應用程式也是指定媒體類型的最高優先順序應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR \_ 未初始化**
</dt> <dd> <dl> <dt>



作業是在任何名為 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) 或 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)的應用程式之前叫用。


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**
</dt> <dd> <dl> <dt>



使用者已取消通話。 此值只會公開給協調 TAPI 2.2 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**
</dt> <dd> <dl> <dt>



包含使用者使用者資訊的字串超過 [**dwUUISendUserUserInfoSize**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)的 **dwUUIAcceptSize**、 **dwUUIAnswerSize**、 **dwUUIDropSize**、 **dwUUIMakeCallSize** 或 **LINEDEVCAPS** 成員中指定的最大位元組數目，或包含使用者資訊的字串太長。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

0xC0000000 至0xFFFFFFFF 的值適用于裝置專屬的擴充功能。 透過0xBFFFFFFF 的值0x80000000 是保留的，而0x00000000 到0x7FFFFFFF 則是用來作為要求識別碼。

如果應用程式收到錯誤訊息，指出它不會明確處理 (（例如裝置專屬延伸模組所定義的錯誤）) ，則應該將錯誤視為 LINEERR \_ OPERATIONFAILED (，以找出未指定原因) 。

叫 \_ 用 TAPI 3.0 的新 LINEERR 常數時，必須使用新的訊息更新 Tapierr.mc 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




