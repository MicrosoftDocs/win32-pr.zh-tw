---
description: Set 方法會設定指定之資料流程品質屬性的值。
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'ITStreamQualityControl：： Set 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998836"
---
# <a name="itstreamqualitycontrolset-method"></a>ITStreamQualityControl：： Set 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

**Set** 方法會設定指定之 [**資料流程品質屬性**](streamqualityproperty.md)的值。

## <a name="syntax"></a>語法


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

[**StreamQualityProperty**](streamqualityproperty.md)列舉的成員。

</dd> <dt>

*左* \[ 值在\]
</dt> <dd>

輸入 *屬性* 所需的值。

</dd> <dt>

*lFlags* \[在\]
</dt> <dd>

[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出要如何控制 *屬性* 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
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

[**ITStreamQualityControl**](itstreamqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**StreamQualityProperty**](streamqualityproperty.md)
</dt> </dl>

 

 




