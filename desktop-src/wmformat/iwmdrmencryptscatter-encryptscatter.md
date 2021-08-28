---
title: 'IWMDRMEncryptScatter EncryptScatter 方法 (Wmdrmsdk .h) '
description: EncryptScatter 方法會 unscrambles 和加密資料。
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- EncryptScatter 方法 windows Media 格式
- EncryptScatter 方法 windows Media Format，IWMDRMEncryptScatter 介面
- IWMDRMEncryptScatter 介面 windows Media Format，EncryptScatter 方法
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fae3f8a40bc5468898424dcf33bf947235a632db44f4dada7f2c96b2a3a064b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839708"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>IWMDRMEncryptScatter：： EncryptScatter 方法

**EncryptScatter** 方法會 unscrambles 和加密資料。

## <a name="syntax"></a>語法


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cBlocks* \[在\]
</dt> <dd>

*RgBlocks* 陣列中的元素數目。

</dd> <dt>

*rgBlocks* \[在\]
</dt> <dd>

一或多個 [**WMDRM \_ 加密 \_ 散佈 \_ 區塊**](wmdrm-encrypt-scatter-block.md) 結構的陣列。 每個元素會描述要 unscrambled 和加密的資料區塊。

</dd> <dt>

*pWMCryptoData* \[在\]
</dt> <dd>

包含加密參數之 [**WMDRMCryptoData**](wmdrmcryptodata.md) 結構的指標。 設定為 **Null** 以使用預設參數。

</dd> <dt>

*cbOutput* \[在\]
</dt> <dd>

傳遞為 *pbOutput* 的輸出資料緩衝區大小。

</dd> <dt>

*pbOutput* \[擴展\]
</dt> <dd>

輸出緩衝區。

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter 介面**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





