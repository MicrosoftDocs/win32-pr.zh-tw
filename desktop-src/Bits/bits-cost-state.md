---
title: 'BITS_COST_STATE (Bits5 \_ 0 .h) '
description: BITS \_ 成本 \_ 狀態列舉定義指定 BITS 成本狀態的常數值。
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: ecbe54966a54310af71a4c96a3d3c2423f524f9b8a8067b10350fba05675a54b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701978"
---
# <a name="bits_cost_state"></a>BITS \_ 成本 \_ 狀態

定義指定 BITS 成本狀態的常數。

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**不 \_ \_ \_ 受限制的 BITS 成本狀態**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**BITS \_ 成本 \_ 狀態 \_ 上限 \_ 使用 \_ 不明**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**\_ \_ \_ 低於上限的 BITS 成本狀態 \_**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**BITS \_ 成本 \_ 狀態 \_ 接近 \_ 上限**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**BITS \_ 成本 \_ 狀態 \_ OVERCAP \_ 收費**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**BITS \_ 成本 \_ 狀態 \_ OVERCAP 已 \_ 節流**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**\_依 BITS 成本 \_ 狀態 \_ 使用量 \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**BITS \_ 成本 \_ 選項 \_ 忽略 \_ 擁塞**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**保留的 BITS \_ 成本 \_ 狀態 \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



保留的。


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**BITS \_ 成本 \_ 狀態 \_ 傳輸 \_ 未 \_ 漫遊**
</dt> <dd> <dl> <dt>

 (BITS \_ 成本 \_ 選項 \_ 忽略 \_ 擁塞 \| 位 \_ 成本 \_ 狀態 \_ 使用方式的 \_ \| bits \_ 成本 \_ 狀態 \_ OVERCAP 節流處理的 \_ \| 位 \_ 成本 \_ 狀態 OVERCAP 依 \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_) cap bits 成本狀態接近上限 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**BITS \_ 成本 \_ 狀態 \_ 傳輸 \_ 沒有 \_ 額外費用**
</dt> <dd> <dl> <dt>

 (BITS \_ 成本 \_ 選項 \_ 忽略 \_ 擁塞 \| 位 \_ 成本 \_ 狀態 \_ 使用方式的 \_ \| bits \_ 成本 \_ 狀態 OVERCAP 節流 bits 成本狀態 \_ \_ \| \_ \_ \_ 接近 \_ cap bits 的成本狀態 \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_) 上限
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**BITS \_ 成本 \_ 狀態 \_ 傳輸 \_ 標準**
</dt> <dd> <dl> <dt>

 (BITS \_ 成本 \_ 選項 \_ 忽略 \_ 擁塞 \| 位 \_ 成本 \_ 狀態 \_ 使用方式的 \_ \| bits \_ 成本 \_ 狀態 \_ OVERCAP \_ 節流的 \| 位成本狀態 \_ \_ \_ 低於 \_ CAP \| bits \_ 成本 \_ 狀態 \_ 上限 \_ 使用未知的 \_ \| bits \_ 成本狀態不 \_ \_ 受限制)  
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**不 \_ 受限制的 BITS 成本 \_ 狀態 \_ 傳輸 \_**
</dt> <dd> <dl> <dt>

 (BITS \_ 成本 \_ 選項 \_ 忽略 \_ 擁塞 \| 位 \_ 成本 \_ 狀態 \_ OVERCAP \_ 節流 \| 位不 \_ 受限制的 bits 成本 \_ 狀態 \_) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**BITS \_ 成本 \_ 狀態 \_ 一律為傳輸 \_**
</dt> <dd> <dl> <dt>

 (BITS \_ 成本 \_ 選項 \_ 忽略 \_ 擁塞 \| 位 \_ 成本 \_ 狀態 \_ 漫遊 \| 位 \_ 成本狀態使用方式的 \_ \_ \_ \| bits \_ 成本 \_ 狀態 \_ OVERCAP \_ 節流 \| bits \_ 成本 \_ 狀態 \_ OVERCAP \_ 收費的 \| bits 成本狀態 \_ \_ \_ 接近 \_ cap \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_) bits 成本
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Bits5 \_ 0 .h (包含 bit .h) </dt> </dl> |
| IDL<br/>                      | <dl> <dt>Bits5 \_ 0 .idl</dt> </dl>                |



 

 





