---
description: 值會定義特定的 SAS 類型。
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: 'WLX_SAS_TYPE_XXX (Winwlx) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975397"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ 類型 \_ XXX

\[WLX \_ SAS \_ 類型 \_ XXX 常數不再適用于 windows Server 2008 和 windows Vista 的使用。\]

**WLX \_ SAS \_ 類型 \_ XXX** 值會定義特定的 sas 類型。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 

從零到127的所有值都會保留給 Microsoft 定義的類型。 127以上的值適用于客戶定義的類型。 下列類型會傳遞至具有 *dwSasType* 參數的函式。



| 常數                                                                                                                                                                                                         | 描述                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ CTRL \_ ALT \_ DEL**</dt> </dl>            | 表示使用者已輸入標準 CTRL + ALT + DEL SAS。<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ SC \_ INSERT**</dt> </dl>                      | 指出 [*智慧卡*](../secgloss/s-gly.md) 已插入相容的裝置。<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ SC \_ REMOVE**</dt> </dl>                      | 表示已從相容裝置移除智慧卡。<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ SCRNSVR \_ 活動**</dt> </dl> | 指出當安全的螢幕保護裝置啟用時，鍵盤或滑鼠活動發生。<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ SCRNSVR \_ TIMEOUT**</dt> </dl>    | 指出由於鍵盤和滑鼠非活動而發生螢幕保護裝置啟用。<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ 超時**</dt> </dl>                             | 表示在指定的超時時間內未收到任何使用者輸入。<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**WLX \_ SAS \_ 類型 \_ 使用者 \_ 登出**</dt> </dl>                | 指出正在將使用者登出系統。<br/>                                                                                            |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                               |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winwlx。h</dt> </dl> |



 

 
