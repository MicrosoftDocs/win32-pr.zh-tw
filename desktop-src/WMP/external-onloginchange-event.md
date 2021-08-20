---
title: OnLoginChange 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnLoginChange 事件
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- External. OnLoginChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0697aff759309bc3a988e6f24a024d5c05bd8ec27dae85921ee09d3847f3dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648738"
---
# <a name="externalonloginchange-event"></a>OnLoginChange 事件

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

當使用者的登入狀態變更或登入嘗試失敗時，就會發生 **OnLoginChange** 事件。

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>可能的值

這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。

## <a name="parameters"></a>參數

處理此事件的函式不會使用任何參數。

## <a name="remarks"></a>備註

每次線上商店的外掛程式呼叫 [IWMPContentPartnerCallback：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)、在 *類型* 參數中傳遞 wmpcnLoginStateChange 時，就會發生此事件。 有時候外掛程式會進行此呼叫，以通知 Windows Media Player 使用者的登入狀態有所變更。 其他時候，外掛程式會進行此呼叫，以通知玩家登入嘗試失敗。 **Notify** 方法的 *pCoNtext* 參數會指定通知是要變更登入狀態，還是嘗試登入失敗。

由於每個呼叫 `Notify(wmpcnLoginStateChange, ...)` 都會導致 Windows Media Player 引發 **OnLoginChange** 事件，因此會呼叫 **OnLoginChange** 事件處理常式，有時是因為登入狀態變更的結果，有時也是因為登入嘗試失敗的結果。 若要判斷使用者目前的登入狀態， **OnLoginChange** 事件處理常式必須呼叫 [External. userLoggedIn](external-userloggedin.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**AttemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**UserLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





