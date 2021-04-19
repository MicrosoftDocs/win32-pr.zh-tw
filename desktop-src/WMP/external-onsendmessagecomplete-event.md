---
title: OnSendMessageComplete 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnSendMessageComplete 事件
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- External. OnSendMessageComplete 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977399"
---
# <a name="externalonsendmessagecomplete-event"></a>OnSendMessageComplete 事件

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

當線上商店完成處理訊息時，就會發生 **OnSendMessageComplete** 事件。 探索頁面上的腳本先前藉由呼叫 [External. sendMessage](external-sendmessage.md)傳送訊息。

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>可能的值

這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。

## <a name="parameters"></a>參數

處理此事件的函式具有下列參數。

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*味精*
</dt> <dd>

在 **sendMessage** 的 **Msg** 參數中傳遞的相同字串。

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*參數*
</dt> <dd>

在 **sendMessage** 的 **Param** 參數中傳遞的相同字串。

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*結果*
</dt> <dd>

包含訊息處理結果的 **字串**。 請參閱＜備註＞。

</dd> </dl>

## <a name="remarks"></a>備註

**SendMessage** 方法會呼叫 [IWMPContentPartner：： sendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)，它會以非同步方式傳回。 也就是說，它會在線上商店完成處理訊息之前傳回。 當線上商店完成處理訊息時，它會呼叫 [IWMPContentPartnerCallback：： SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)，進而呼叫腳本的 **OnSendMessageComplete** 事件處理常式。

當線上商店呼叫 **IWMPContentPartnerCallback：： SendMessageComplete** 時，它會在 *bstrResult* 參數中提供結果碼。 Windows Media Player 不會解讀結果碼。 相反地，Windows Media Player 會將結果碼傳遞給 *result* 參數中的 **OnSendMessageComplete** 事件處理常式。

**OnSendMessageComplete** 事件處理常式的 (*Msg*、 *Param*、 *Result*) 的參數都不是由 Windows Media Player 所解讀。 參數只有線上商店才有意義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**SendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner：： SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





