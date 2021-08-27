---
description: 傳送 TAPI 電話 \_ 建立訊息，以通知應用程式建立新的電話裝置。
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: 'PHONE_CREATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18633ca9f3d45e08c3e2e054d51261dabe6494f42055567a5a68707408f94d5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072908"
---
# <a name="phone_create-message"></a>電話 \_ 建立訊息

傳送 TAPI **電話 \_ 建立** 訊息，以通知應用程式建立新的電話裝置。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPhone* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam1* 
</dt> <dd>

新建立裝置的 *hDeviceID* 。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

協商 API 版本1.3 的應用程式會傳送指定 PHONESTATE 重新初始化的 [**電話 \_ 狀態**](phone-state.md) 消息 \_ ，要求他們關閉 API 的使用方式，並再次呼叫 [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) 以取得新的裝置數目。 不過，在允許重新初始化應用程式之前，TAPI 1.4 版和更新版本不需要關閉所有應用程式。建立新裝置時，可以立即進行重新初始化。

支援 TAPI 1.4 版或更新版本的應用程式會傳送 **電話 \_ 建立** 訊息。 這會通知他們有新裝置和其新的裝置識別碼存在。 然後，應用程式可以選擇是否嘗試在新裝置的休閒中使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電話 \_ 狀態**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




