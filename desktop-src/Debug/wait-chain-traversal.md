---
description: Wait Chain (WCT) 可讓偵錯工具診斷應用程式停止回應和鎖死。
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: 等候鏈遍歷
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/04/2021
ms.locfileid: "103845663"
---
# <a name="wait-chain-traversal"></a>等候鏈遍歷

Wait Chain (WCT) 可讓偵錯工具診斷應用程式停止回應和鎖死。

*等候鏈* 是執行緒和同步處理物件的交替順序，其中每個執行緒都會等候後面的物件。 接下來的每個物件都是由鏈中的後續執行緒所擁有。

執行緒等候同步處理物件的時間來自執行緒要求物件的時間，直到執行緒取得該物件為止。 此「鎖定」是由執行緒取得執行緒時所擁有，直到執行緒釋放它為止。 換句話說，當執行緒1正在等候執行緒2所擁有的鎖定時，執行緒1的執行緒2就會「等待」。

WCT 支援下列同步處理原始物件：

- [ (ALPC) 的 Advanced Local Procedure 呼叫 ](../etw/alpc.md)
- [元件物件模型 (COM)](../com/the-component-object-model.md)
- [重要區段](../sync/critical-section-objects.md)
- [Mutex](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- [進程和執行緒](../procthread/processes-and-threads.md)的[等候](../sync/wait-functions.md)作業

若要取得一或多個執行緒的等候鏈，請使用 [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) 和 [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) 函式來建立 WCT 會話。 WCT 會話會以 **HWCT** 類型的控制碼表示。

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>會話可以是同步或非同步

除非已抓取等候鏈，否則無法取消同步會話，並封鎖呼叫執行緒。

非同步會話不會封鎖呼叫的執行緒，而且可以使用 [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) 函式來取消應用程式。 非同步作業的結果是透過應用程式所提供的 [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) 回呼函式提供。

針對非同步會話，呼叫端可以透過 [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) 指定內容資料結構的指標 (這個相同的指標會傳遞至 [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) 回呼函數) 。

內容資料結構是使用者定義的，而不是 WCT 的不透明。 應用程式可以使用它來在 WCT 查詢和回呼函數之間通訊內容。 一般來說，您會透過此結構傳遞事件控制碼，並在執行回呼時，發出此事件的信號，並通知監視執行緒已完成查詢。

請參閱 [使用 WCT](using-wct.md) 以取得等候鏈進行的範例。

## <a name="related-topics"></a>相關主題

[使用 WCT](using-wct.md)、 [WCT 參考](wct-reference.md)、 [MSDN 雜誌 2007 7 月-Bugslayer.web：等候鏈的遍歷](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)