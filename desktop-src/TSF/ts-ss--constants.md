---
title: 'TS_SS_ 常數 (Textstor) '
description: Ts \_ SS \_ \ 常數（定義于 ts 狀態結構的執行時間之前 \_ ）會描述靜態檔狀態。
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967314"
---
# <a name="ts_ss_-constants"></a>TS \_ SS \_ \* 常數

Ts \_ SS \_ \* 常數（定義于 [**ts \_ 狀態**](/windows/desktop/api/Textstor/ns-textstor-ts_status)結構的執行時間之前）會描述靜態檔狀態。



| 常數/值                                                                                                                                                                                                                                                      | Description                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**TS \_SS \_ DISJOINTSEL**</dt> <dt> ( 0x1 )</dt> </dl>                             | 此檔支援多重選取。<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**TS \_SS \_ 區域**</dt> <dt> ( 0x2 )</dt> </dl>                                         | 檔可包含多個區域。<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**TS \_SS \_ 暫時性**</dt> <dt> ( 0x4 )</dt> </dl>                                | 檔預期會有簡短的使用週期。<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**TS \_SS \_ NOHIDDENTEXT**</dt> <dt> ( 0x8 )</dt> </dl>                          | 檔絕不會包含隱藏文字。<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**TS \_SS \_ TKBAUTOCORRECTENABLE**</dt> <dt> ( 0x10 )</dt> </dl> | **從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的自動校正。<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**TS \_SS \_ TKBPREDICTIONENABLE**</dt> <dt> ( 0x20 )</dt> </dl>    | **從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的文字建議。<br/> |



## <a name="remarks"></a>備註

**TS \_ 狀態** 結構的 **dwStaticFlags** 成員會使用這些常數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TS \_ 狀態**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**TF \_ 狀態**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

