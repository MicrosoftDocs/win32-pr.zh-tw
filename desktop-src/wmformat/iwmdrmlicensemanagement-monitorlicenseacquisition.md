---
title: 'IWMDRMLicenseManagement MonitorLicenseAcquisition 方法 (Wmdrmsdk .h) '
description: MonitorLicenseAcquisition 方法會起始授權取得程式的監視。
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- MonitorLicenseAcquisition 方法 windows Media 格式
- MonitorLicenseAcquisition 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，MonitorLicenseAcquisition 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986562"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>IWMDRMLicenseManagement：： MonitorLicenseAcquisition 方法

**MonitorLicenseAcquisition** 方法會起始授權取得程式的監視。

## <a name="syntax"></a>語法


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKID* \[在\]
</dt> <dd>

取得的授權 (小孩) 的金鑰識別碼。

</dd> <dt>

*bstrHeader* \[在\]
</dt> <dd>

[**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)方法呼叫中使用的內容標頭。

</dd> <dt>

*bstrActions* \[在\]
</dt> <dd>

字串，包含在呼叫 **AcquireLicense** 方法時所要求的動作。

</dd> <dt>

*ppunkCancelationCookie* \[擴展\]
</dt> <dd>

指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。 這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。

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

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





