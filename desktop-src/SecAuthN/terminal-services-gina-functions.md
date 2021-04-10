---
description: 啟用終端機服務時，GINA 必須呼叫 Winlogon 支援函式來完成每個使用者的設定、查詢終端機服務用戶端會話的認證，以及中斷與終端機服務網路會話的連線。注意 GINA 在 Windows Vista 中會忽略 Dll。
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: 終端機服務 GINA 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847931"
---
# <a name="terminal-services-gina-functions"></a>終端機服務 GINA 函式

啟用終端機服務時， [*GINA*](../secgloss/g-gly.md) 必須呼叫 [*Winlogon*](../secgloss/w-gly.md) 支援函式來完成每個使用者的設定、查詢終端機服務用戶端會話的 [*認證*](../secgloss/c-gly.md) ，以及中斷與終端機服務網路會話的連線。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 

這些支援函數包括下列各項。



| 函式                                                                     | 描述                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | 完成使用者的設定。                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | 呼叫以查詢未使用網際網路連接器授權之遠端用戶端的認證。 |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | 呼叫以查詢使用網際網路連接器授權之遠端用戶端的認證。     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | 呼叫以取得終端機服務使用者設定資訊。                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | 呼叫以中斷與終端機服務網路會話的連線。                                      |



 

為了存取這些 Winlogon 支援函數，GINA DLL 必須使用 [**WLX \_ 分派 \_ \_ 第 1 \_ 版**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) 的結構。 在 GINA 的 [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) 函式中，這兩個參數至少必須是 WLX \_ \_ 第1版 \_ 。

 

 
