---
description: 呼叫佇列或路由點是參數內的特殊位址，其中呼叫會暫時保留暫止的動作。
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: 呼叫佇列和路由點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66895101b72ca8e16810d3766edf897efcfedddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192616"
---
# <a name="call-queues-and-route-points"></a>呼叫佇列和路由點

呼叫佇列或路由點是參數內的特殊位址，其中呼叫會暫時保留暫止的動作。 這個特性是以 LINEADDRESSCAPS 中 DwAddrCapFlags 成員的 bits LINEADDRCAPFLAGS \_ QUEUE 和 LINEADDRCAPFLAGS ROUTEPOINT 來表示 \_ 。  [](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) 出現在這類位址上的所有呼叫都是由應用程式等候動作，而且可能會有執行的預設動作 (例如，如果應用程式在定義的期間內不採取任何動作，請傳送至代理程式或主幹) 。 應用程式必須由系統管理員設定，如此一來，它就能知道應該對每個佇列或路由點位址上出現的呼叫採取哪些動作，以及可用來決定要採取之動作的時間量。

應用程式可以使用 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)來判斷佇列或路由點中暫止的呼叫數目。 [**LineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)函式可用來取得資訊，例如呼叫識別碼、傳入或傳出來源等，以及應用程式用來進行呼叫處理的決策;您可以重新導向、轉型、捨棄等呼叫，或只允許自動將佇列傳遞至目的地。 若已放棄，則呼叫 LINECALLSTATE \_ 中斷連線。 離開佇列時，呼叫進入 *閒置狀態* ; **lineGetCallInfo** 可以用來讀取重新導向識別碼，以判斷它們的傳送位置。

某些參數允許在佇列中進行呼叫，或在保存時接收特定的處理，例如無聲、回電、忙碌信號、音樂或接聽錄製的公告。 [**LineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)函式可讓應用程式控制處理。 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)中的 **dwCallTreatmentListSize** 和 **dwCallTreatmentListOffset** 成員所分隔的結構，可讓應用程式判斷支援的治療。 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **dwCallTreatment** 成員表示目前的處理，而具有 LINECALLINFOSTATE 處理的 [**行 \_ CALLINFO**](line-callinfo.md)訊息會 \_ 指出此變更的時間。 LINECALLSTATUS 中 \_ **dwCallFeatures** 成員的 LINECALLFEATURE SETTREATMENT 位表示 [](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)允許應用程式變更處理的時間。 LINECALLTREATMENT \_ 常數集定義一組有限的預先定義呼叫處理; 服務提供者可以定義更多。

 

 



