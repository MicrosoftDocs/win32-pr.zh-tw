---
description: GetNumberOfCapabilities 方法會抓取與目前格式相關聯的功能數目。
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'ITFormatControl：： GetNumberOfCapabilities 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993395"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a>ITFormatControl：： GetNumberOfCapabilities 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

**GetNumberOfCapabilities** 方法會抓取與目前格式相關聯的功能數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwCount* \[擴展\]
</dt> <dd>

功能的計數。

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

 

 




