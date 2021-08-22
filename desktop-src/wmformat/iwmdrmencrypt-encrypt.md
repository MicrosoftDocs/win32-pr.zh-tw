---
title: 'IWMDRMEncrypt Encrypt 方法 (Wmdrmsdk .h) '
description: Encrypt 方法會就地加密資料緩衝區。
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- 加密方法 windows Media 格式
- 加密方法 windows Media Format，IWMDRMEncrypt 介面
- IWMDRMEncrypt 介面 windows 媒體格式，加密方法
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb49b2857c23bb11b5e4d091dece820bb833b2b4e77224558f2d7972885445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027736"
---
# <a name="iwmdrmencryptencrypt-method"></a>IWMDRMEncrypt：： Encrypt 方法

**Encrypt** 方法會就地加密資料緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>pbdata* \[in、out\]
</dt> <dd>

要加密的資料。 如果方法成功，資料會在傳回時加密。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

資料的大小（以位元組為單位）。

</dd> <dt>

*pWMCryptoData* \[在\]
</dt> <dd>

[**WMDRMCryptoData**](wmdrmcryptodata.md)結構的指標，其中包含額外的參數。 設定為 **Null** 以使用預設的加密值。

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

[**IWMDRMEncrypt 介面**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





