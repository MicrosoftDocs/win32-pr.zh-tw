---
title: '一般常數 (Winbio \_ 類型 .h) '
description: 指定最大 SID 長度、控制碼、識別碼、最大字串長度，以及最大範例緩衝區大小。
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934373"
---
# <a name="general-constants-winbio_typesh"></a>一般常數 (Winbio \_ 類型 .h) 

整個 Windows 生物特徵辨識架構都會使用下列常數。



| 常數/值                                                                                                                                                                                                                                                                   | Description                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**安全性 \_ 最大 \_ SID \_ 大小**</dt> </dl>                                                                                          | 安全識別碼 (SID) 值的最大長度。 目前這是68。<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**WINBIO \_ 單位 \_ 識別碼**</dt> </dl>                                                                                                                | 生物識別單位的識別碼。<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**WINBIO \_ 會話 \_ 控制碼**</dt> </dl>                                                                                           | 不帶正負號的長整數，其中包含開啟生物特徵辨識會話的控制碼。<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**WINBIO \_ 架構 \_ 控制碼**</dt> </dl>                                                                                     | 不帶正負號的長整數，其中包含開啟架構會話的控制碼。<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**WINBIO \_ UUID**</dt> </dl>                                                                                                                          | GUID。<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**WINBIO \_ 字串**</dt> </dl>                                                                                                                    | 位元組陣列，其中包含以 null 終止的 Unicode 字串。<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_最大 \_ 字串 \_ 長度**</dt> </dl>                                                                                       | **WINBIO \_ 字串** 值的最大長度。 目前這是256。<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_最大 \_ 範例 \_ 緩衝區 \_ 大小**</dt> <dt>0x7fffffff</dt> </dl> | 單一生物特徵辨識資料捕捉中的最大位元組數目。<br/>                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





