---
description: WlxLoggedOutSAS 的 >dwoptions 參數會使用值。
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: 'WLX_LOGON_OPTION_XXX (Winwlx) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae482fa7af757a18fc3a38f809befbee94e4d59753cde8e35e01d172bcc065d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914757"
---
# <a name="wlx_logon_option_xxx"></a>WLX \_ LOGON \_ 選項 \_ XXX

\[WLX \_ LOGON \_ 選項 \_ XXX 常數不再適用于 Windows Server 2008 和 Windows Vista 的使用。\]

**WLX \_ LOGON \_ 選項 \_ XXX** 值是由 [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)的 *>dwoptions* 參數使用。

> [!Note]  
> Windows Vista 會忽略 GINA dll。

 

成功登入時，您的 GINA DLL 可以使用此值來指定下列選項。



| 常數                                                                                                                                                                                          | 描述                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**WLX \_ 登入 \_ 選擇 \_ 沒有 \_ 設定檔**</dt> </dl> | 指定 Winlogon 不得為登入的使用者載入設定檔。 在此情況下，您的 GINA DLL 將會載入設定檔，或使用者不需要設定檔。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                               |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winwlx。h</dt> </dl> |



 

 




