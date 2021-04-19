---
description: ReleaseFormat 方法會釋放與格式相關聯的結構。
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'ITFormatControl：： ReleaseFormat 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984113"
---
# <a name="itformatcontrolreleaseformat-method"></a>ITFormatControl：： ReleaseFormat 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

**ReleaseFormat** 方法會釋放與格式相關聯的結構。

## <a name="syntax"></a>語法


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaType* \[在\]
</dt> <dd>

終端機格式的 **AM \_ 媒體 \_ 類型** 描述元指標。 如需 **\_ 媒體 \_ 類型** 的詳細資訊，請參閱 DirectX 檔。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




