---
title: 'WMDRMCryptoData 結構 (Wmdrmsdk .h) '
description: WMDRMCryptoData 結構包含用來加密和解密內容的密碼編譯演算法的相關資訊。
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- WMDRMCryptoData 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999377"
---
# <a name="wmdrmcryptodata-structure"></a>WMDRMCryptoData 結構

**WMDRMCryptoData** 結構包含用來加密和解密內容的密碼編譯演算法的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**cryptoType**
</dt> <dd>

[**DRM \_ 加密 \_ 類型**](drm-crypto-type.md)列舉的成員，指定密碼編譯演算法的類型。

</dd> <dt>

**qwCounterID**
</dt> <dd>

128位 AES 計數器模式的高64位。 只有當 **cryptoType** 成員設定為 **加密 \_ 類型 \_ MCE** 時，才會使用這個成員。

</dd> <dt>

**qwOffset**
</dt> <dd>

128位 AES 計數器模式的低64位。 只有當 **cryptoType** 成員設定為 **加密 \_ 類型 \_ MCE** 時，才會使用這個成員。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





