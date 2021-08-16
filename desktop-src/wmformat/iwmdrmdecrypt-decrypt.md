---
title: 'IWMDRMDecrypt 解密方法 (Wmdrmsdk .h) '
description: 解密方法會就地解密資料緩衝區。
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- 解密方法 windows 媒體格式
- 解密方法 windows Media Format，IWMDRMDecrypt 介面
- IWMDRMDecrypt 介面 windows 媒體格式，解密方法
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be82ec976da39103698b93a09b3d5235c8c8ee712783ca8284dc7b18c6a8a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027745"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt：:D ecrypt 方法

**解密** 方法會就地解密資料緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>pbdata* \[in、out\]
</dt> <dd>

要解密的資料。 如果方法成功，此資料會在傳回時解密。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

資料的大小（以位元組為單位）。

</dd> <dt>

*pWMCryptoData* \[在\]
</dt> <dd>

[**WMDRMCryptoData**](wmdrmcryptodata.md)結構的指標，其中包含額外的參數。 如果內容是使用預設參數進行加密，則可以是 **Null** 。

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

[**IWMDRMDecrypt 介面**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





