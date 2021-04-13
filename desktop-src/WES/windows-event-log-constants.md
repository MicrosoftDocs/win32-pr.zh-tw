---
title: 'Windows 事件記錄檔常數 (\System32\winevt\logs\application.evtx .h) '
description: Windows 事件記錄檔會定義下列常數
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384613"
---
# <a name="windows-event-log-constants"></a>Windows 事件記錄檔常數

Windows 事件記錄檔會定義下列常數：

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**.EVT \_ VARIANT \_ 類型 \_ 遮罩**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



用來將 variant 類型的陣列位遮罩的位元遮罩，讓您可以判斷 [**.Evt \_ variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) 結構包含的 variant 值的資料類型。


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**.EVT \_ VARIANT \_ 類型 \_ 陣列**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



如果變數包含值陣列的指標，而不是值本身，則 [**.Evt \_ VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant)結構的 **類型** 成員會設定此位。


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**.EVT \_ 讀取 \_ 許可權**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



讀取存取控制許可權，允許從事件記錄檔讀取資訊。


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**.EVT \_ 寫入 \_ 許可權**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



寫入存取控制許可權，允許將資訊寫入事件記錄檔。


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**.EVT \_ 清楚 \_ 存取**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



清除存取控制許可權，允許從事件記錄檔中清除所有資訊。


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**.EVT \_ 所有 \_ 存取**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



所有 (讀取、寫入、清除和刪除) 存取控制許可權。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>\System32\winevt\logs\application.evtx。h</dt> </dl> |



 

 





