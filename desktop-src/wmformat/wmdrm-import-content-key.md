---
title: 'WMDRM_IMPORT_CONTENT_KEY 結構 (Drmexternals .h) '
description: WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰結構會儲存匯入受保護內容時所使用的內容金鑰。
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383990"
---
# <a name="wmdrm_import_content_key-structure"></a>WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰結構

**WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰** 結構會儲存匯入受保護內容時所使用的內容金鑰。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

版本。

</dd> <dt>

**cbStructSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**dwIVKeyType**
</dt> <dd>

初始化向量索引鍵類型。 設定為 WMDRM \_ KEYTYPE \_ RC4。

</dd> <dt>

**cbIVKey**
</dt> <dd>

初始化向量索引鍵的大小（以位元組為單位）。

</dd> <dt>

**dwContentKeyType**
</dt> <dd>

內容金鑰類型。 設定為 WMDRM \_ KEYTYPE \_ 雞尾酒。

</dd> <dt>

**cbContentKey**
</dt> <dd>

內容金鑰的大小（以位元組為單位）。

</dd> <dt>

**rgbKeyData**
</dt> <dd>

包含內容索引鍵的緩衝區位址。 緩衝區大小必須符合 **cbContentKey** 的值。 此金鑰應符合從 XMR 授權訊息匯入的金鑰。

</dd> </dl>

## <a name="remarks"></a>備註

此結構（包括包含工作階段金鑰的緩衝區）必須使用工作階段金鑰進行加密，並包含在 [**WMDRM 匯 \_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)結構的 **pbEncryptedKeyMessage** 成員中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                      |
| 版本<br/>                  | Windows Media Format 11 SDK<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





