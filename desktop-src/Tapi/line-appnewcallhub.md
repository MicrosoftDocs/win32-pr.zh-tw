---
description: '\_當新的呼叫中樞建立時，會傳送 TAPI 線路 APPNEWCALLHUB 訊息來通知應用程式。'
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: 'LINE_APPNEWCALLHUB 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998660"
---
# <a name="line_appnewcallhub-message"></a>行 \_ APPNEWCALLHUB 訊息

當新的呼叫中樞建立時，會傳送 TAPI **線路 \_ APPNEWCALLHUB** 訊息來通知應用程式。


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

新中樞上的追蹤層級，如其中一個 [**LINECALLHUBTRACKING \_ 常數**](linecallhubtracking--constants.md)所定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此訊息源自 TAPI 而不是服務提供者，因此沒有對應的 TSPI 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




