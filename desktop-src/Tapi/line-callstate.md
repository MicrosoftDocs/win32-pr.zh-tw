---
description: '\_當指定之呼叫的狀態變更時，就會傳送 TAPI 線路 CALLSTATE 訊息。'
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: 'LINE_CALLSTATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982592"
---
# <a name="line_callstate-message"></a>行 \_ CALLSTATE 訊息

當指定之呼叫的狀態變更時，就會傳送 TAPI **線路 \_ CALLSTATE** 訊息。 一般來說，在呼叫的存留期間，會收到數個這類訊息。 應用程式會收到此訊息的新來電通知;新的呼叫處於供應專案 *狀態。* 應用程式可以使用 [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) 來取得有關目前通話狀態的詳細資訊。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

呼叫的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

新的通話狀態。 此參數必須是下列其中一個 [**LINECALLSTATE \_ 常數**](linecallstate--constants.md)。



| dwParam1                                                                                                                                                                                             | 意義                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ 忙碌**</dt> </dl>                         | *dwParam2* 包含忙碌模式的詳細資料。 此參數會使用其中一個 [**LINEBUSYMODE \_ 常數**](linebusymode--constants.md)。<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ 已連線**</dt> </dl>          | *dwParam2* 包含連接模式的詳細資料。 此參數會使用其中一個 [**LINECONNECTEDMODE \_ 常數**](lineconnectedmode--constants.md)。<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_ 撥號**</dt> </dl>             | *dwParam2* 包含撥號音模式的詳細資料。 此參數會使用其中一個 [**LINEDIALTONEMODE \_ 常數**](linedialtonemode--constants.md)。<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**LINECALLSTATE \_ 供應專案**</dt> </dl>             | *dwParam2* 包含連接模式的詳細資料。 此參數會使用其中一個 [**LINEOFFERINGMODE \_ 常數**](lineofferingmode--constants.md)。<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* 包含有關特殊資訊模式的詳細資料。 此參數會使用其中一個 [**LINESPECIALINFO \_ 常數**](linespecialinfo--constants.md)。<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE 已 \_ 中斷連線**</dt> </dl> | *dwParam2* 包含有關中斷連線模式的詳細資料。 此參數會使用其中一個 [**LINEDISCONNECTMODE \_ 常數**](linedisconnectmode--constants.md)。<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

撥號狀態相關資訊。 請參閱 *dwParam1*。

> [!Note]  
> 在 *延遲* 回應適當的情況下，請使用 LINEDISCONNECTMODE \_ TEMPFAILURE。 *封鎖* 回應是適當的，請使用 \_ 封鎖 LINEDISCONNECT。 如需詳細資訊，請參閱 [**LINEDISCONNECTMODE \_ 常數**](linedisconnectmode--constants.md)。

 

如果 *dwParam1* 是 LINECALLSTATE \_ CONFERENCED， *DwParam2* 會包含主旨 *hConfCall* 為其成員之會議父呼叫的 *hCall* 參數。 如果在 *dwParam2* 中指定的呼叫之前，應用程式不會將它視為父會議呼叫 (*hConfCall*，則應用程式必須在此訊息的結果中執行此動作。 如果應用程式沒有會議之父呼叫的控制碼 (因為它先前在該控制碼上呼叫 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ，) *dwParam2* 會設定為 **Null**。

</dd> <dt>

*dwParam3* 
</dt> <dd>

如果為零，此參數表示應用程式的呼叫許可權不會變更。

如果是非零值，它會指定應用程式的呼叫許可權。 這會發生在下列情況中：當應用程式第一次提供此呼叫的控制碼時， (1) ; (2) 當應用程式是呼叫切換的目標時 (即使應用程式已經是呼叫) 的擁有者也一樣。 此參數會使用下列其中一個 [**LINECALLPRIVILEGE \_ 常數**](linecallprivilege--constants.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此訊息會傳送至任何具有呼叫控制碼的應用程式。 程式 **行 \_ CALLSTATE** 訊息也會通知應用程式，以監視其他應用程式所建立之輸出呼叫的存在和狀態，或 (使用者手動（例如，在連結的手機裝置) 上）。 這類呼叫的撥號狀態會反映未 *提供* 之呼叫的實際狀態。 藉由檢查撥號狀態，應用程式可以判斷呼叫是否為需要回答的輸入呼叫。

具有未知撥號狀態的 **行 \_ CALLSTATE** 訊息可以傳送至監視應用程式，因為成功 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)、 [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)、 [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)、 [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)、 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)、 [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)或 [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) 已由另一個應用程式所要求的結果。 在提出要求的應用程式的同時，若要求 [**的 \_ 作業 (成功) ，該行上**](line-reply.md) 的任何監視應用程式都會傳送 **該行 \_ CALLSTATE** (未知的) 訊息。 **\_ CALLSTATE** 訊息，指出新產生之呼叫的「實際」撥號狀態，會使用服務提供者所提供的資訊，在之後不久的要求和監視應用程式) 傳送 (。

**一行 \_ CALLSTATE** (未知的) 訊息只會在 [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)讓呼叫被解析成三向會議時，才會傳送到監視應用程式。

為了回溯相容性，較舊的應用程式在 *DWPARAM2* LINECALLSTATE CONFERENCED 訊息時，不需要任何特定的值 \_ 。 因此，TAPI 會在 *dwParam2* 中傳遞父呼叫 *hConfCall* ，不論接收訊息的應用程式 API 版本為何。 在服務提供者所起始的會議通話案例中，繼承應用程式並不知道父呼叫已成為電話會議，除非它會以自發的方式檢查其他資訊 (例如，呼叫 [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)) 。

無法停用此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ 回復**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




