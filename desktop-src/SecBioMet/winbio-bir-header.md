---
title: 'WINBIO_BIR_HEADER 結構 (Winbio \_ 類型 .h) '
description: 包含 (BIR) 的生物特徵辨識資訊記錄標頭。
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2166a206dd1590f83e16bc67482d3b42e24717efae4c44e54a99b9aa7d83b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911081"
---
# <a name="winbio_bir_header-structure"></a>WINBIO \_ BIR \_ 標頭結構

**WINBIO \_ BIR \_ 標頭** 結構包含生物特徵辨識資訊記錄的標頭 (BIR) 。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**ValidFields**
</dt> <dd>

位元遮罩，指定此結構中的哪些欄位有效。 如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 欄位常數**](winbio-bir-field-constants.md)。

</dd> <dt>

**HeaderVersion**
</dt> <dd>

指定標頭版本的 **WINBIO \_ BIR \_ 版本** 常數。 版本號碼是8位的值，其中的前四個位指定主要號碼，而低四個位則指定次要版本號碼。 目前，這必須是 WINBIO \_ CBEFF \_ 標頭 \_ 版本 (0x11) 。

</dd> <dt>

**PatronHeaderVersion**
</dt> <dd>

指定標頭版本的 **WINBIO \_ BIR \_ 版本** 常數。 版本號碼是8位的值，其中的前四個位指定主要號碼，而低四個位則指定次要版本號碼。 目前，這必須是 WINBIO \_ PATRON \_ 標頭 \_ 版本 (0x11) 。

</dd> <dt>

**DataFlags**
</dt> <dd>

值，指定標頭資料的格式。 這可以是下列安全性和處理層級旗標的位 **or** 。 如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 資料 \_ 旗標常數**](winbio-bir-data-flags-constants.md)。



| 值                                                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 隱私權**</dt> <dt> ( (UCHAR) 0x02)</dt> </dl>                                       | 資料已加密。<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 完整性**</dt> <dt> ( (UCHAR) 0x01)</dt> </dl>                                 | 資料是由 (MAC) 的訊息驗證程式代碼進行數位簽署或保護。<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_\_ \_ 簽署的資料旗**</dt>標 <dt> ( (UCHAR) 0x04)</dt> </dl>                                          | 如果設定此旗標和 **WINBIO \_ 資料旗標 \_ \_ 完整性** 旗標，則會簽署資料。 如果未設定此旗標，但已設定 **WINBIO \_ 資料 \_ 旗標 \_ 完整性** 旗標，則會計算資料的 MAC。<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 原始**</dt> <dt> ( (UCHAR) 0x20)</dt> </dl>                                                   | 資料的格式與捕捉的格式一樣。<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 中繼**</dt> <dt> ( (UCHAR) 0x40)</dt> </dl>                        | 資料不是原始資料，但尚未完全處理。<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_\_ \_**</dt> <dt> ( (UCHAR) 0X80)</dt>處理的資料旗標 </dl>                                 | 已處理資料。<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 選項 \_ 遮罩 \_ 存在**</dt> <dt> ( (UCHAR) 0x08)</dt> </dl> | 這個值一律是 1。<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**類型**
</dt> <dd>

WINBIO \_ 生物特徵辨識 \_ 類型值，指定生物特徵辨識資訊記錄中所參考的生物特徵辨識資料類型。 目前只支援 **WINBIO \_ 類型 \_ 指紋** 。 如需詳細資訊，請參閱 [**WINBIO \_ 生物特徵辨識 \_ 類型常數**](winbio-biometric-type-constants.md)。

</dd> <dt>

**亞**
</dt> <dd>

**WINBIO \_ 生物特徵辨識 \_ 子類型** 值，指定與生物特徵辨識資料相關聯的輔助因素。 如需詳細資訊，請參閱備註和 [**WINBIO \_ 生物特徵辨識 \_ 子類型常數**](winbio-biometric-subtype-constants.md)。

</dd> <dt>

**目的**
</dt> <dd>

**WINBIO \_ BIR \_ 目的** 遮罩，可指定資料的預期用途。 這可以是下列值的位 **or** 。 如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 用途常數**](winbio-bir-purpose-constants.md)。

-   WINBIO \_ 用途 \_ 驗證
-   WINBIO \_ 目的 \_ 識別
-   WINBIO \_ 目的 \_ 註冊
-   WINBIO \_ 目的 \_ 註冊 \_ 以進行 \_ 驗證
-   WINBIO \_ 目的 \_ 註冊 \_ 以供 \_ 識別
-   WINBIO \_ 目的 \_ 審核

</dd> <dt>

**DataQuality**
</dt> <dd>

值，指定生物特徵辨識資訊記錄中生物特徵辨識資料的相對品質 (BIR) 。 這可以是從0到100或下列其中一個值的整數。 如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 品質常數**](winbio-bir-quality-constants.md)。



| 值                                                                                                                                                                                                                                                                                                        | 意義                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_資料 \_ 品質 \_ 未 \_ 設定**</dt> <dt> ( (WINBIO \_ BIR \_ QUALITY) -1)</dt> </dl>                   | BIR 建立者支援品質度量，但未在 BIR 中設定任何值。<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_\_ \_ 不 \_ 支援的資料品質**</dt> <dt> ( (WINBIO \_ BIR \_ 品質) -2)</dt> </dl> | BIR 建立者不支援品質度量。<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

BIR 建立的日期和時間，以國際標準時間 (格林威治平均時間) ）。

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

BIR 有效的期間。

<dl> <dt>

**BeginDate**
</dt> <dd>

有效期間開始的日期和時間（國際標準時間）。

</dd> <dt>

**日期**
</dt> <dd>

BIR 不再有效的日期和時間，以國際標準時間。

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

[**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)結構，可指定 [**WINBIO \_ BIR**](winbio-bir.md)結構中標準資料區塊的資料格式。 **WINBIO \_ 註冊的 \_ 格式** 成員不可以是零。 您可以使用下列常數來簡化錯誤檢查。



| 值                                                                                                                                                                                                                                                                                      | 意義                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_沒有 \_ 格式 \_ 擁有者 \_ 可用**</dt> <dt> ( (USHORT) 0)</dt> </dl> | 未指定 IBIA (國際生物特徵辨識產業關聯) 指派的擁有者值。<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_沒有 \_ 格式 \_ 類型 \_ 可用**</dt> <dt> ( (USHORT) 0)</dt> </dl>    | 未指定任何格式類型。<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

[**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)結構，指定在 BIR 中產生標準資料區塊之元件的產品識別碼。 **WINBIO \_ 註冊的 \_ 格式** 成員可以是零。

</dd> </dl>

## <a name="remarks"></a>備註

*子類型* 參數指定與生物特徵辨識資料相關聯的輔助因素。 目前，Windows 生物特徵辨識架構 (WBF) 只支援指紋捕捉，並使用下列常數來表示子類型資訊：

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
> 請勿嘗試驗證為 *子類型* 參數值提供的值。 Windows 生物特徵辨識服務會先驗證提供的值，再將其傳遞至您的實作為。 如果值為 **WINBIO \_ 子類型 \_ NO \_ INFORMATION** 或 **WINBIO \_ 子類型 \_ ANY**，則在適當的位置驗證。

 

如果有任何一個位被判斷提示，表示 **WINBIO \_ BIR \_ 標頭** 結構的格式不正確。


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



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

[**WINBIO \_ 生物特徵辨識 \_ 子類型常數**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 資料 \_ 旗標常數**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 欄位常數**](winbio-bir-field-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 用途常數**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 品質常數**](winbio-bir-quality-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 版本常數**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





