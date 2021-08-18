---
title: 'WINBIO_BIR_DATA_FLAGS 常數 (Winbio \_ 類型 .h) '
description: 指定資料的條件。
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87769500de02dedc7247b15e94064a43b7c6d528234c27ad700d4a336f42a092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622628"
---
# <a name="winbio_bir_data_flags-constants"></a>WINBIO \_ BIR \_ 資料 \_ 旗標常數

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **DataFlags** 成員會使用下列常數。



| 常數/值                                                                                                                                                                                                                                                                                   | 描述                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 隱私權**</dt> <dt>0x02</dt> </dl>                                       | 資料已加密。<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 完整性**</dt> <dt>0x01</dt> </dl>                                 | 資料會經過數位簽署，或由 (MAC) 的訊息驗證代碼保護。<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 已簽署**</dt> <dt>0x04</dt> </dl>                                          | 如果設定此旗標和 **WINBIO \_ 資料旗標 \_ \_ 完整性** 旗標，則會簽署資料。 如果未設定此旗標，但已設定 **WINBIO \_ 資料 \_ 旗標 \_ 完整性** 旗標，則會計算資料的 MAC。<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 原始**</dt> <dt>0x20</dt> </dl>                                                   | 資料的格式與捕捉的格式一樣。<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 中繼**</dt> <dt>0x40</dt> </dl>                        | 資料不是原始資料，但尚未完全處理。<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_已 \_ \_ 處理的資料旗**</dt>標 <dt>0x80</dt> </dl>                                 | 已處理資料。<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_資料 \_ 旗標 \_ 選項 \_ 遮罩 \_ 存在**</dt> <dt>0x08</dt> </dl> | 旗標遮罩。 此值一律為一個 (1) 。<br/>                                                                                                                                                           |



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

 

 





