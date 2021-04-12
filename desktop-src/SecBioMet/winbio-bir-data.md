---
title: 'WINBIO_BIR_DATA 結構 (Winbio \_ 類型 .h) '
description: 指定生物特徵辨識資訊區塊的大小（以位元組為單位）和位移。
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384597"
---
# <a name="winbio_bir_data-structure"></a>WINBIO \_ BIR \_ 資料結構

**WINBIO \_ BIR \_ 資料** 結構會指定以位元組為單位的大小，以及辨識項資訊區塊的位移。 [**WINBIO \_ BIR**](winbio-bir.md)結構會使用此結構來指定生物特徵辨識資訊記錄的各個部分所在的位置。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

生物特徵辨識資訊的大小（以位元組為單位）。

</dd> <dt>

**Offset**
</dt> <dd>

[**WINBIO \_ BIR**](winbio-bir.md)結構開頭的位移（以位元組為單位），表示生物特徵辨識資訊。

</dd> </dl>

## <a name="remarks"></a>備註

使用位移而非指標，可讓您輕鬆地序列化 BIR，以及在32和64位環境之間或使用者和核心模式之間進行較不復雜的轉譯。

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

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)
</dt> </dl>

 

 





