---
title: 'IWMSecureBuffer Encrypt 方法 (Wmdrmsdk .h) '
description: Encrypt 方法會加密資料指標。
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- 加密方法 windows Media 格式
- 加密方法 windows Media Format，IWMSecureBuffer 介面
- IWMSecureBuffer 介面 windows 媒體格式，加密方法
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983241"
---
# <a name="iwmsecurebufferencrypt-method"></a>IWMSecureBuffer：： Encrypt 方法

**Encrypt** 方法會加密資料指標。

## <a name="syntax"></a>語法


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSecureChannel* \[在\]
</dt> <dd>

安全通道介面的指標，其中包含要加密的資料指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

您可以使用這個方法來加密資料指標，以便跨 DLL 界限傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**解密**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**IWMSecureBuffer 介面**](iwmsecurebuffer.md)
</dt> </dl>

 

 





