---
title: 'IWMDRMLicenseManagement ProcessLicenseRevocationResponse 方法 (Wmdrmsdk .h) '
description: ProcessLicenseRevocationResponse 方法會撤銷本機授權存放區的授權。 這個方法會使用授權撤銷伺服器所收到的授權撤銷 blob (LRB) 來識別要撤銷的授權。
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- ProcessLicenseRevocationResponse 方法 windows Media 格式
- ProcessLicenseRevocationResponse 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，ProcessLicenseRevocationResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseRevocationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d58c33f79db575dec37d7d2ac51e3c65b10416b9ca35a50084f36a56693854be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930308"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>IWMDRMLicenseManagement：:P rocessLicenseRevocationResponse 方法

**ProcessLicenseRevocationResponse** 方法會撤銷本機授權存放區的授權。 這個方法會使用授權撤銷伺服器所收到的授權撤銷 blob (LRB) 來識別要撤銷的授權。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessLicenseRevocationResponse(
  [in]  BYTE  *pbSignedLRB,
  [in]  DWORD cbSignedLRB,
  [out] BYTE  **ppbSignedACK,
  [out] DWORD *pcbSignedACK
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbSignedLRB* \[在\]
</dt> <dd>

授權撤銷 blob (LRB) 從授權撤銷伺服器收到，以回應藉由呼叫 [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) 方法所產生的挑戰。

</dd> <dt>

*cbSignedLRB* \[在\]
</dt> <dd>

LRB 的大小（以位元組為單位）。

</dd> <dt>

*ppbSignedACK* \[擴展\]
</dt> <dd>

接收授權撤銷通知位址之指標的位址。 確認應傳送給授權撤銷服務。 完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。

</dd> <dt>

*pcbSignedACK* \[擴展\]
</dt> <dd>

接收認可大小（以位元組為單位）之變數的位址。

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
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





