---
description: 傳送 TAPI 線路 \_ DEVSPECIFIC 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。 訊息的意義和參數的解讀是裝置特定的。
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: 'LINE_DEVSPECIFIC 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca1ba410ac3127ff917965e8eda7c579be68dab5150c6dcae63a1930a98d265
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975668"
---
# <a name="line_devspecific-message"></a>行 \_ DEVSPECIFIC 訊息

傳送 TAPI **線路 \_ DEVSPECIFIC** 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。 訊息的意義和參數的解讀是裝置特定的。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

線路裝置或呼叫的控制碼。 這是裝置特定的。

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

服務提供者會使用 **LINE \_ DEVSPECIFIC** 訊息搭配 [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) 函數。 其意義是裝置特定的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




