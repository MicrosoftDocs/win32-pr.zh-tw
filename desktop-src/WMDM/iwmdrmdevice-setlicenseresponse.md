---
title: IWMDRMDevice SetLicenseResponse 方法
description: SetLicenseResponse 方法會設定授權回應。
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- SetLicenseResponse 方法 windows Media 裝置管理員
- SetLicenseResponse 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，SetLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982589"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>IWMDRMDevice：： SetLicenseResponse 方法

**SetLicenseResponse** 方法會設定授權回應。

## <a name="syntax"></a>語法


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbResponse* \[在\]
</dt> <dd>

指定要設定的回應。

</dd> <dt>

*cbResponse* \[在\]
</dt> <dd>

回應的大小（以位元組為單位）。

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

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





