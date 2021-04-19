---
title: IWMDRMDevice SetSecureClockResponse 方法
description: SetSecureClockResponse 方法會設定安全的時鐘回應。
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- SetSecureClockResponse 方法 windows Media 裝置管理員
- SetSecureClockResponse 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，SetSecureClockResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986597"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>IWMDRMDevice：： SetSecureClockResponse 方法

**SetSecureClockResponse** 方法會設定安全的時鐘回應。

## <a name="syntax"></a>語法


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbResponse* \[在\]
</dt> <dd>

要設定的安全時鐘回應。

</dd> <dt>

*cbResponse* \[在\]
</dt> <dd>

指定的安全時鐘回應大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





