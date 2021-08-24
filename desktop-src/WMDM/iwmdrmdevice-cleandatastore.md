---
title: IWMDRMDevice CleanDataStore 方法
description: CleanDataStore 方法會啟動清除裝置上 DRM 資料存放區的程式。
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- CleanDataStore 方法 windows Media 裝置管理員
- CleanDataStore 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，CleanDataStore 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9decc999d1ecb6c97359d1c4c169b84e7f67da88f5fa25bfe2cb17b2c31f9fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766638"
---
# <a name="iwmdrmdevicecleandatastore-method"></a>IWMDRMDevice：： CleanDataStore 方法

**CleanDataStore** 方法會啟動清除裝置上 DRM 資料存放區的程式。

## <a name="syntax"></a>語法


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

存放區清除準則的旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





