---
title: IWMDRMDevice IsWMDRMDevice 方法
description: IsWMDRMDevice 方法會判斷裝置是否支援可攜式裝置的 Windows Media DRM 10。
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- IsWMDRMDevice 方法 windows Media 裝置管理員
- IsWMDRMDevice 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，IsWMDRMDevice 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984037"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>IWMDRMDevice：： IsWMDRMDevice 方法

**IsWMDRMDevice** 方法會判斷裝置是否支援可攜式裝置的 WINDOWS Media DRM 10。

## <a name="syntax"></a>語法


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwVersion* \[擴展\]
</dt> <dd>

適用于可攜式裝置的 Windows Media DRM 10 版本，其值為0x00010000。

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

 

 





