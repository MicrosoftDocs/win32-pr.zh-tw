---
title: 'WINBIO_REGISTERED_FORMAT 結構 (Winbio \_ 類型 .h) '
description: 將已註冊的資料格式指定為擁有者/格式組。
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT 結構 Windows 生物特徵辨識架構 API
- PWINBIO_REGISTERED_FORMAT 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508595"
---
# <a name="winbio_registered_format-structure"></a>WINBIO \_ 已註冊的 \_ 格式結構

**WINBIO \_ 註冊的 \_ 格式** 結構會將已註冊的資料格式指定為擁有者/格式組。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>成員

<dl> <dt>

**擁有者**
</dt> <dd>

IBIA (國際生物特徵辨識產業關聯) 指派的擁有者值。

</dd> <dt>

**型別**
</dt> <dd>

擁有者指派的格式。

</dd> </dl>

## <a name="remarks"></a>備註

由於 Windows 目前僅支援指紋辨識器，因此應該在 **WINBIO \_ 註冊的 \_ 格式** 結構中使用下列值。



| 常數                                    | 意義                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| WINBIO \_ ANSI \_ 381 \_ 格式的 \_ 擁有者<br/> | 資訊技術標準的國際委員會 (INCITS) 技術委員會 M1 (生物特徵辨識) 。<br/> |
| WINBIO \_ ANSI \_ 381 \_ 格式 \_ 類型<br/>  | ANSI INCITS 381 以映射為基礎的資料交換格式。<br/>                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ ANSI \_ 381 \_ 格式常數**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)
</dt> </dl>

 

 





