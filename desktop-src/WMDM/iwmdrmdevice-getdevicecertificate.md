---
title: IWMDRMDevice GetDeviceCertificate 方法
description: GetDeviceCertificate 方法會抓取裝置憑證。
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- GetDeviceCertificate 方法 windows Media 裝置管理員
- GetDeviceCertificate 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetDeviceCertificate 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299233ff4344f44535933221141534ab2b0173ba54e47c9cc340020a2f462eb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619818"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a>IWMDRMDevice：： GetDeviceCertificate 方法

**GetDeviceCertificate** 方法會抓取裝置憑證。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrDevCert* \[擴展\]
</dt> <dd>

包含已抓取裝置憑證之 **BSTR** 的指標。

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

 

 





