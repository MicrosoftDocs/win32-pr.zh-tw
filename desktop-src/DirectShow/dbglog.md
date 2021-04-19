---
description: 如果已針對指定的類型和層級啟用記錄，DbgLog 宏會將字串傳送至偵錯工具輸出位置。 零售組建中會忽略此宏。
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: 'DbgLog 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981351"
---
# <a name="dbglog-macro"></a>DbgLog 宏

如果已針對指定的類型和層級啟用記錄， **DbgLog** 宏會將字串傳送至偵錯工具輸出位置。 零售組建中會忽略此宏。

## <a name="syntax"></a>語法


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* 
</dt> <dd>

一或多個訊息類型的位元組合。

</dd> <dt>

*Level* 
</dt> <dd>

此訊息的記錄層級。

</dd> <dt>

*Pformatetc 架構* 
</dt> <dd>

**Printf** 樣式的格式字串。

</dd> <dt>

*...* 
</dt> <dd>

格式字串的其他引數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="remarks"></a>備註

如果任何訊息類型的 debug 記錄設定為指定的層級或更高的層級，此宏就會將格式化的字串傳送至偵錯工具的輸出位置。

宏會自動將換行字元加入至輸出字串。

> [!Note]  
> 另外一組括弧必須用來括住巨集引數：

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




