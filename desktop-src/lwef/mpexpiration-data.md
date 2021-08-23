---
title: 'MPEXPIRATION_DATA 結構 (MpClient .h) '
description: 產品到期狀態通知。
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA 結構舊版 Windows 環境功能
- PMPEXPIRATION_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f270b7d433e6de7cd1eb3e7a3cfc88c9cb85c6087c20371ac804ec61d949d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976028"
---
# <a name="mpexpiration_data-structure"></a>MPEXPIRATION \_ 資料結構

產品到期狀態通知。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**原因**
</dt> <dd>

類型： **MP \_ 過期 \_ 原因**

</dd> <dd>

到期原因。 這是下列其中一個可能的值：



| 值                                                                                                                                                                                                                                | 意義                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**MP \_過期的 \_ 未知**</dt> <dt>0</dt> </dl> | 未知。<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**MP \_過期的 \_ EVAL**</dt> <dt>1</dt> </dl>          | 評價。<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**MP \_過期的 \_ WAT**</dt> <dt>2</dt> </dl>             | 笏。<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

類型： **MP \_ 過期 \_ 狀態 \_ 報告**

</dd> <dd>

過期狀態。 這是下列其中一個可能的值：



| 值                                                                                                                                                                                                                                                                      | 意義                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**MP \_過期 \_ 狀態 \_ 報表 \_ 不明**</dt> <dt>0</dt> </dl> | 未知的狀態。<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**MP \_過期 \_ 狀態 \_ 報告 \_ 有效**</dt> <dt>1</dt> </dl>       | 沒有到期日。<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**MP \_過期 \_ 狀態 \_ 報告 \_ 警告**</dt> <dt>2</dt> </dl> | 即將到期。<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**MP \_過期 \_ 狀態 \_ 報告已 \_ 過期**</dt> <dt>3</dt> </dl> | 過期。<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





