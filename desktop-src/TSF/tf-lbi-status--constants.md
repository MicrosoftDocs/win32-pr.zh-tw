---
title: 'TF_LBI_STATUS_ 常數 (Ctfutb) '
description: TF \_ LBI \_ status \_ \ 常數表示 language bar 專案的狀態。 這些值會與 ITfLangBarItem GetStatus 方法搭配使用。
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686263"
---
# <a name="tf_lbi_status_-constants"></a>TF \_ LBI \_ 狀態 \_ \* 常數

**TF \_ LBI \_ STATUS \_ \** _ 常數表示語言列專案的狀態。 這些值會搭配 [ITfLangBarItem：： GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) 方法使用。



| 常數/值                                                                                                                                                                                                                                                       | Description                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_隱藏的 LBI \_ 狀態 \_ * *</dt> <dt>0x00000001</dt> </dl>                 | 專案是隱藏的。 如果專案不包含 TF \_ LBI \_ style HIDDENSTATUSCONTROL 樣式，則會忽略這個樣式 \_ 。<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**TF \_LBI \_ 狀態 \_ 停用**</dt> <dt>0x00000002</dt> </dl>           | 項目已停用。<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**TF \_LBI \_ 狀態 \_ BTN \_ 切換**</dt>的 <dt>0x00010000</dt> </dl> | 專案處於已切換或已按下的狀態。 如果專案不包含 TF \_ LBI \_ style \_ BTN \_ 轉場樣式，則會忽略這個樣式。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ctfutb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfLangBarItem：： GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





