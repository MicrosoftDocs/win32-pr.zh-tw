---
title: 非同步和同步系結
description: 非同步和同步系結
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb498d083260db087e9f32cd3f24b67f03f9a788c0add2592dde36fe7a7905e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048856"
---
# <a name="asynchronous-and-synchronous-binding"></a>非同步和同步系結

用戶端可以藉由呼叫 [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) 函式來查看是否為非同步標記。 如果用戶端傳回 BINDF \_ 非同步旗標，而不是從後續呼叫 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)傳回物件指標或儲存體指標，則該標記會傳回 MK \_ 的 \_ 非同步來取代物件指標，而 **Null** 則取代儲存體指標。 為了回應，用戶端應該在 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) 和 [**IBindStatusCallback：： OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85))的執行期間，等候接收要求的物件或儲存體。

回呼物件也會透過 [**IBindStatusCallback：： OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))、透過 [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))的資料可用性通知，以及有關系結作業狀態之標記的各種其他通知，來接收進度通知。

如果用戶端不會 \_ 從 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))的標記呼叫傳回 BINDF 非同步旗標，系結作業將會同步執行，而所需的物件或儲存體將會從後續呼叫 [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 或 [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage)傳回。 同樣地，如果用戶端需要同步作業，而且不想要接收任何進度通知或回呼，則可以要求非同步標記，而不是藉由執行 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85))來同步處理。 在這種情況下，非同步標記行為會像標準同步的標記一樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步名字](asynchronous-monikers.md)
</dt> </dl>

 

 