---
title: 'WINBIO_BIR_FIELD 常數 (Winbio \_ 類型 .h) '
description: 指定位元遮罩。
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a354f3119fcef6da3ff204f833616eeb2ac9570cdad0712a87686904ad528958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035088"
---
# <a name="winbio_bir_field-constants"></a>WINBIO \_ BIR \_ 欄位常數

下列常數可用來為 [**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **ValidFields** 成員建立位元遮罩。



| 常數/值                                                                                                                                                                                                                                                                                           | 描述                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_BIR \_ FIELD \_ .subhead \_ COUNT**</dt> <dt>0x0001</dt> </dl>                          | 為了符合 NISTIR 6529-A，常見的生物特徵辨識 Exchange 格式 Framework (CBEFF) Patron 格式 A，但不會使用。<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 產品 \_ 識別碼**</dt> <dt>0x0002</dt> </dl>                                   | **ProductId** 成員有效。<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ PATRON \_ 識別碼**</dt> <dt>0x0004</dt> </dl>                                      | 為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 索引**</dt> <dt>0x0008</dt> </dl>                                                   | 為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 建立 \_ 日期**</dt> <dt>0x0010</dt> </dl>                          | **CreationDate** 成員有效。<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 有效 \_ 期間**</dt> <dt>0x0020</dt> </dl>                    | **ValidityPeriod** 成員有效。<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 類型**</dt> <dt>0x0040</dt> </dl>                       | **類型** 成員有效。<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 子類型**</dt> <dt>0x0080</dt> </dl>              | **子類型** 成員有效。<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ CBEFF \_ 標頭 \_ 版本**</dt> <dt>0x0100</dt> </dl>    | **HeaderVersion** 成員有效。<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ PATRON \_ 標頭 \_ 版本**</dt> <dt>0x0200</dt> </dl> | **PatronHeaderVersion** 成員有效。<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 用途**</dt> <dt>0x0400</dt> </dl>              | **目的** 成員有效。<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 條件**</dt> <dt>0x0800</dt> </dl>        | 為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_ 品質**</dt> <dt>0x1000</dt> </dl>                                             | **DataQuality** 成員有效。<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_BIR \_ FIELD \_ CREATOR**</dt> <dt>0x2000</dt> </dl>                                             | 為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_BIR \_ 現場 \_ 挑戰**</dt> <dt>0x4000</dt> </dl>                                       | 為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_BIR \_ 欄位 \_**</dt>裝載 <dt>0x8000</dt> </dl>                                             | 為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。<br/>                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





