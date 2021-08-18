---
title: 遠端桌面服務 API 列舉類型
description: 列出搭配遠端桌面服務 API 使用的列舉類型。
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5b6dcb4ee772969e374eeda5c12edca09cebddef3c9a6c8378b144b7ba2819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000258"
---
# <a name="remote-desktop-services-api-enumeration-types"></a>遠端桌面服務 API 列舉類型

下列列舉類型會與遠端桌面服務 API 搭配使用。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**WTS \_CONFIG \_ 類別**](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

包含值，這些值表示在呼叫 [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) 和 [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) 函數時要設定或抓取的使用者設定資訊類型。

</dd> <dt>

[**WTS \_CONFIG \_ 來源**](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

指定 [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) 函數所傳回的設定資訊來源。

</dd> <dt>

[**WTS \_CONNECTSTATE \_ 類別**](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

指定遠端桌面服務會話的連接狀態。

</dd> <dt>

[**WTS \_INFO \_ 類別**](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

包含值，這些值表示在呼叫 [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) 函式時要取出的會話資訊類型。

</dd> <dt>

[**WTS \_型別 \_ 類別**](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

指定遠端桌面服務函數已在緩衝區中傳回的結構類型。

</dd> <dt>

[**WTS \_虛擬 \_ 類別**](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

包含值，這些值表示要取出的虛擬通道資訊類型。

</dd> <dt>

[**WTSSBX \_ 位址 \_ 系列**](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

包含值，這些值表示用於重新導向之網路位址的位址系列。

</dd> <dt>

[**WTSSBX \_ 機器 \_ 清空**](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

包含值，指出遠端桌面工作階段主機 (RD 工作階段主機) server 的清空狀態。

</dd> <dt>

[**WTSSBX \_ 機器 \_ 會話 \_ 模式**](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

包含值，指出 RD 工作階段主機伺服器的會話模式。

</dd> <dt>

[**WTSSBX \_ 電腦 \_ 狀態**](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

包含表示伺服器目前狀態的值。

</dd> <dt>

[**WTSSBX \_ 通知 \_ 類型**](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

包含值，指出 RD 工作階段主機伺服器或使用者會話上發生的狀態變更類型。

</dd> <dt>

[**WTSSBX \_ 會話 \_ 狀態**](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

包含值，這些值表示使用者會話的連接狀態。

</dd> </dl>

 

 




