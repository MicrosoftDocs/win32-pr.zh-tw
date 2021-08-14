---
description: KTM 會定義下列交易存取遮罩，以在開啟交易時使用。
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: '交易存取遮罩 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faafcce45944e37418191254fc5a2b81d00d9248b27ea5e8753fe8e34a734754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520638"
---
# <a name="transaction-access-masks"></a>交易存取遮罩

KTM 會定義下列交易存取遮罩，以在開啟交易時使用。

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**交易 \_ 查詢 \_ 資訊**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



呼叫者可以查詢交易資訊。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**交易 \_ 集 \_ 資訊**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



呼叫端可以設定交易資訊。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**交易 \_ 登記**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



呼叫者可以在此交易中登記。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**交易 \_ 認可**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



呼叫者可以認可此交易。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**交易 \_ 回復**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



呼叫端可以回復此交易。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**交易 \_ 傳播**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



呼叫端可以將此交易傳播至上層資源管理員，例如分散式交易協調器 (DTC) 。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**交易 \_ 一般 \_ 讀取**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 讀取**、 **交易 \_ 查詢 \_ 資訊**，以及 **同步處理**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**交易 \_ 一般 \_ 寫入**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



呼叫端具有下列許可權： **標準的 \_ 許可權 \_ 寫入**、 **交易 \_ 集 \_ 資訊**、 **交易 \_ 認可**、 **交易 \_ 登記**、 **交易 \_ 回復**、 **交易 \_ 傳播** 和 **同步處理**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**交易 \_ 一般 \_ 執行**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 執行**、 **交易 \_ 認可**、 **交易 \_ 回復**，以及 **同步處理**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**交易 \_ 所有 \_ 存取**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



呼叫端具有下列許可權： **需要標準 \_ 許可權 \_**、 **交易 \_ 一般 \_ 讀取**、 **交易 \_ 一般 \_ 寫入** 和 **交易 \_ 一般 \_ 執行**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**交易 \_ 資源 \_ 管理員 \_ 許可權**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



呼叫端具有下列許可權： **交易 \_ 一般 \_ 讀取**、 **標準 \_ 許可權 \_ 寫入**、 **交易 \_ 集 \_ 資訊**、 **交易 \_ 回復**、 **交易 \_ 登記**、 **交易 \_ 傳播**，以及 **同步** 處理。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

當您在交易中登記時，建議使用資源管理員，在開啟交易時指定 **交易 \_ 資源 \_ 管理員 \_ 許可權** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                           |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinNT。h</dt> </dl> |



 

 




