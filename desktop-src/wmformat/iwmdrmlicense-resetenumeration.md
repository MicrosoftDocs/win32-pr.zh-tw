---
title: 'IWMDRMLicense ResetEnumeration 方法 (Wmdrmsdk .h) '
description: ResetEnumeration 方法會將授權清單重設為其原始狀態。 作用中的授權會成為清單中的第一個授權。
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- ResetEnumeration 方法 windows Media 格式
- ResetEnumeration 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，ResetEnumeration 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982999"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>IWMDRMLicense：： ResetEnumeration 方法

**ResetEnumeration** 方法會將授權清單重設為其原始狀態。 作用中的授權會成為清單中的第一個授權。

## <a name="syntax"></a>語法


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





