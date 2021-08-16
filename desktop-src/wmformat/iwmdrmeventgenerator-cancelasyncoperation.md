---
title: 'IWMDRMEventGenerator CancelAsyncOperation 方法 (Wmdrmsdk .h) '
description: CancelAsyncOperation 方法會取消非同步作業。
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- CancelAsyncOperation 方法 windows Media 格式
- CancelAsyncOperation 方法 windows Media Format，IWMDRMEventGenerator 介面
- IWMDRMEventGenerator 介面 windows Media Format，CancelAsyncOperation 方法
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ca44fa141d21caeed1d0f16da65a1db61fe319e2b9424600275563e6c5d52f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847155"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>IWMDRMEventGenerator：： CancelAsyncOperation 方法

**CancelAsyncOperation** 方法會取消非同步作業。

## <a name="syntax"></a>語法


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*punkCancelationCookie* \[在\]
</dt> <dd>

識別要取消之非同步作業的取消 cookie 指標。 此 cookie 是由用來啟動作業的方法所提供。

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
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMEventGenerator 介面**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





