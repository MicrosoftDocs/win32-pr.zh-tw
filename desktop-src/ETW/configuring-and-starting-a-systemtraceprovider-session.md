---
description: SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: 設定並啟動 SystemTraceProvider 會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972228"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>設定並啟動 SystemTraceProvider 會話

SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。 在 Windows 7 和 Windows Server 2008 R2 上，SystemTraceProvider 只能用於 NT Kernel 記錄器會話。

在 Windows 8、Windows Server 2012 和更新版本上，SystemTraceProvider 最多可多工記錄，最多8個記錄器會話。 記錄器會話的前兩個位置是保留給 NT 核心記錄器和圓形核心內容記錄器。

如需使用 NT Kernel 記錄器會話作為追蹤提供者的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。

若要讓 SystemTraceProvider 啟動 NT Kernel 記錄器以外的會話，請執行下列命令。

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

<dl> <dt>

[設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[設定和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[更新事件追蹤會話](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
