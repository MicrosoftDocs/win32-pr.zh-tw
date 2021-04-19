---
description: '\_當電話裝置的狀態變更時，TAPI 會將電話狀態訊息傳送至應用程式。'
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: 'PHONE_STATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985732"
---
# <a name="phone_state-message"></a>電話 \_ 狀態訊息

當電話裝置的狀態變更時，TAPI 會將 **電話 \_ 狀態** 消息傳送至應用程式。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPhone* 
</dt> <dd>

手機裝置的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟手機裝置時提供的應用程式回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已變更的電話狀態。 此參數會使用其中一個 [**PHONESTATE \_ 常數**](phonestate--constants.md)。

</dd> <dt>

*dwParam2* 
</dt> <dd>

詳細說明狀態變更的電話狀態相關資訊。 如果在 *dwParam1* 中設定了多個旗標，則不會使用這個參數，因為多個狀態專案已變更。 應用程式應該叫用 [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) 來取得一組完整的資訊。

如果 *dwParam1* 是 PHONESTATE \_ OWNER， *dwParam2* 就會包含新的擁有者數目。

如果 *dwParam1* 是 PHONESTATE \_ 監視器， *dwParam2* 就會包含新的監視器數目。

如果 *dwParam1* 為 PHONESTATE \_ 燈，則 *dwParam2* 包含已變更之燈泡的按鈕/燈泡識別碼。

如果 *dwParam1* 是 PHONESTATE \_ RINGMODE， *dwParam2* 就會包含新的響鈴模式。

如果 *dwParam1* 是 PHONESTATE \_ 的話筒、喇叭或耳機， *dwParam2* 就會包含該 hookswitch 裝置的新 hookswitch 模式。 此參數會使用其中一個 [**PHONEHOOKSWITCHMODE \_ 常數**](phonehookswitchmode--constants.md)。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

您可以使用 [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)和 [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)來控制和查詢傳送 **電話 \_ 狀態** 訊息至應用程式。 依預設，此訊息會針對所有狀態變更停用，但 PHONESTATE \_ 重新初始化除外，但無法停用。 此訊息會傳送至所有具有電話控制碼的應用程式，包括呼叫 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) 的應用程式，並將 *dwPrivileges* 參數設定為 PHONEPRIVILEGE \_ 擁有者或 PHONEPRIVILEGE \_ 監視器。

具有擁有者和/或監視器指示的 **電話 \_ 狀態** 消息，會傳送至已經有手機控制碼的應用程式。 這可能是因為另一個應用程式使用 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)、 [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) 或 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)來變更電話裝置的擁有權或 monitorship。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電話 \_ 關閉**](phone-close.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




