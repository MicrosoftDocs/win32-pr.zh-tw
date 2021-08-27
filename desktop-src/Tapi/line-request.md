---
description: 傳送 TAPI 線路 \_ 要求訊息，以報告來自另一個應用程式的新要求抵達。
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: 'LINE_REQUEST 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cd49b14aafabfdd4d7ab37c5f2beec1487a08a53385ae8a1439b7443d49cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126228"
---
# <a name="line_request-message"></a>行 \_ 要求訊息

傳送 TAPI **線路 \_ 要求** 訊息，以報告來自另一個應用程式的新要求抵達。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

未使用。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

[**LineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)上所指定之應用程式的註冊實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

新暫止要求的要求模式。 此參數會使用 [**LINEREQUESTMODE \_ 常數**](linerequestmode--constants.md)。

</dd> <dt>

*dwParam2* 
</dt> <dd>

此參數的條件為，如果 *dwParam1* 設為 LINEREQUESTMODE \_ DROP， *dwParam2* 就會包含要求 DROP 的應用程式 *hWnd* 。 否則，就不會使用 *dwParam2* 。

</dd> <dt>

*dwParam3* 
</dt> <dd>

如果 *dwParam1* 設定為 LINEREQUESTMODE \_ DROP，則 *dwParam3* 的低序位字組會包含要求卸載之應用程式所指定的 *wRequestID* 。 否則，就不會使用 *dwParam3* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**行 \_ 要求** 訊息會傳送至已針對對應的要求模式註冊的最高優先順序應用程式。 此訊息指出指定要求模式的輔助電話語音要求抵達。 如果 *dwParam1* 是 LINEREQUESTMODE \_ MAKECALL，應用程式可以使用對應的要求模式來叫用 [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) 來接收要求。 如果 *dwParam1* 是 LINEREQUESTMODE \_ DROP，則訊息會包含要求收件者執行要求所需的所有資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




