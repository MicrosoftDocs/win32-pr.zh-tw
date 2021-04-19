---
title: 遠端桌面服務管理
description: 遠端桌面服務 API 可讓您列舉和管理遠端桌面工作階段主機 (RD 工作階段主機) 伺服器、用戶端會話和進程。
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e763a652335c85931225746334bc21db0e6e086d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965245"
---
# <a name="remote-desktop-services-administration"></a>遠端桌面服務管理

遠端桌面服務 API 可讓您列舉和管理遠端桌面工作階段主機 (RD 工作階段主機) 伺服器、用戶端會話和進程。

若要取出網域中所有 RD 工作階段主機伺服器的名稱，請呼叫 [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) 函式來列舉 SV \_ 類型 TERMINALSERVER 類型的伺服器 \_ 。 若要開啟特定 RD 工作階段主機伺服器的控制碼，請在 [**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) 函式的呼叫中傳遞伺服器名稱。 當您完成使用控制碼時，請呼叫 [**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) 函式來釋放它。

您可以使用 **WTSOpenServer** 所傳回的控制碼，在伺服器上執行下列作業。



| 函式                                                         | 作業                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | 中斷用戶端與指定會話的連線。 會話仍維持使用中狀態，且使用者可以重新登入以連接到相同的會話。                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | 傳回指定 RD 工作階段主機伺服器上的會話清單。                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | 傳回指定 RD 工作階段主機伺服器上的進程清單。                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | 登出指定的會話。                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | 傳回指定 RD 工作階段主機伺服器上指定之會話的相關資訊。                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | 在用戶端顯示指定的會話時顯示訊息方塊。                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | 關閉並選擇性地重新開機指定的 RD 工作階段主機伺服器。                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | 終止指定 RD 工作階段主機伺服器上的指定進程。                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | 開啟指定虛擬通道之伺服器端的控制碼。 如需虛擬通道的詳細資訊，請參閱 [使用遠端桌面服務虛擬通道](using-terminal-services-virtual-channels.md)。 |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | 等候事件，例如建立用戶端會話或登入 RD 工作階段主機 server 的使用者。                                                                                                  |



 

其中有幾個函式會配置緩衝區，以將資訊傳回給呼叫者。 當您完成使用緩衝區時，請呼叫 [**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) 函式來釋放它。

 

 