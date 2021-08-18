---
title: 'WMDRM_IMPORT_SESSION_KEY 結構 (Drmexternals .h) '
description: WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰結構會保存用來匯入受保護內容的工作階段金鑰。
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34cdff6d17ad6ce60dd40478b56c9718be0863295422d2e5c60fee2c437dc6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844057"
---
# <a name="wmdrm_import_session_key-structure"></a>WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰結構

**WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰** 結構會保存用來匯入受保護內容的工作階段金鑰。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwKeyType**
</dt> <dd>

工作階段金鑰類型。 設定為 WMDRM \_ KEYTYPE \_ RC4。

</dd> <dt>

**cbKey**
</dt> <dd>

工作階段金鑰的大小（以位元組為單位）。 此值可以是您所需的最大值，因為對整個訊息的單一 RSA OAEP 作業限制 (此結構以及工作階段金鑰) 。

</dd> <dt>

**rgbKey**
</dt> <dd>

包含工作階段金鑰之緩衝區的位址。 緩衝區大小必須符合 **cbKey** 的值。 緩衝區中的資料是隨機產生的索引鍵值。

</dd> </dl>

## <a name="remarks"></a>備註

此結構（包括包含工作階段金鑰的緩衝區）必須以 Windows 媒體 DRM 電腦公開金鑰加密，並包含在 [**WMDRM 匯 \_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)結構的 **pbEncryptedSessionKeyMessage** 成員中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                      |
| 版本<br/>                  | Windows媒體格式 11 SDK<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





