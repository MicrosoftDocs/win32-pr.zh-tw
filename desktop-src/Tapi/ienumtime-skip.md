---
description: IEnumTime：： Skip 方法-Skip 方法會略過列舉順序中的下一個指定元素數目。
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'IEnumTime：： Skip 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190a98c14cb8f551276a173e2d73872d876f2ceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090716"
---
# <a name="ienumtimeskip-method"></a>IEnumTime：： Skip 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Skip** 方法會略過列舉順序中的下一個指定元素數目。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要略過的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                             | Description                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 略過的元素數目 *celt*。<br/>     |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 未 *celt* 略過的元素數目。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




