---
description: 使用 Microsoft Win32 SetThreadPriority 函式，將執行緒的優先順序設定為新的值。
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: 'CMsgThread. SetThreadPriority 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981408"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>CMsgThread. SetThreadPriority 方法

使用 Microsoft Win32 **SetThreadPriority** 函式，將執行緒的優先順序設定為新的值。

## <a name="syntax"></a>語法


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nPriority* 
</dt> <dd>

執行緒的優先權。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                              | Description                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | 已成功設定優先順序。<br/> |
| <dl> <dt>FALSE * * * *</dt> </dl> | 未設定優先權。<br/>          |



 

## <a name="remarks"></a>備註

用戶端和背景工作執行緒可以呼叫這個成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




