---
description: WlxLoggedOutSAS 的 >dwoptions 參數會使用值。
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: 'WLX_LOGON_OPTION_XXX (Winwlx) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319831"
---
# <a name="wlx_logon_option_xxx"></a>WLX \_ LOGON \_ 選項 \_ XXX

\[WLX \_ LOGON \_ 選項 \_ XXX 常數不再適用于 windows Server 2008 和 windows Vista 的使用。\]

**WLX \_ LOGON \_ 選項 \_ XXX** 值是由 [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)的 *>dwoptions* 參數使用。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 

成功登入時，您的 GINA DLL 可以使用此值來指定下列選項。



| 常數                                                                                                                                                                                          | 描述                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**WLX \_ 登入 \_ 選擇 \_ 沒有 \_ 設定檔**</dt> </dl> | 指定 Winlogon 不得為登入的使用者載入設定檔。 在此情況下，您的 GINA DLL 將會載入設定檔，或使用者不需要設定檔。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                               |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winwlx。h</dt> </dl> |



 

 




