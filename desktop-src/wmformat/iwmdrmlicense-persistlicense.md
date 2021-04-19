---
title: 'IWMDRMLicense PersistLicense 方法 (Wmdrmsdk .h) '
description: PersistLicense 方法會將目前的授權從暫時存放區儲存到永久的本機授權存放區。
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- PersistLicense 方法 windows Media 格式
- PersistLicense 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，PersistLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987105"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>IWMDRMLicense：:P ersistLicense 方法

**PersistLicense** 方法會將目前的授權從暫時存放區儲存到永久的本機授權存放區。

## <a name="syntax"></a>語法


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果目前的授權不在暫存存放區中，此方法將會失敗。

您可以呼叫 [**CanPersist**](iwmdrmlicense-canpersist.md) 來查詢是否允許保存授權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





