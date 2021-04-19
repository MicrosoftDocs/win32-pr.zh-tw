---
title: 取消方法呼叫
description: 隨著分散式和 Web 應用程式的推出，某些方法呼叫可能會花費很長的時間才能傳回。
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966891"
---
# <a name="canceling-method-calls"></a>取消方法呼叫

隨著分散式和 Web 應用程式的推出，某些方法呼叫可能會花費很長的時間才能傳回。 網路連線的延遲可能很高，伺服器電腦可能會服務許多用戶端，或者伺服器元件可能傳遞大量資料，例如多媒體檔案。 使用者應該能夠取消花費太長時間的要求，而且應用程式應該能夠處理取消要求，並繼續執行其他工作。 在 COM 中，您可以使用 [**imessagefilter.prefiltermessage**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) 介面來取消源自單一執行緒單元的暫止呼叫。

當呼叫被封送處理時，proxy 會建立一個可實 [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) 介面的 cancel 物件。 Cancel 物件與呼叫暫止的呼叫和執行緒相關聯。

若要解除擱置中的呼叫，用戶端會透過 cancel 物件傳遞取消要求，此物件會處理通知伺服器物件已取消呼叫的詳細資料。 如果所呼叫的方法尚未傳回，伺服器物件在偵測取消要求時，會清除它已配置的任何程式資源，並藉由傳回適當的 **HRESULT** 值來通知其用戶端，以取消執行呼叫。 如果已傳回呼叫的方法，cancel 物件會通知用戶端。 無論是哪一種情況，用戶端執行緒都會解除封鎖，並可繼續處理。

伺服器物件對取消要求的回應是由伺服器實施者自行決定，但是用戶端上的呼叫執行緒一律會解除封鎖，並忽略伺服器嘗試傳遞給它的任何結果。 Cancel 物件提供一種方法來要求取消目前正在執行的方法，但是無法保證伺服器物件將停止處理呼叫。 例如，呼叫可能已經傳回，或伺服器物件可能不支援取消物件。

COM 會針對使用標準封送處理的用戶端物件和介面，自動提供取消物件的標準執行。 若為使用自訂封送處理的物件和介面，您將必須執行您自己的 cancel 物件。

現在，cancel 物件只會處理同步呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[取消非同步呼叫](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 