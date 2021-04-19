---
description: GetFrameFromFrameHandle 函式會從框架控制碼傳回框架的指標。
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: 'GetFrameFromFrameHandle 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973219"
---
# <a name="getframefromframehandle-function"></a>GetFrameFromFrameHandle 函式

**GetFrameFromFrameHandle** 函式會從框架控制碼傳回框架的指標。

## <a name="syntax"></a>語法


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為框架的指標。

如果函式不成功，則傳回值為0。

## <a name="remarks"></a>備註

**GetFrameFromFrameHandle** 函式會抓取網路監視器提供的其他 helper 函數無法取出的資料。 盡可能使用下列功能。

<dl>

[**GetFrameDstAddressOffset**](getframedstaddressoffset.md)  
[**GetFrameSrcAddressOffset**](getframesrcaddressoffset.md)  
[**GetFrameCaptureHandle**](getframecapturehandle.md)  
[**GetFrameDestAddress**](getframedestaddress.md)  
[**GetFrameSourceAddress**](getframesourceaddress.md)  
[**GetFrameMacHeaderLength**](getframemacheaderlength.md)  
[**GetFrameLength**](getframelength.md)  
[**GetFrameStoredLength**](getframestoredlength.md)  
[**GetFrameMacType**](getframemactype.md)  
[**GetFrameNumber**](getframenumber.md)  
[**GetFrameTimeStamp**](getframetimestamp.md)  
</dl>

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameFromFrameHandle** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




