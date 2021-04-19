---
description: TAPI 電話 \_ 回復訊息會傳送至應用程式，以報告以非同步方式完成的函式呼叫結果。
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: 'PHONE_REPLY 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976764"
---
# <a name="phone_reply-message"></a>電話 \_ 回復訊息

TAPI **電話 \_ 回復** 訊息會傳送至應用程式，以報告以非同步方式完成的函式呼叫結果。


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

以非同步方式運作的函式會將正面要求識別碼值傳回給應用程式。 此要求識別碼會以回復訊息傳回，以識別已完成的要求。 **電話 \_ 回復** 訊息的另一個參數會產生成功或失敗的指示。 可能的錯誤與對應函式所定義的錯誤相同。 無法停用此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




