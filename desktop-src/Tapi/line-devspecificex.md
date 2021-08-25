---
description: 傳送 TAPI 線路 \_ DEVSPECIFICEX 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。 訊息的意義和參數的解讀是裝置特定的。
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: 'LINE_DEVSPECIFICEX 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b65b322b265b6bbd9717a9fc5b3c0eccf46bb3802fef7684a58d2d69645cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867068"
---
# <a name="line_devspecificex-message"></a>行 \_ DEVSPECIFICEX 訊息

傳送 TAPI **線路 \_ DEVSPECIFICEX** 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。 訊息的意義和參數的解讀是裝置特定的。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

線路裝置或呼叫的控制碼。 此參數是裝置特定的。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

特定裝置。

</dd> <dt>

*dwParam2* 
</dt> <dd>

特定裝置。

</dd> <dt>

*dwParam3* 
</dt> <dd>

特定裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

服務提供者會使用 **LINE \_ DEVSPECIFICEX** 訊息搭配 [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) 函數。 其意義是裝置特定的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




