---
description: 傳送 TAPI 線路 \_ 建立訊息，以通知應用程式建立新的線路裝置。
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: 'LINE_CREATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab18245dc151f074588216d272c305c3a4cbd6aaa85c650ec9854710f5b9eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762272"
---
# <a name="line_create-message"></a>行 \_ 建立訊息

傳送 TAPI **線路 \_ 建立** 訊息，以通知應用程式建立新的線路裝置。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
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

較舊的應用程式 (協商 TAPI 1.3 版) 會傳送指定 LINEDEVSTATE 重新初始化的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息 \_ ，要求他們關閉 API 的使用，並再次呼叫 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) 來取得新的裝置數目。 但與舊版 TAPI 不同的是，此版本不需要在允許重新初始化應用程式之前關閉所有應用程式;在建立新裝置時，將會立即進行重新初始化 (當服務提供者從系統) 移除時，仍需要完成關閉。

支援 TAPI 1.4 版或更新版本的應用程式會傳送 **LINE \_ CREATE** message。 這會通知他們有新裝置和其新的裝置識別碼存在。 然後，應用程式可以選擇是否嘗試在新裝置的休閒中使用。 這則訊息會傳送至所有支援此 API 或後續版本 API 的應用程式，此 API 稱為 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) 或 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)，包括當時沒有任何線路裝置開啟的應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




