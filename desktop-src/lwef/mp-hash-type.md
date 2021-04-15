---
title: 'MP_HASH_TYPE 列舉 (MpClient .h) '
description: 可能的雜湊類型。
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE 列舉舊版 Windows 環境功能
- PMP_HASH_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466661"
---
# <a name="mp_hash_type-enumeration"></a>MP \_ HASH \_ 類型列舉

可能的雜湊類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP \_ HASH \_ 類型 \_ NONE**
</dt> <dd>

沒有雜湊。

</dd> <dt>

<span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP \_ HASH \_ TYPE \_ CRC32**
</dt> <dd>

CRC32

</dd> <dt>

<span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP \_ HASH \_ 類型 \_ MD5**
</dt> <dd>

MD5

</dd> <dt>

<span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP \_ HASH \_ 類型 \_ SHA1**
</dt> <dd>

SHA1

</dd> <dt>

<span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP \_ HASH \_ TYPE \_ SHA256**
</dt> <dd>

SHA 256

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





