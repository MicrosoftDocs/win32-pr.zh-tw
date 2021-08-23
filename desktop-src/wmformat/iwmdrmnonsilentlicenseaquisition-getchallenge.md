---
title: 'IWMDRMNonSilentLicenseAquisition GetChallenge 方法 (Wmdrmsdk .h) '
description: GetChallenge 方法會抓取應張貼至授權伺服器的授權挑戰。
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- GetChallenge 方法 windows Media 格式
- GetChallenge 方法 windows Media Format，IWMDRMNonSilentLicenseAquisition 介面
- IWMDRMNonSilentLicenseAquisition 介面 windows Media Format，GetChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf495652033bdb5201f2b4e5bd9dc1d6a222cc3ebdf4ec6438fe391ed06fac85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027516"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>IWMDRMNonSilentLicenseAquisition：： GetChallenge 方法

**GetChallenge** 方法會抓取應張貼至授權伺服器的授權挑戰。

## <a name="syntax"></a>語法


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrChallenge* \[擴展\]
</dt> <dd>

接收授權挑戰之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
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

[**IWMDRMNonSilentLicenseAquisition 介面**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





