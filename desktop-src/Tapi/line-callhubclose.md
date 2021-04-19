---
description: '\_當呼叫中樞關閉時，就會傳送 TAPI 線路 CALLHUBCLOSE 訊息。'
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: 'LINE_CALLHUBCLOSE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989816"
---
# <a name="line_callhubclose-message"></a>行 \_ CALLHUBCLOSE 訊息

當呼叫中樞關閉時，就會傳送 TAPI **線路 \_ CALLHUBCLOSE** 訊息。


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

保留的。 設定為0。

</dd> <dt>

*dwParam2* 
</dt> <dd>

保留的。 設定為0。

</dd> <dt>

*dwParam3* 
</dt> <dd>

保留的。 設定為0。

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



 

 




