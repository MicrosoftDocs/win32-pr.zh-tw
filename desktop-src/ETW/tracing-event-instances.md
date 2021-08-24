---
description: 傳統提供者會使用 TraceEventInstance 函數來追蹤屬於單一交易一部分的事件。 您也可以使用此函數來追蹤父/子事件。
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: 在傳統提供者中撰寫相關的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41443c0a05bd94e25ae4ca6a4549671c6aa0682b848660ca31683bb4bf8b75b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813810"
---
# <a name="writing-related-events-in-a-classic-provider"></a>在傳統提供者中撰寫相關的事件

[傳統](about-event-tracing.md) 提供者會使用 [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) 函數來追蹤屬於單一交易一部分的事件。 您也可以使用此函數來追蹤父/子事件。

在呼叫 [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) 函數之前，您必須先呼叫 [**CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) 函數來取得交易識別碼。 此函式會產生唯一的交易識別碼，並將其對應至已註冊的類別 GUID 控制碼。 在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)函數之後，已註冊之類別 guid 的控制碼可在 [**追蹤 \_ GUID \_ 註冊**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration)結構的 **RegHandle** 成員中使用。 交易識別碼會放置在您傳遞給 **CreateTraceInstanceId** 函數的 [**事件 \_ 實例 \_ 資訊**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info)結構的 **InstanceId** 成員中。

傳遞至 [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)函式的 [**事件 \_ 實例 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header)結構類似于 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構 (查看) 的 [追蹤事件](tracing-events.md)，但它包含與實例相關的其他資訊，而且不包含 **Guid** 成員。

事件實例可以用來建立事件之間的階層式關聯性。 [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)函式會接受來自兩個事件實例的實例特定資訊。 *PInstInfo* 參數指向事件實例的 [**事件 \_ 實例 \_ 資訊**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info)結構，而 *PParentInstInfo* 參數指向父事件實例的 **事件 \_ 實例 \_ 資訊** 結構。 "Parent" 事件實例的定義為應用程式定義;父系可以是已經產生的任何實例。

 

 
