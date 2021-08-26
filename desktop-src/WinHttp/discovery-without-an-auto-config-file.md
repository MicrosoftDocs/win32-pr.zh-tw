---
description: 如果未在區域網路上部署 proxy 自動設定檔案，WinHttpGetProxyForUrl 就會找不到 proxy 伺服器。
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: 沒有自動設定檔的探索
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553f4f798a821ff219b587c494d5dccfbba8c4b22efd0d1692ca2069f53041de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097938"
---
# <a name="discovery-without-an-auto-config-file"></a>沒有自動設定檔的探索

如果未在區域網路上部署 proxy 自動設定檔案， [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 就會找不到 proxy 伺服器。 如果 **WinHttpGetProxyForUrl** 失敗，則會根據其執行時間環境，取得可取得可行 proxy 設定的一些可能回溯策略。 這些包括提示您透過使用者介面進行 proxy 設定、要求某人使用 WinHTTP "ProxyCfg.exe" 公用程式將 proxy 設定儲存在登錄中，或使用 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) 來檢查 proxy 伺服器是否列在 Internet Explorer 的設定中。

由於用戶端具有直接網際網路連線（例如透過 ISP），而且不需要 proxy 伺服器，因此可能沒有 proxy 自動設定檔案。

相反地，可能需要 proxy 伺服器，但區域網路可能不支援 WPAD。 在此情況下，必須從使用者取得 proxy 設定，或在用戶端電腦上找到它。

在仲介層伺服器環境中執行的 WinHTTP 應用程式（例如 COM + 或 ASP 應用程式）應該依賴伺服器管理員，在登錄中使用 "ProxyCfg.exe" 公用程式設定預設 proxy 設定。 然後，您可以使用 [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)函式來抓取此預設設定資訊，或直接在 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)呼叫中指定 **WINHTTP \_ 存取 \_ 類型 \_ PRECONFIG** 旗標。

另一方面，在用戶端桌上型電腦上執行的 WinHTTP 應用程式可能會嘗試檢查 Internet Explorer 的 proxy 設定。 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) 會在目前使用中連線 (撥號、VPN 或 LAN) 的目前使用者 Internet Explorer PROXY 設定中，填入呼叫端提供的 [**WINHTTP \_ 目前 \_ 使用者 \_ IE \_ PROXY \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) 設定結構。 這項設定可能表示使用自動偵測，或可能指定 proxy 自動設定檔案的 URL，或者可以指定要使用的實際 proxy 伺服器，或指定三個的組合。 如果此資訊包含 PAC URL 或 proxy 伺服器，WinHTTP 應用程式可以嘗試使用這些 URL。

您可以在平臺軟體發展工具組 (SDK) WinHTTP 範例中找到使用 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 和 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) 函數的範例。

 

 



