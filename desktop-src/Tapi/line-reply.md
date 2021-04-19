---
description: 傳送 TAPI 線路 \_ 回復訊息，以報告以非同步方式完成的函式呼叫結果。
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: 'LINE_REPLY 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983214"
---
# <a name="line_reply-message"></a>行 \_ 回復訊息

傳送 TAPI **線路 \_ 回復** 訊息，以報告以非同步方式完成的函式呼叫結果。


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

傳回應用程式的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

這是回復的要求識別碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

成功或錯誤指示。 應用程式應該將此參數轉換為 LONG。 零表示成功;負數表示錯誤。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

以非同步方式運作的函式會將正面要求識別碼值傳回給應用程式。 此要求識別碼會以回復訊息傳回，以識別已完成的要求。 **行 \_ 回復** 訊息的另一個參數會產生成功或失敗指示。 可能的錯誤與對應函式所定義的錯誤相同。 無法停用此訊息。

在某些情況下，應用程式可能無法接收對應至非同步函式呼叫的 **行 \_ 回復** 訊息。 如果在收到訊息之前將對應的呼叫控制碼解除配置，就會發生這種情況。

> [!Note]  
> 當應用程式叫用將資料寫入至應用程式記憶體的任何非同步作業時，應用程式必須保留該記憶體以供寫入，直到收到 **一行 \_ 回復** 或 [**行 \_ GATHERDIGITS**](line-gatherdigits.md) 訊息為止。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> </dl>

 

 




