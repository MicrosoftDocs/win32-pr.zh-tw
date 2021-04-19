---
description: 使用 Microsoft Win32 GetThreadPriority 函式來取得目前背景工作執行緒的優先權。
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: 'CMsgThread. GetThreadPriority 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978633"
---
# <a name="cmsgthreadgetthreadpriority-method"></a>CMsgThread. GetThreadPriority 方法

使用 Microsoft Win32 **GetThreadPriority** 函式來取得目前背景工作執行緒的優先權。

## <a name="syntax"></a>語法


```C++
int GetThreadPriority();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

以整數形式傳回執行緒優先權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




