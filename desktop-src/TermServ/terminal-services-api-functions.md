---
title: 遠端桌面服務 API 函數
description: 下列函式會搭配遠端桌面服務使用。
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682527"
---
# <a name="remote-desktop-services-api-functions"></a>遠端桌面服務 API 函數

下列函式會搭配遠端桌面服務使用。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

抓取與指定進程相關聯的遠端桌面服務會話。

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

開啟指定之遠端桌面授權伺服器的控制碼。

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

關閉遠端桌面授權伺服器的開啟控制碼。

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

傳回到遠端桌面授權伺服器的憑證。

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

根據搜尋準則，在遠端桌面授權伺服器上安裝的所有金鑰套件開始列舉。

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

從先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫繼續，然後終止列舉。

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

繼續進行先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個金鑰套件。

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

根據搜尋準則開始列舉遠端桌面授權伺服器所發行的授權。

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

從先前的 [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) 函式呼叫繼續，然後終止列舉。

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

繼續進行先前的 [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個授權。

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

關閉虛擬通道的用戶端。

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

應用程式的用戶端 DLL 的應用程式定義進入點，此應用程式會使用遠端桌面服務的虛擬通道。

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

初始化用戶端 DLL 對遠端桌面服務虛擬通道的存取。

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

應用程式定義的回呼函式，遠端桌面服務呼叫以通知用戶端 DLL 的虛擬通道事件。

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

開啟虛擬通道的用戶端。

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

遠端桌面服務呼叫的應用程式定義回呼函式，以通知用戶端 DLL 特定虛擬通道的事件。

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

將資料從虛擬通道的用戶端端傳送到伺服器端上的夥伴應用程式。

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

關閉遠端桌面工作階段主機 (RD 工作階段主機) server 的開啟控制碼。

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

將遠端桌面服務會話連接到本機電腦上的現有會話。

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

建立新的遠端桌面服務接聽程式，或設定現有的接聽程式。

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

中斷已登入的使用者與指定的遠端桌面服務會話的連線，而不關閉會話。

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

啟用或停用 [子會話](child-sessions.md)。

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

列舉 RD 工作階段主機伺服器上的所有遠端桌面服務接聽程式。

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

抓取指定 RD 工作階段主機伺服器上使用中進程的相關資訊。

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

抓取指定 RD 工作階段主機伺服器上的作用中進程的相關資訊，或 (RD 虛擬化主機) 伺服器上的遠端桌面虛擬化主機。

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

傳回指定網域內所有 RD 工作階段主機伺服器的清單。

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

抓取 RD 工作階段主機伺服器上的會話清單。

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

抓取指定 RD 工作階段主機伺服器或 RD 虛擬化主機伺服器上的會話清單。

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

釋出遠端桌面服務函數所配置的記憶體。

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

釋放包含 [**WTS \_ 處理 \_ 資訊 \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) 的記憶體，例如 [**或 \_ WTS 會話 \_ 資訊 \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) 結構（由遠端桌面服務函式所配置）。

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

抓取主控台會話的會話識別碼。

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

抓取子會話識別碼（如果有的話）。

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

抓取遠端桌面服務接聽程式的安全描述項。

</dd> <dt>

[**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

判斷子會話是否已啟用。

</dd> <dt>

[**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

登出指定的遠端桌面服務會話。

</dd> <dt>

[**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

開啟指定 RD 工作階段主機伺服器的控制碼。

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

開啟指定的 RD 工作階段主機伺服器或 RD 虛擬主機伺服器的控制碼。

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

抓取遠端桌面服務接聽程式的設定資訊。

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

抓取指定 RD 工作階段主機伺服器上指定之會話的會話資訊。

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

抓取指定網域控制站或 RD 工作階段主機伺服器上指定之使用者的設定資訊。

</dd> <dt>

[**WTSQueryUserToken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

取得會話識別碼所指定之已登入使用者的主要存取權杖。

</dd> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

註冊指定的視窗，以接收會話變更通知。

</dd> <dt>

[**WTSRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

註冊指定的視窗，以接收會話變更通知。

</dd> <dt>

[**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

在指定的遠端桌面服務會話的用戶端桌面上顯示訊息方塊。

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

設定遠端桌面服務接聽程式的安全描述項。

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

修改指定網域控制站或 RD 工作階段主機伺服器上指定之使用者的設定資訊。

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

關閉 (，並選擇性地重新開機) 指定的 RD 工作階段主機伺服器。

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

啟動另一個遠端桌面服務會話的遠端控制。 您必須從遠端會話呼叫這個函數。

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

停止遠端控制會話。

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

終止指定的 RD 工作階段主機伺服器上指定的進程。

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

取消註冊指定的視窗，使其不會收到任何進一步的會話變更通知。

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

取消註冊指定的視窗，使其不會收到任何進一步的會話變更通知。

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

關閉開啟的虛擬通道控制碼。

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

開啟指定虛擬通道之伺服器端的控制碼。

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

以類似于 [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)的方式建立虛擬通道。

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

刪除從用戶端傳送到指定虛擬通道上伺服器的所有已排入佇列的輸入資料。

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

刪除從伺服器傳送至指定虛擬通道上之用戶端的所有已排入佇列的輸出資料。

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

傳回指定虛擬通道的相關資訊。

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

從虛擬通道的伺服器端讀取資料。

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

將資料寫入虛擬通道的伺服器端。

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

先等候遠端桌面服務事件，再返回呼叫端。

</dd> </dl>

 

 