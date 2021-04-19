---
title: 'IWMDRMLicense CreateEncryptor 方法 (Wmdrmsdk .h) '
description: CreateEncryptor 方法會使用目前授權的設定來建立加密程式物件。
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- CreateEncryptor 方法 windows Media 格式
- CreateEncryptor 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CreateEncryptor 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001825"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>IWMDRMLicense：： CreateEncryptor 方法

**CreateEncryptor** 方法會使用目前授權的設定來建立加密程式物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEncryptor* \[擴展\]
</dt> <dd>

接收新建立物件之 [**IWMDRMEncrypt**](iwmdrmencrypt.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | Description                                              |
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

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





