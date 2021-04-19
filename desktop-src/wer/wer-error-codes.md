---
title: 'WER 錯誤碼 (Werapi .h) '
description: 下表提供 Windows 錯誤報告所使用的自訂錯誤碼清單。
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965898"
---
# <a name="wer-error-codes"></a>WER 錯誤碼

下表提供 Windows 錯誤報告所使用的自訂錯誤碼清單。



| 常數                                                                                                                                                                                            | 描述                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <dt>**WER \_ E \_ \_ 緩衝區不足**</dt> </dl> | 緩衝區太小，無法包含資料。<br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <dt>**WER \_ E \_ 不正確 \_ 狀態**</dt> </dl>                   | 以不支援的方式呼叫函數。<br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <dt>**\_超過 WER E \_ 長度 \_**</dt> </dl>             | 超過長度限制的其中一個。<br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <dt>**WER \_ E \_ 遺失 \_ 參數**</dt> </dl>                   | 遺漏一或多個參數。<br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <dt>**\_ \_ 找不到 WER E \_**</dt> </dl>                               | Element not found.<br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <dt>**\_ \_ 已停用 WER E 存放區 \_**</dt> </dl>                | 存放區已停用。<br/>                    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Werapi。h</dt> </dl> |



 

 





