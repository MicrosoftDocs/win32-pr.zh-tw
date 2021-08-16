---
title: SendMessage 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 SendMessage 方法會將訊息傳送至線上商店的外掛程式。
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- sendMessage 方法 Windows Media Player
- sendMessage 方法 Windows Media Player、External 類別
- External class Windows Media Player，sendMessage 方法
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4985bae2f9170bdb0db1d6cdb995f2c14fe813bcb061485c179bc058539e84c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648358"
---
# <a name="externalsendmessage-method"></a>SendMessage 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**SendMessage** 方法會將訊息傳送至線上商店的外掛程式。

## <a name="syntax"></a>語法


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Msg* \[在\]
</dt> <dd>

包含訊息的 **字串**。

</dd> <dt>

*Param* \[在\]
</dt> <dd>

包含與訊息相關聯之參數的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

以非同步方式傳送訊息。 也就是說，這個方法會立即傳回，而不是等候處理訊息。 當外掛程式完成處理訊息時，它會呼叫 [IWMPContentPartnerCallback：： SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) 方法，進而呼叫腳本的 [OnSendMessageComplete](external-onsendmessagecomplete-event.md) 事件處理常式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner：： SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





