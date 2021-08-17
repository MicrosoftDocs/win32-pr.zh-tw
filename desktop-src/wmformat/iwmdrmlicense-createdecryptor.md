---
title: 'IWMDRMLicense CreateDecryptor 方法 (Wmdrmsdk .h) '
description: CreateDecryptor 方法會使用目前授權的設定來建立解密程式物件。
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- CreateDecryptor 方法 windows Media 格式
- CreateDecryptor 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CreateDecryptor 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ac7e6bb1e9d4f9e5e7c706c0a9e3518f62b1068ed743dc795554dd43ac61e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027706"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>IWMDRMLicense：： CreateDecryptor 方法

**CreateDecryptor** 方法會使用目前授權的設定來建立解密程式物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDecryptor* \[擴展\]
</dt> <dd>

接收新建立物件之 [**IWMDRMDecrypt**](iwmdrmdecrypt.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | 描述                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateEncryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





