---
description: LINEDEVSTATE \_ 位旗標常數描述各種行狀態事件。
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: 'LINEDEVSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb11959614999ff50e421e0b77c63d1215a831040774e3123b43aa3534a3f853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140061"
---
# <a name="linedevstate_-constants"></a>LINEDEVSTATE \_ 常數

**LINEDEVSTATE \_** 位旗標常數描述各種行狀態事件。

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE \_ 電池**
</dt> <dd> <dl> <dt>



電池計量已大幅改變 (行動電話) 。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



指出，由於使用者或其他情況所做的設定變更，位址的 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) 結構中有一或多個成員已變更。 應用程式應該使用 [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) 來讀取更新的結構。 如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送至 tapi，tapi 會將它傳遞至已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 TAPI 版本的應用程式將會收到指定 LINEDEVSTATE 重新初始化的 **行 \_ LINEDEVSTATE** 訊息 \_ ，要求使用者將其關機並重新初始化，以取得更新的資訊。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ 關閉**
</dt> <dd> <dl> <dt>



另一個應用程式已關閉該行。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



表示已對一或多個與線路裝置相關聯的媒體裝置進行設定變更。 如有需要，應用程式可以使用 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 來讀取更新的資訊。 如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



指出以 [**行 \_ LINEDEVSTATE**](line-linedevstate.md)訊息的 *dwParam2* 參數所包含的完成識別碼所識別的完成呼叫已從外部取消，不再被視為有效 (如果該值是在後續的 [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)呼叫中傳遞，此函式會失敗並出現 LINEERR \_ INVALCOMPLETIONID) 。 如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ 已連線**
</dt> <dd> <dl> <dt>



該行先前已中斷連線，而且現在已連線到 TAPI。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



該行的裝置特定資訊已變更。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE 已 \_ 中斷連線**
</dt> <dd> <dl> <dt>



這行先前已連線，且現在已與 TAPI 中斷連線。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INSERVICE**
</dt> <dd> <dl> <dt>



線路連接到 TAPI。 這種情況發生于第一次啟動 TAPI 時，或是當 TAPI 處於作用中狀態時，會在開關上實際插入和服務。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE \_ 鎖定**
</dt> <dd> <dl> <dt>



線路裝置的鎖定狀態已變更。  (如需詳細資訊，請參閱 \_ 在 [**LINEDEVSTATUSFLAGS \_ 常數**](linedevstatusflags--constants.md)中鎖定 LINEDEVSTATUSFLAGS。 ) 


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE \_ 維護**
</dt> <dd> <dl> <dt>



正在切換的程式列上執行維護。 無法使用 TAPI 線上路裝置上運作。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



訊息等候指示器已關閉。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



訊息等候指示器已開啟。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



線路裝置上的呼叫次數已變更。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



線路裝置上的未完成通話完成次數已變更。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ 開啟**
</dt> <dd> <dl> <dt>



另一個應用程式已開啟該行。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ 其他**
</dt> <dd> <dl> <dt>



以下列出的裝置狀態專案已變更。 應用程式應該檢查目前的裝置狀態，以判斷哪些專案已變更。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



線路在切換時不在服務中，或已實際中斷連接。 無法使用 TAPI 線上路裝置上運作。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ 重新初始化**
</dt> <dd> <dl> <dt>



行裝置設定中的專案已變更。 若要瞭解這些變更 (，因為新線路裝置的外觀) 應用程式應該重新初始化其使用的 TAPI。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ 已移除**
</dt> <dd> <dl> <dt>



指出服務提供者已將裝置從系統中移除 (很可能透過 [控制台] 或類似的公用程式) ，透過使用者動作。 具有此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息通常會緊接在裝置上的 [**行 \_ 關閉**](line-close.md) 訊息後面。 後續在 TAPI 重新初始化之前存取裝置的嘗試，將會導致 LINEERR \_ NODEVICE 傳回給應用程式。 如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE \_ 響鈴**
</dt> <dd> <dl> <dt>



此參數會告知這一行通知使用者。

**TAPI：** 服務提供者會重複傳送包含此常數的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息，以在每個通道週期通知應用程式。 例如，在美國，服務提供者每隔六秒就會傳送一則包含這個常數的訊息。

**TSPI：** 在 POTS 裝置上，服務提供者可以在中央辦公室傳送環形電壓時傳送訊息。 在數位裝置（例如 ISDN）上，如果交換器只產生一個環形要求，服務提供者可能需要合成重複的訊息。 每次重複訊息時，都應該會顯示增加的信號計數，讓「付費儲存」功能正常運作。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



線路裝置的漫遊模式已變更。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE \_ 信號**
</dt> <dd> <dl> <dt>



信號等級已大幅改變 (行動電話) 。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE \_ 終端機**
</dt> <dd> <dl> <dt>



終端機設定已變更。 例如，如果有多個線路裝置共用終端機，就會發生這種情況 (例如，兩行共用電話終端機) 。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



指出，由於使用者或其他情況所做的設定變更， [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) 結構中的一或多個成員已經變更。 應用程式應該使用 [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) 來讀取更新的結構。 如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送至 tapi，tapi 會將它傳遞至已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 TAPI 版本的應用程式將會收到指定 LINEDEVSTATE 重新初始化的 **行 \_ LINEDEVSTATE** 訊息 \_ ，要求使用者將其關機並重新初始化，以取得更新的資訊。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ 關閉**](line-close.md)
</dt> <dt>

[**行 \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




