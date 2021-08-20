---
description: 值會定義特定的 SAS 類型。
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: 'WLX_SAS_TYPE_XXX (Winwlx) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 568308d064b576f036d18aaa2d150cb1c6b7f0a2d89ee60d9410fcad123351d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785710"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ 類型 \_ XXX

\[WLX \_ SAS \_ 類型 \_ XXX 常數不再適用于 Windows Server 2008 和 Windows Vista 的使用。\]

**WLX \_ SAS \_ 類型 \_ XXX** 值會定義特定的 sas 類型。

> [!Note]  
> Windows Vista 會忽略 GINA dll。

 

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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                               |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winwlx。h</dt> </dl> |



 

 
