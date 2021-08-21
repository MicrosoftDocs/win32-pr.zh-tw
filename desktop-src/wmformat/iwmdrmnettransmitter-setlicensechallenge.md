---
title: 'IWMDRMNetTransmitter SetLicenseChallenge 方法 (Wmdrmsdk .h) '
description: SetLicenseChallenge 方法會處理由網路裝置接收器 Windows 媒體 DRM 傳送的授權挑戰。
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- SetLicenseChallenge 方法 windows Media 格式
- SetLicenseChallenge 方法 windows Media Format，IWMDRMNetTransmitter 介面
- IWMDRMNetTransmitter 介面 windows Media Format，SetLicenseChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027566"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>IWMDRMNetTransmitter：： SetLicenseChallenge 方法

**SetLicenseChallenge** 方法會處理由網路裝置接收器 Windows 媒體 DRM 傳送的授權挑戰。

## <a name="syntax"></a>語法


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbLicenseChallenge* \[在\]
</dt> <dd>

接收者傳送的授權挑戰資料指標。

</dd> <dt>

*cbLicenseChallenge* \[在\]
</dt> <dd>

授權挑戰的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果這個方法成功，則對 **IWMDRMNetTransmitter** 其他方法的後續呼叫將會使用處理過的挑戰中的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMNetTransmitter 介面**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





