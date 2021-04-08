---
title: HTTP Server 2.0 版 API 的新功能
description: HTTP 伺服器版本 2.0 API 提供下列功能。
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- HTTP Server 2.0 版 API 的新功能
- HTTP 伺服器版本 2.0 API，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021065"
---
# <a name="whats-new-for-http-server-version-20-api"></a>HTTP Server 2.0 版 API 的新功能

HTTP 伺服器版本 2.0 API 新增了屬性設定物件和 advanced request queue management。 如需詳細資訊和函式的完整清單，請參閱 [HTTP 伺服器版本2.0 參考](http-server-api-version-2-0-reference.md) 主題。 HTTP 伺服器版本 2.0 API 提供下列功能。

## <a name="configuration-objects"></a>設定物件

伺服器會話和 URL 群組設定物件可讓應用程式設定 HTTP 服務。 伺服器會話是最上層的設定物件，它會覆寫會話下建立之所有 URL 群組的 HTTP 伺服器 API 預設設定。 在伺服器會話下建立的 URL 群組會維護一組可接收群組設定的 Url。 如需詳細資訊，請參閱 [HTTP 版本2.0 架構](http-version-2-0-architecture.md) 主題。

## <a name="property-configuration-in-version-20"></a>2.0 版中的屬性設定

設定是在伺服器會話或 URL 群組物件上執行。 伺服器會話設定物件上會設定整個伺服器的設定。 在伺服器會話下建立的 URL 群組會繼承伺服器會話設定。 在 URL 群組上設定的設定會覆寫伺服器會話設定。 應用程式可以設定的設定包括連接逾時、連線限制、驗證和記錄。 如需詳細資訊，請參閱設定 [HTTP 2.0 版中的屬性](configuring-properties-in-http-version-2-0.md) 主題。

## <a name="process-isolation-on-request-queues"></a>要求佇列上的進程隔離

2.0 版要求佇列支援進程隔離，可讓多個背景工作進程在要求佇列上執行 IO。 在要求佇列上設定的設定屬性，可讓應用程式更充分掌控服務。 命名的要求佇列功能可讓應用程式建立要求佇列，並使用 (ACL) 的存取控制清單來保護它們。 在建立要求佇列的帳戶以外的使用者帳戶下操作的應用程式，可以開啟要求佇列、接收要求和傳送回應。 如需詳細資訊，請參閱 [進程隔離](process-isolation.md) 主題。

## <a name="full-kernel-mode-ssl"></a>完整核心模式 SSL

預設會啟用核心模式 SSL 安全性;也支援相互驗證的用戶端憑證。 藉由在核心模式中完成 SSL 作業來提高效能，進而減少核心和使用者模式之間的轉換。 如需詳細資訊，請參閱 [核心模式 SSL](kernel-mode-ssl.md) 主題。

## <a name="kernel-mode-response-cache"></a>核心模式回應快取

具有靜態內容的回應可在核心模式中快取，以提供比使用者模式快取更高的效能。 快取原則結構會隨著回應傳送。 如需詳細資訊，請參閱 [HTTP 2.0 中的核心模式](kernel-mode-cache-in-http-2-0.md) 快取主題。

## <a name="authentication"></a>驗證

HTTP \_ 回應和 HTTP \_ 要求結構會更新以包含驗證資訊。 下列配置支援伺服器端驗證： Negotiate、NTLM、Basic 和 Digest。 應用程式可以指定支援的驗證配置，並設定這些配置的喜好設定順序。

## <a name="object-scoped-versioning"></a>物件範圍版本控制

HTTP 伺服器版本 1.0 API 在 HTTPInitialize 的呼叫中傳遞了版本資訊。 此版本已針對相同進程中的所有應用程式設定為全域。 在 HTTP 伺服器版本 2.0 API 中，會在建立物件時提供版本資訊。 如需詳細資訊，請參閱 [HTTP Server 2.0 版 API 中](versioning-in-http-2-0.md)的版本設定。

## <a name="logging"></a>記錄

從2.0 版開始，記錄可透過 HTTP 伺服器 API 來設定。 在伺服器會話上啟用記錄可做為服務的集中式記錄形式。 您也可以在個別記錄檔的 URL 群組上啟用記錄。 應用程式會指定記錄檔的格式，以及針對錯誤和成功交易記錄的欄位。

## <a name="graceful-request-queue-shutdown"></a>正常要求佇列關閉

應用程式可以關閉要求佇列，並在終止要求佇列進程之前，正常處理佇列中的未處理要求。 當要求佇列關閉時，HTTP 伺服器 API 會停止佇列要求，並在要求佇列中重新路由未處理的要求。

## <a name="demand-start-on-a-request-queue"></a>要求佇列上的要求開始

要求佇列上的需求啟動功能可讓控制器應用程式延遲工作者進程具現化，直到第一個要求抵達要求佇列為止。 因此，應用程式可以避免耗用資源，直到需要它們為止。 如需詳細資訊，請參閱 [2.0 版要求佇列主題的「需求開始」](demand-start-on-version-2-0-request-queues.md) 主題。

## <a name="port-sharing"></a>埠共用

以 HTTP Server API 為基礎的應用程式會自動與電腦上其他非 HTTP 伺服器 API 型應用程式共用 IP 接聽空間;不再需要 IP 接聽清單。 當應用程式註冊 URL 時，HTTP 伺服器 API 只會在指定的 IP 位址和埠配對上接聽。

## <a name="etw-support"></a>ETW 支援

使用「Windows 事件追蹤」 (ETW) 的 Advanced 追蹤可讓應用程式獲得更高的診斷能力。 事件追蹤適用于 URL 註冊和保留、屬性設定、快取事件、驗證以及記錄等等。

## <a name="performance-counters"></a>效能計數器

效能計數器工具可讓應用程式取出服務計數器，並診斷服務效能。 全域計數器會追蹤服務的效能、site 計數器追蹤 URL 群組效能，以及要求佇列計數器會追蹤要求佇列的效能。

## <a name="international-domain-names-idn"></a> (IDN) 的國際功能變數名稱

URL 的國際化主機和路徑部分允許註冊非 ASCII 功能變數名稱和路徑。 HTTP 伺服器 API 會處理 Unicode Url，以符合 IDN 標準。

## <a name="netsh-extensions"></a>NetSH 擴充功能

Netsh 公用程式會取代 Windows Server 2003 和 Windows XP Service Pack 2 中提供的 HttpCfg.exe 工具 (SP2) 。 Netsh 擴充功能提供管理、診斷和設定 HTTP 服務的方法。 系統管理員可以查詢和設定整個伺服器的設定，例如命名空間註冊和 SSL 憑證。

 

 




