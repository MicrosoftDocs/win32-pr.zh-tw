---
title: 'IWMDRMLicenseManagement CreateLicenseRevocationChallenge 方法 (Wmdrmsdk .h) '
description: CreateLicenseRevocationChallenge 方法會產生授權撤銷挑戰。
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- CreateLicenseRevocationChallenge 方法 windows Media 格式
- CreateLicenseRevocationChallenge 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，CreateLicenseRevocationChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977721"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>IWMDRMLicenseManagement：： CreateLicenseRevocationChallenge 方法

**CreateLicenseRevocationChallenge** 方法會產生授權撤銷挑戰。

## <a name="syntax"></a>語法


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbMachineID* \[在\]
</dt> <dd>

使用者指定的機器識別碼。 此值可用來查詢伺服器上的授權，而且必須符合授權伺服器所使用的任何格式。

</dd> <dt>

*cbMachineID* \[在\]
</dt> <dd>

電腦識別碼的大小（以位元組為單位）。

</dd> <dt>

*pbChallenge* \[在\]
</dt> <dd>

使用者指定的挑戰資料。 除了電腦識別碼之外，還會使用此資料來查詢授權伺服器，以取得要撤銷的授權。

</dd> <dt>

*cbChallenge* \[在\]
</dt> <dd>

挑戰資料的大小（以位元組為單位）。

</dd> <dt>

*ppbChallengeOutput* \[擴展\]
</dt> <dd>

接收挑戰輸出位址之指標的位址。 此緩衝區是傳送至授權撤銷服務的資料。 完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。

</dd> <dt>

*pcbChallengeOutput* \[擴展\]
</dt> <dd>

接收配置之挑戰輸出資料大小的變數位址（以位元組為單位）。

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
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





