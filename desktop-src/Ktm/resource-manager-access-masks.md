---
description: KTM 定義了在開啟資源管理員時要使用的下列登記存取遮罩。
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: 'Resource Manager 存取遮罩 (WinNT) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115401"
---
# <a name="resource-manager-access-masks"></a>Resource Manager 存取遮罩

KTM 定義了在開啟資源管理員時要使用的下列登記存取遮罩。

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER \_ 查詢 \_ 資訊**
</dt> <dd> <dl> <dt>



呼叫端可以查詢資源管理員 (RM) 資訊。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER \_ 設定 \_ 資訊**
</dt> <dd> <dl> <dt>



呼叫端可以設定 RM 資訊。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER \_ 復原**
</dt> <dd> <dl> <dt>



呼叫端可以復原指定的 RM。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER \_ 登錄**
</dt> <dd> <dl> <dt>



呼叫端可以在交易中登記 RM。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER \_ 取得 \_ 通知**
</dt> <dd> <dl> <dt>



呼叫端可能會收到 RM 的通知。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER \_ 一般 \_ 讀取**
</dt> <dd> <dl> <dt>



呼叫端具有下列許可權：標準 \_ 許可權 \_ 讀取、RESOURCEMANAGER \_ 查詢 \_ 資訊，以及 RESOURCEMANAGER \_ 復原。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER \_ 一般 \_ 寫入**
</dt> <dd> <dl> <dt>



呼叫端具有下列許可權：標準 \_ 許可權 \_ 寫入、resourcemanager \_ 設定 \_ 資訊、resourcemanager 登錄 \_ 和 RESOURCEMANAGER \_ 取得 \_ 通知。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER \_ 泛型 \_ 執行**
</dt> <dd> <dl> <dt>



呼叫端具有下列許可權：標準 \_ 許可權 \_ 執行、RESOURCEMANAGER 登錄 \_ 和 RESOURCEMANAGER \_ 取得 \_ 通知。


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER \_ 所有 \_ 存取**
</dt> <dd> <dl> <dt>



呼叫端具有下列許可權：需要標準 \_ 許可權 \_ 。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                           |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>WinNT。h</dt> </dl> |



 

 




