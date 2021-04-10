---
title: 'MPRESOLVED_REASON 列舉 (MpClient .h) '
description: 解決補救失敗的可能原因。
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON 列舉舊版 Windows 環境功能
- PMPRESOLVED_REASON 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025261"
---
# <a name="mpresolved_reason-enumeration"></a>MPRESOLVED \_ 原因列舉

解決補救失敗的可能原因。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**未知的 MPRESOLVED \_ 原因 \_**
</dt> <dd>

處於錯誤狀態。

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED \_ 原因 \_ 完整 \_ 掃描**
</dt> <dd>

已執行完整掃描。

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED \_ 原因已 \_ 超時 \_**
</dt> <dd>

經過的時間已足夠。 預設值為一周。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





