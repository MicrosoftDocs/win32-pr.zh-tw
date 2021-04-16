---
description: 服務會負責將其狀態的變更報告至服務控制管理員 (SCM) 。
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: 服務狀態轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df7684b1ebc04aa1116b09a3ae4321f2552d7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556550"
---
# <a name="service-state-transitions"></a>服務狀態轉換

服務會負責將其狀態的變更報告至服務控制管理員 (SCM) 。 服務控制程式和系統只能從 SCM 找出服務的狀態，因此服務必須正確地報告其狀態。 服務會藉由呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 函式，並將指標指向完整初始化的 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) 結構，以報告其狀態。 結構的 **dwCurrentState** 成員包含要報告的服務狀態。

服務的初始狀態為已停止服務 \_ 。 當 SCM 啟動服務時，會將服務狀態設定為服務 \_ 開始 \_ 擱置，並呼叫服務的 [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函式。 服務接著會使用 [服務 ServiceMain](service-servicemain-function.md)函式中所述的其中一種技術來完成初始化。 服務完成初始化並準備開始接收控制項要求之後，服務會呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 來執行報表服務， \_ 並指定服務已準備好接受的控制項要求。 從服務啟動到服務執行的轉換， \_ \_ \_ 表示服務已順利啟動的 SCM 和服務監視工具。 如果服務報告的狀態不是執行中的服務 \_ ，則 SCM 或服務監視工具可能會將服務標示為無法啟動。

SCM 只會將指定的控制項要求傳送到服務 (但服務 \_ 控制 \_ 詢問要求（一律會) 傳送）除外。 如需服務可以接受的控制項要求清單，請參閱 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)結構的 **dwControlsAccepted** 成員。 如需註冊接收裝置事件的詳細資訊，請參閱 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 函式。

服務狀態通常會因處理控制項要求而變更。 控制導致服務狀態變更的要求包括服務 \_ 控制 \_ 停止、服務 \_ 控制 \_ 暫停和服務 \_ 控制 \_ 繼續。 如果服務必須花很長的處理方式來處理這些要求中的任何一項，則應該建立次要執行緒來執行冗長的處理，並將對應的擱置狀態回報給 SCM。  (若要在 Windows Vista 和更新版本的 Windows 上獲得最佳效能，此服務應該使用 [執行緒集](/windows/desktop/ProcThread/thread-pools) 區中的背景工作執行緒來達到此目的。 ) 此服務應該會在長時間處理完成時回報已完成的狀態轉換。 如需處理控制項要求的詳細資訊，請參閱 [服務控制處理常式函數](service-control-handler-function.md)。

只有特定的服務狀態轉換是有效的。 下圖顯示有效的轉換。

![有效的服務狀態轉換](images/service-status-transitions.png)

回報給 SCM 的服務狀態會決定 SCM 與服務的互動方式。 例如，如果服務將服務 \_ 停止 \_ 擱置，則 SCM 不會將進一步的控制權要求傳輸至服務，因為此狀態表示服務正在關閉。 服務所報告的下一個狀態應該是服務 \_ 停止，因為這是服務停止暫止之後唯一的有效狀態 \_ \_ 。 但是，如果服務報告不正確轉換，則 SCM 不會讓呼叫失敗。

下圖更詳細地說明服務狀態轉換，包括服務控制程式所起始的控制項要求 (服務用戶端) ，以及服務對 SCM 報告狀態變更的 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 呼叫。 如先前所述，SCM 只會傳送服務已指定要接受的控制項要求，因此服務可能不會收到圖表中顯示的所有要求。

![服務狀態轉換詳細資料 ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
