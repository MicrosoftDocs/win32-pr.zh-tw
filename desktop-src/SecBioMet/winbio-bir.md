---
title: 'WINBIO_BIR 結構 (Winbio \_ 類型 .h) '
description: 代表 (BIR) 的生物特徵辨識資訊記錄。
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb9e82a27717b33bcd0e06f5cd5bc23a3c43bc3a67cf70068f1a9eeb31b08bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911091"
---
# <a name="winbio_bir-structure"></a>WINBIO \_ BIR 結構

**WINBIO \_ BIR** 結構代表 (BIR) 的生物特徵辨識資訊記錄。 資訊記錄包含標頭、資料和簽章區塊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>成員

<dl> <dt>

**HeaderBlock**
</dt> <dd>

[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)結構，其中包含 BIR 標頭的大小（以位元組為單位）和位移。 標頭包含描述資訊記錄內容的資訊。

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)結構，其中包含由 Windows 生物特徵辨識架構 (WBF) 所建立的已處理或未處理生物特徵辨識資訊的大小（以位元組為單位）和位移。

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)結構，其中包含廠商感應器和軟體所提供的已處理或未處理生物特徵辨識資訊的大小（以位元組為單位）和位移。

</dd> <dt>

**SignatureBlock**
</dt> <dd>

選擇性的 [**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md) 結構，其中包含數位簽章消息驗證程式代碼的大小（以位元組為單位）和位移 (MAC) ，可用來驗證 BIR 的完整性。 如果有的話，簽章或 MAC 必須涵蓋標頭和資料區塊。

</dd> </dl>

## <a name="remarks"></a>備註

使用位移而非指標，可讓您輕鬆地序列化 BIR，以及在32和64位環境之間或使用者和核心模式之間進行較不復雜的轉譯。

BIR 可與 NIST 6529-A 所定義 (CBEFF) 的通用生物特徵辨識 Exchange 格式架構相容。

如果此結構包含 *StandardDataBlock* 值， *HeaderBlock* 參數所指定之標頭的 *型* 別參數必須設定為 **WINBIO \_ ANSI \_ 381 \_ 格式 \_ 類型**。 這是目前 Windows 生物特徵辨識架構版本所支援的唯一標準資料格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)
</dt> </dl>

 

 





