---
description: 應用程式可以在轉譯為螢幕時，等候事件不必要 (也就是 pixels occluded) 。
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: 不需要轉譯時等候事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972293"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>不需要轉譯時等候事件

應用程式可以在轉譯為螢幕時，等候事件不必要 (也就是 pixels occluded) 。 當桌面視窗管理員 (DWM) 或應用程式 pixels occluded 時，不需要轉譯，而且作業系統可長期保持較低的電源狀態。 這可節省電力並延長電池壽命。

應用程式可以在下列情況等候事件：

-   所有監視都已關閉。
-   應用程式執行所在的會話已中斷連線。
-   應用程式會在單一監視設定上，以全螢幕的形式執行。
-   應用程式會在與作用中桌面不同的桌上型電腦上執行，而且沒有在使用中桌面上呈現的許可權。

當應用程式可以再次轉譯時，作業系統會觸發事件。 在驅動程式升級期間，或 timeout 偵測和復原 (TDR) procession 時，不會清除此事件，不過當新的介面卡和監視變成作用中時，就會將其清除。

如果您想要讓應用程式收到有關遮蔽狀態變更的通知，應用程式必須註冊這些變更。 應用程式可以註冊，以透過訊息至視窗或透過事件信號來通知遮蔽狀態變更。 若要註冊以接收有關遮蔽狀態變更之視窗的通知訊息，應用程式會呼叫 [**IDXGIFactory2：： RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) 方法。 若要註冊以透過事件信號接收遮蔽狀態變更的通知，應用程式會呼叫 [**IDXGIFactory2：： RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) 方法。 這兩種方法都會將指標傳回給應用程式用來取消註冊通知的索引鍵值。 若要取消註冊通知，應用程式會將此索引鍵值傳遞給 [**IDXGIFactory2：： UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 1.2 改進](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



