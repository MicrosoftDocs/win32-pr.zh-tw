---
description: WinHTTP 記錄可以用來協助針對 WSDAPI 應用程式進行疑難排解。 當中繼資料交換失敗或 SSL/TLS 協商失敗時，這會很有説明。
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: 正在捕獲 WinHTTP 記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115028"
---
# <a name="capturing-winhttp-logs"></a>正在捕獲 WinHTTP 記錄檔

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) 記錄可以用來協助針對 WSDAPI 應用程式進行疑難排解。 當中繼資料交換失敗或 SSL/TLS 協商失敗時，這會很有説明。

此程式說明如何在用戶端電腦上捕獲 WinHTTP 記錄檔。 啟用記錄時，不能執行以 WSDAPI 為基礎的用戶端應用程式。 如果用戶端應用程式在啟用記錄功能時執行，則必須先重新開機用戶端和/或電腦，才能 WS-Discovery 和中繼資料交換流量將會出現在 WinHTTP 記錄檔中。

**若要捕獲 WinHTTP 記錄檔**

1.  在用戶端電腦上開啟提高許可權的命令提示字元視窗。
2.  執行下列命令： **netsh winHTTP set 追蹤 trace-file-prefix = "C： \\ Temp \\ dpws" level = verbose format = ansi state = enabled max-trace-file-size = 1073741824**

    此命令會啟用 WinHTTP 記錄。 所有記錄檔都會儲存在 C： \\ Temp 目錄中，而且檔案名會以 dpws 前置詞開頭。 最多會儲存 1 GB 的記錄檔。

3.  如果在用戶端上使用 WinHTTP 的進程已在執行中，請重新開機電腦。 例如，如果使用的是 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal) api，則必須重新開機電腦。 函式探索 Api 會從服務主機內部呼叫 WinHTTP，在啟用追蹤時可能已經啟動。
4.  啟動以 WSDAPI 為基礎的用戶端應用程式。 您可以使用正在進行調試的應用程式或 WSD Debug 用戶端。
5.  重現應用程式失敗。
6.  終止以 WSDAPI 為基礎的用戶端應用程式。
7.  如果使用 WinHTTP 的進程未與用戶端應用程式一起終止，請重新開機電腦。 例如，如果使用的是 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal) api，則必須重新開機電腦。
8.  執行下列命令： **netsh winHTTP set 追蹤 state = disabled**

    此命令會停用 WinHTTP 記錄。

9.  檢查 C： Temp 中的 DPWS 記錄 \\ ，並確認已傳送所需的要求和訊息。
10. 如果正在使用安全通道 (HTTPS) 通訊，請檢查 SSL/TLS 是否失敗。

一旦捕捉到 WinHTTP 記錄檔，就可以檢查記錄以尋找 WSDAPI 應用程式失敗的原因。 請注意，用來查看這些記錄的文字編輯器必須以系統管理員身分執行。 如需詳細資訊，請參閱 [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
