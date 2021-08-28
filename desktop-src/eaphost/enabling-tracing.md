---
title: 啟用 EAPHost 追蹤
description: 可協助使用者找出 EAP 驗證程式期間發生之問題的根本原因。 調試資訊可以包含執行的 API 呼叫、執行的內部函式呼叫，以及執行的狀態轉換。
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c638fa7f546028cd9cf66227cfe3c302d6599492d1cbbfcfdac6c2b428273db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086290"
---
# <a name="enabling-eaphost-tracing"></a>啟用 EAPHost 追蹤

包含偵錯工具資訊的追蹤記錄可協助使用者找出 EAP 驗證程式期間發生之問題的根本原因。 調試資訊可以包含執行的 API 呼叫、執行的內部函式呼叫，以及執行的狀態轉換。

用戶端和驗證端都可以同時啟用追蹤。 也可以對 [路由及遠端存取服務 (RRAS) ](/windows/desktop/RRAS/routing-start-page) api 的呼叫啟用追蹤。 如需詳細資訊，請參閱「 [路由及遠端存取」服務的追蹤](#tracing-on-the-routing-and-remote-access-service)。

> [!Note]  
> 追蹤記錄檔僅提供英文版。

 

啟用 EAPHost 追蹤時，記錄資訊會儲存在使用者指定位置的 .etl 檔案中。 如果在 EAP 驗證期間發生錯誤，追蹤會產生可傳送給 Microsoft 開發人員根本原因分析支援的 .etl 檔案。 具有 Microsoft windows build 共用、符號和 traceformat 檔案存取權的合作夥伴，可以使用 **tracerpt** 工具將 .etl 檔案轉換成純文字檔案。

EAPHost 記錄中不會捕捉網路原則伺服器 (NPS) 失敗。 如果您嘗試針對 NPS 失敗進行疑難排解，請參閱 IASSAM。記錄檔和 [IASNAP。記錄](https://go.microsoft.com/fwlink/p/?linkid=84108) 檔。

## <a name="tracing-on-the-client"></a>用戶端上的追蹤

若要在用戶端上啟用追蹤：

1.  開啟提升權限的命令提示字元視窗。
2.  執行下列命令： **logman** **start trace** **EapHostPeer** **-o** **。 \\EapHostPeer .etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**
3.  重現您要追蹤的情節。
4.  執行下列命令： **logman** **stop** **EapHostPeer** **-ets**
5.  使用下列命令將 etl 檔案轉換成文字： **tracerpt EapHostPeer .etl** **– pdb** **&lt; &gt; pdbpath** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > 如果您沒有 tracerpt 工具的存取權，請避免最後一個步驟，並將 .etl 檔案傳送給 Microsoft 開發人員支援服務。

     

## <a name="tracing-on-the-authenticator"></a>Authenticator 上的追蹤

若要啟用驗證器端的追蹤：

1.  開啟提升權限的命令提示字元視窗。
2.  執行下列命令： **logman** **start trace** **EapHostAuthr** **-o** **。 \\EapHostAuthr .etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**
3.  重現您要追蹤的情節。
4.  執行下列命令： **logman** **stop** **EapHostAuthr** **-ets**
5.  使用下列命令將 etl 檔案轉換成文字： **tracerpt EapHostAuthr .etl** **– pdb** **&lt; &gt; pdbpath** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > 如果您沒有 tracerpt 工具的存取權，請避免最後一個步驟，改為將 .etl 檔案傳送給 Microsoft 開發人員支援人員。

     

## <a name="event-tracing"></a>事件追蹤

在 Windows 7 和更新版本的 Windows 中，EapHost 會在驗證器和對等上提供以事件為基礎的追蹤。 以事件為基礎的追蹤的優點是，不需要任何符號檔來查看追蹤訊息。 若要啟用事件追蹤：

1.  開啟 **EventViewer**。
2.  重要的 EapHost 訊息會記錄在以下：「自訂視圖 \\ 管理事件」
3.  非重大訊息會記錄在：「應用程式和服務 \\ Microsoft \\ Windows \\ EapHost
4.  從標題列的 [ **view** ] 功能表中選取 [**顯示分析和偵錯工具記錄** 檔]，即可在相同的路徑底下看到「分析」和「debug」類型事件訊息。

## <a name="tracing-on-the-routing-and-remote-access-service"></a>在路由及遠端存取服務上追蹤

若要啟用 RRAS 追蹤：

1.  開啟提升權限的命令提示字元視窗。
2.  執行下列命令： **netsh** **ras** **set** **tr** **\* *_ _* en**
3.  開啟 **% systemroot% \\ 追蹤** 以查看 RAS 追蹤

若要停用 RRAS 追蹤：

1.  開啟提升權限的命令提示字元視窗。
2.  執行下列命令： **netsh** **ras** **set** **tr** **\* *_ _***

如需詳細資訊，請參閱 [Netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> <dt>

[路由及遠端存取服務 (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 