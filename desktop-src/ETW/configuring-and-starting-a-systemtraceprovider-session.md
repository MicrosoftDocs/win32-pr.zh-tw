---
description: SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: 設定並啟動 SystemTraceProvider 會話
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386738"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>設定並啟動 SystemTraceProvider 會話

SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。 在 Windows 7 和 Windows Server 2008 R2 上，SystemTraceProvider 只能用於 NT Kernel 記錄器會話。

在 Windows 8、Windows Server 2012 和更新版本上，SystemTraceProvider 最多可多工記錄，最多8個記錄器會話。 記錄器會話的前兩個位置是保留給 NT 核心記錄器和圓形核心內容記錄器。

如需使用 NT Kernel 記錄器會話作為追蹤提供者的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。

在 Windows 10 SDK 組建20348和更新版本上，您可以透過個別的系統提供者來設定 SystemTraceProvider，這些提供者可以使用 [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) （例如 Windows 事件提供者的標準事件追蹤）來控制。 如需系統提供者、關鍵字以及對應的舊版旗標和群組的完整清單，請參閱 [系統提供者](system-providers.md)

## <a name="enable-a-systemtraceprovider-session"></a>啟用 SystemTraceProvider 會話

若要讓 SystemTraceProvider 啟動 NT Kernel 記錄器以外的會話，請執行下列命令：

**tracelog.exe-start MySession-f c： \\ Kernel1 .etl-EFLAG PROC \_ THREAD + LOADER + CSWITCH**

若要以程式設計方式啟用 SystemTraceProvider 來啟動 NT Kernel 記錄器以外的會話，請使用下列步驟。

-   定義私用記錄器名稱。

    **\#定義私用 \_ 記錄器 \_ 名稱 L "部分私用追蹤會話"**

-   在控制器上，設定 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的下列成員。

    將 **LogFileMode** 設定為 **事件 \_ 追蹤 \_ 系統 \_ 記錄器 \_ 模式**。

    將 **LoggerName** 設定為私用記錄器，而不是 **核心 \_ 記錄器 \_ 名稱**。

    請確定 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **Wnode Guid** 成員未設定為 **SystemTraceControlGuid**。 您必須將新的 **GUID** 指派給這個成員。

-   在取用者上，將 [**事件 \_ 追蹤 \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea)記錄檔結構的 **LoggerName** 成員設定至此私用記錄器。

> [!Note]  
> 如果您想要讓非系統管理員或非 TCB 進程可以代表協力廠商應用程式使用 SystemTraceProvider 來啟動程式碼剖析追蹤會話，則您需要授與使用者設定檔許可權，然後將此使用者新增至為記錄器會話建立的會話 **GUID** () 和系統追蹤提供者 **GUID** ，以啟用系統追蹤提供者。 如需詳細資訊，請參閱 [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) 函數。

 

## <a name="related-topics"></a>相關主題

[設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)

[設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)

[設定和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)

[設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)

[系統提供者](system-providers.md)

[更新事件追蹤會話](updating-an-event-tracing-session.md)

 

 
