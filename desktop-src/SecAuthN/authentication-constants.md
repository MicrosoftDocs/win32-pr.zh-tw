---
description: 列出用於 Microsoft 驗證 Api 的常數。
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: '驗證常數 (驗證) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985033"
---
# <a name="authentication-constants-authentication"></a>驗證常數 (驗證) 

## <a name="credentials-management-constants"></a>認證管理常數

認證管理會使用下列常數來指定字串大小上限。



| 常數                                        | 描述                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| CREDUI \_ \_ 訊息 \_ 長度上限<br/>         | [**CREDUI \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)結構的 **pszMessageText** 成員最大字元數。<br/> |
| CREDUI \_ 最大 \_ 標題 \_ 長度<br/>         | [**CREDUI \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)結構的 **pszCaptionText** 成員最大字元數。<br/> |
| CREDUI \_ 最大 \_ 泛型 \_ 目標 \_ 長度<br/> | 字串中指定目標名稱的最大字元數。<br/>                                             |
| CREDUI \_ 最大 \_ 網域 \_ 目標 \_ 長度<br/>  | 字串中指定功能變數名稱的最大字元數。<br/>                                             |
| CREDUI \_ 使用者 \_ 名稱 \_ 長度上限<br/>        | 字串中指定使用者帳戶名稱的最大字元數。<br/>                                       |
| CREDUI \_ \_ 密碼 \_ 長度上限<br/>        | 字串中指定密碼的最大字元數。<br/>                                                |



 

## <a name="gina-defined-values"></a>Gina 定義的值

[*GINA*](/windows/desktop/SecGloss/g-gly) 介面函式和 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 支援函數會使用下列定義的值。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 



| 值                                                              | 描述                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**WLX \_ LOGON \_ 選項 \_ XXX**](wlx-logon-option-xxx.md)<br/> | 包含預先定義的登入選項。 [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)的 *>dwoptions* 參數會使用它。<br/> |
| [**WLX \_ SAS \_ 類型 \_ XXX**](wlx-sas-type-xxx.md)<br/>         | 定義特定的 SAS 類型。<br/>                                                                                              |



 

 

