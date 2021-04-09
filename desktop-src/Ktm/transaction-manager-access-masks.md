---
description: KTM 會定義在開啟交易管理員 (TM) 時要使用的下列登記存取遮罩。
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: '交易管理員存取遮罩 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849015"
---
# <a name="transaction-manager-access-masks"></a>交易管理員存取遮罩

KTM 會定義在開啟交易管理員 (TM) 時要使用的下列登記存取遮罩。

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER \_ 查詢 \_ 資訊**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



呼叫者可以查詢此 TM 的相關資訊。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER \_ 設定 \_ 資訊**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



呼叫者可以設定此 TM 的相關資訊。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER \_ 復原**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



呼叫者可以復原此 TM。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER \_ 重新命名**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



呼叫端可以重新命名 TM 實例。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ 建立 \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



呼叫者可以建立與此 TM 相關聯的資源管理員。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER 系結 \_ \_ 交易**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



此值為 reserved。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**將 \_ 一般 \_ 讀取**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 讀取** 和 **TRANSACTIONMANAGER \_ 查詢 \_ 資訊**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER \_ 泛型 \_ 寫入**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 寫入**、 **transactionmanager \_ 設定 \_ 資訊**、 **transactionmanager \_ 復原**、 **TRANSACTIONMANAGER \_ 重新命名** 和 **transactionmanager \_ 建立 \_ RM**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER \_ 泛型 \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



呼叫端具有下列許可權： **標準 \_ 許可權 \_ 執行**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ 所有 \_ 存取**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



此值會設定 TM 存取值的所有有效位。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                           |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinNT。h</dt> </dl> |



 

 




