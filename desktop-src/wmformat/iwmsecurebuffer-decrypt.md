---
title: 'IWMSecureBuffer 解密方法 (Wmdrmsdk .h) '
description: 解密方法會解密透過呼叫 Encrypt 方法加密的資料指標。
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- 解密方法 windows 媒體格式
- 解密方法 windows Media Format，IWMSecureBuffer 介面
- IWMSecureBuffer 介面 windows 媒體格式，解密方法
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9867cb6476ab0a2838903c906f662032e14dfb0d4fa0547b045672e03b6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930098"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer：:D ecrypt 方法

**解密** 方法會解密透過呼叫 [**Encrypt**](iwmsecurebuffer-encrypt.md)方法加密的資料指標。

## <a name="syntax"></a>語法


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSecureChannel* \[在\]
</dt> <dd>

安全通道介面的指標，其中包含加密的資料指標。

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

[**加密**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**IWMSecureBuffer 介面**](iwmsecurebuffer.md)
</dt> </dl>

 

 





