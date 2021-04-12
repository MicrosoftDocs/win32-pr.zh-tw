---
title: URL 的名字
description: OLE 的「標記」架構提供一個方便的程式設計模型來處理 Url。
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104195643"
---
# <a name="url-monikers"></a>URL 的名字

OLE 的「標記」架構提供一個方便的程式設計模型來處理 Url。 此標記架構透過 [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) 函式和 [**IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) 和 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面，以及透過 [**IMoniker：： GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) 方法的可列印名稱，來支援可延伸且完整的名稱剖析。 **IMoniker** 介面是您實際使用所遇到之 url 的方式，而且建立符合標記架構的元件是實際延伸 URL 命名空間的方法。

系統提供的「標記」類別（URL 標記）提供建立和使用特定 Url 的架構。 因為 Url 經常會看到跨高延遲網路的資源，所以 URL 標記可支援非同步和同步系結。 URL 標記目前不支援 [非同步儲存體](/windows/desktop/Stg/asynchronous-storage)。

下圖顯示使用 URL 標記時所牽涉到的元件。 所有這些元件都應該很熟悉。  (查看 [非同步名字](asynchronous-monikers.md)。 ) 

![顯示有關使用 U R L 的標記之元件的圖表。](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

如同所有的「標記」用戶端，URL 標記的使用者通常會建立並保存對標記的參考，以及系結 ([**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)) 時所要使用的系結內容。 若要支援非同步系結，用戶端可以實作為系結狀態的回呼物件，此物件會實 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面，並使用 [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) 函式向系結內容註冊該物件。 這個物件會在呼叫 [**IBindStatusCallback：： OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85))期間接收傳輸的 [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85))介面。

URL 標記會識別剖析 URL 首碼所使用的通訊協定，然後從傳輸層抓取 [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) 介面。 用戶端會使用 **IBinding** 來支援系結作業的暫停、取消和優先順序。 回呼物件也會透過 [**IBindStatusCallback：： OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))、透過 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))的資料可用性通知，以及有關系結狀態的各種其他傳輸層通知，接收進度通知。 URL 的名字或特定傳輸層也可能會透過 **IBindStatusCallback：： QueryInterface** 要求用戶端提供的擴充資訊，讓用戶端能夠提供將影響系結作業的通訊協定特定資訊。

如需詳細資訊，請參閱下列主題：

-   [回呼同步處理](callback-synchronization.md)
-   [媒體類型的協商](media-type-negotiation.md)
-   [URL 標記函數](url-moniker-api-functions.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步名字](asynchronous-monikers.md)
</dt> <dt>

[關於 URL 的名字](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 