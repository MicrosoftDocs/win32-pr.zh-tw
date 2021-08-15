---
description: 若要啟動服務或驅動程式服務，服務控制程式會使用 StartService 函數。
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: 服務啟動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17901987581b6a2680e0a70cfe2e0ed80472d293cbe32932f768e9133b6a058d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888697"
---
# <a name="service-startup"></a>服務啟動

若要啟動服務或驅動程式服務，服務控制程式會使用 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 函數。 如果資料庫已鎖定， **StartService** 函數就會失敗。 如果發生這種情況，服務控制程式應等候幾秒鐘，然後再次呼叫 **StartService** 。 它可以藉由呼叫 [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) 函數來檢查資料庫目前的鎖定狀態。

如果服務控制程式正在啟動服務，則可以使用 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 函式來指定要傳遞至服務之 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函數的引數陣列。 **StartService** 函式會在建立新執行緒之後傳回，以執行 **ServiceMain** 函數。 服務控制程式可以藉由呼叫 [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)函式，來取得 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)結構中新啟動服務的狀態。 在初始化期間， **dwCurrentState** 成員應為服務 \_ 開始 \_ 暫止。 **DwWaitHint** 成員是時間間隔（以毫秒為單位），表示服務控制程式在再次呼叫 **QueryServiceStatus** 之前應等待的時間長度。 初始化完成時，服務會將 **dwCurrentState** 變更為正在執行的服務 \_ 。

服務控制管理員不支援在啟動時將自訂環境變數傳遞給服務。 此外，服務控制管理員在服務執行時，不會偵測和傳遞環境變數的變更。 使用登錄值或 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 引數，而不是讓服務相依于環境變數。

以下是服務控制管理員啟動一般服務時會發生什麼情況的簡化總覽：

-   SCM 會從登錄讀取服務路徑，並準備啟動服務。 這包括取得服務鎖定。 保留服務鎖定時嘗試啟動另一項服務的任何嘗試都會封鎖，直到釋放服務鎖定為止。
-   SCM 會啟動進程，並等候子進程結束 (指出失敗) 或回報服務執行 \_ 狀態。
-   應用程式會執行其非常簡單的初始化，並呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 函數。
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 會連接到服務控制管理員，並啟動第二個執行緒來呼叫服務的 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函式。 **ServiceMain** 應該會儘快回報服務是否 \_ 正在執行。
-   當服務控制管理員收到服務正在執行的通知時，它會釋放服務鎖定。

如果服務未在80秒內更新其狀態，再加上最後一個等候提示，服務控制管理員就會判斷服務是否已停止回應。 服務控制管理員將會記錄事件並停止服務。

如果程式正在啟動驅動程式服務，則 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 會在設備磁碟機完成初始化後傳回。

如需詳細資訊，請參閱 [啟動服務](starting-a-service.md)。

 

 
