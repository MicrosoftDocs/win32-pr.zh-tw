---
title: 建立連至網際網路的撥號連線
description: 下列函式是用來處理數據機連接。
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955588"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>建立連至網際網路的撥號連線

下列函式是用來處理數據機連接。

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> WinINet 撥號函式不支援雙撥號連線、智慧卡驗證，或需要以登錄為基礎之認證的連線。

 

> [!Note]  
> 從 Windows Vista 和 Windows Server 2008 開始，WinINet 撥號函式會使用[RAS 函數](/windows/desktop/RRAS/remote-access-service-functions)來建立撥號連線。 WinINet 支援 [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) 函式中記載的功能。

 

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 