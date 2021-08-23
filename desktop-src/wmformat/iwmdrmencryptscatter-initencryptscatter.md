---
title: 'IWMDRMEncryptScatter InitEncryptScatter 方法 (Wmdrmsdk .h) '
description: InitEncryptScatter 方法會初始化 IWMDRMEncryptScatter 介面以供使用。
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- InitEncryptScatter 方法 windows Media 格式
- InitEncryptScatter 方法 windows Media Format，IWMDRMEncryptScatter 介面
- IWMDRMEncryptScatter 介面 windows Media Format，InitEncryptScatter 方法
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e83cce80b218d4cc8482d013537b7fae562312f242bc3549f4fa5069b1c677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027755"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>IWMDRMEncryptScatter：： InitEncryptScatter 方法

**InitEncryptScatter** 方法會初始化 **IWMDRMEncryptScatter** 介面以供使用。

## <a name="syntax"></a>語法


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cStreams* \[在\]
</dt> <dd>

*RgInfos* 陣列中的元素數目。 這也是要加密的資料中包含的資料流程數目。

</dd> <dt>

*rgInfos* \[在\]
</dt> <dd>

一或多個 [**WMDRM \_ 加密 \_ 散佈 \_ 資訊**](wmdrm-encrypt-scatter-info.md) 結構的陣列。 每個元素都包含資料流程的加密資訊。 此陣列中的元素數目必須等於 *cStreams* 的值。

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

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter 介面**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





