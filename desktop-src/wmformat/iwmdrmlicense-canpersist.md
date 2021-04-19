---
title: 'IWMDRMLicense CanPersist 方法 (Wmdrmsdk .h) '
description: CanPersist 方法會查詢授權是否可保存在本機授權存放區中。
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- CanPersist 方法 windows Media 格式
- CanPersist 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CanPersist 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998835"
---
# <a name="iwmdrmlicensecanpersist-method"></a>IWMDRMLicense：： CanPersist 方法

**CanPersist** 方法會查詢授權是否可保存在本機授權存放區中。

## <a name="syntax"></a>語法


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfCanPersist* \[擴展\]
</dt> <dd>

TRUE 表示可以保存授權。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





