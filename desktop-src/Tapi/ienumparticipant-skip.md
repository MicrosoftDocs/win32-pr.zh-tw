---
description: Skip 方法會略過列舉順序中的下一個指定元素數目。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'IEnumParticipant：： Skip 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a55eb3298578738bb427efd6ab2b830b9a7850668aa3c9fa4712cc1bf48d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660698"
---
# <a name="ienumparticipantskip-method"></a>IEnumParticipant：： Skip 方法

\[**Skip** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Skip** 方法會略過列舉順序中的下一個指定元素數目。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。

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



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 略過的元素數目 *celt*。<br/>               |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | 未 *celt* 略過的元素數目。<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




