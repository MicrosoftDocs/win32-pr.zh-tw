---
title: 'WINBIO_BDB_ANSI_381_RECORD 結構 (Winbio \_ 類型 .h) '
description: 包含來自終端使用者的單一指紋或棕櫚範例的相關資訊。
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383974"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄結構

**WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄** 結構包含來自終端使用者的單一指紋或棕櫚範例的相關資訊。 這些結構的集合會包含在每個 [**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭**](winbio-bdb-ansi-381-header.md) 結構中。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a>成員

<dl> <dt>

**BlockLength**
</dt> <dd>

包含此結構的位元組數目以及範例影像資料的位元組數目。

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

指定取樣水準行中的圖元數。

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

指定取樣垂直線的圖元數。

</dd> <dt>

**位置**
</dt> <dd>

**WINBIO \_ 生物特徵辨識 \_ 子類型** 值，指定用來產生生物特徵辨識範例的手指或掌。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**CountOfViews**
</dt> <dd>

這必須設定為一個 (1) ;

</dd> <dt>

**ViewNumber**
</dt> <dd>

這必須設定為一個 (1) ;

</dd> <dt>

**ImageQuality**
</dt> <dd>

保留的。 這必須是 254 (0xFE) 。

</dd> <dt>

**ImpressionType**
</dt> <dd>

保留的。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。 必須設定為零 (0) 。

</dd> </dl>

## <a name="remarks"></a>備註

*Position* 成員會指定用來建立生物特徵辨識範例的手邊區域或掌上區域。 Windows 生物特徵辨識架構 (WBF) 目前僅支援指紋捕捉，並使用下列常數來表示位置資訊。

-   WINBIO \_ ANSI \_ 381 \_ POS \_ 不明
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 食指 \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 中間 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 環形 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 小 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 經驗
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 索引 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 中間 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 環形 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 小 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 四 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 四 \_ 手指
-   WINBIO \_ ANSI \_ 381 \_ POS \_ 雙 \_ 拇指

> [!IMPORTANT]
>
> 請勿嘗試驗證為 *位置* 值提供的值。 Windows 生物識別服務會先驗證提供的值，再將其傳遞至您的實作為。 如果值為 **WINBIO \_ 子類型 \_ NO \_ INFORMATION** 或 **WINBIO \_ 子類型 \_ ANY**，則在適當的位置驗證。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> </dl>

 

 





