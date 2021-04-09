---
title: 'TF_SS_ 常數 (Msctf) '
description: TF \_ SS \_ \ 常數，定義在 tf 狀態結構的執行時間之前 \_ ，會描述靜態檔狀態。
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025200"
---
# <a name="tf_ss_-constants"></a>TF \_ SS \_ \* 常數

TF \_ SS \_ \* 常數（定義在 [**tf \_ 狀態**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))結構的執行時間之前）會描述靜態檔狀態。



| 常數/值                                                                                                                                                                                                                                                                              | Description                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**TF \_SS \_ DISJOINTSEL**</dt> <dt> ( TS \_ SS \_ DISJOINTSEL )</dt> </dl>                                     | 此檔支援多重選取。<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**TF \_SS \_ 區域**</dt> <dt> ( TS \_ SS \_ 區域 )</dt> </dl>                                                     | 檔可包含多個區域。<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**TF \_SS \_ 暫時性**</dt> <dt> ( TS \_ SS \_ 暫時性 )</dt> </dl>                                         | 檔預期會有簡短的使用週期。<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**TF \_SS \_ TKBAUTOCORRECTENABLE**</dt> <dt> ( TS \_ SS \_ TKBAUTOCORRECTENABLE )</dt> </dl> | **從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的自動校正。<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**TF \_SS \_ TKBPREDICTIONENABLE**</dt> <dt> ( TS \_ SS \_ TKBPREDICTIONENABLE )</dt> </dl>     | **從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的文字建議。<br/> |



## <a name="remarks"></a>備註

TF 狀態結構的 **dwStaticFlags** 成員會 \_ 使用這些常數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TF \_ 狀態**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

