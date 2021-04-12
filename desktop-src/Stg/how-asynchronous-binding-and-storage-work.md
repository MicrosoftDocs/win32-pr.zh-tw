---
title: 非同步綁定和儲存的運作方式
description: 非同步存放裝置可增強 COM 結構化儲存規格，以支援在高延遲的低速連結網路（例如網際網路）上下載儲存體物件。
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- 非同步綁定和儲存的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626e8c7a55b667e158de42b3c88a17315b5e41ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375656"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>非同步綁定和儲存的運作方式

非同步存放裝置可增強 COM 結構化儲存規格，以支援在高延遲的低速連結網路（例如網際網路）上下載儲存體物件。 非同步存放裝置可與非同步名字區一起運作，以提供完整的非同步系結行為。

## <a name="document-object-embedded-in-a-web-page"></a>內嵌在網頁中的檔物件

當使用者按一下代表內嵌于網頁之檔的連結時，就會發生下列事件：

1.  瀏覽器會呼叫 [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) 函式，並傳遞連結 URL。
2.  [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) 會剖析 URL、建立對應的非同步標記，並將指標傳回至標記的 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) 介面。
3.  瀏覽器會呼叫 [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) 來判斷標記是否為非同步、建立系結內容、向系結內容註冊 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面（僅限於當標記為非同步時），以及呼叫 [**IMoniker：： BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)，並傳遞系結內容。
4.  標記會系結至物件，並針對 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) 介面進行查詢，這會指出物件是否支援非同步綁定和儲存。 如果物件傳回 **IPersistMoniker** 的指標：

    1.  URL 標記會呼叫 [**IPersistMoniker：： Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))，並將自己的 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) 指標傳遞給物件。
    2.  物件會修改系結內容、選擇它是否想要封鎖或非封鎖的儲存體、註冊它自己的 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) ，以及在透過 [**IPersistMoniker：： Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))所收到的指標上呼叫 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) 。
    3.  此標記會建立異步儲存、保留包裝函式物件之 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 介面的參考、在根儲存體上註冊 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) 介面，以及呼叫 [**IPersistStorage：： Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load)，傳遞非同步儲存的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 指標。 當資料抵達背景執行緒上的 (時) 會呼叫 **IFillLockBytes** ，以填滿暫存檔案上的 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) 。
    4.  物件會從儲存體讀取資料，並在收到足夠的資料可視為已初始化時，從 [**IPersistMoniker：： Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) 傳回資料。 如果物件嘗試讀取尚未下載的資料，下載程式會收到 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify)的通知。 在 [**IProgressNotify：： OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) 方法內，下載的執行緒會在強制回應訊息迴圈中封鎖，或導致非同步存放裝置傳回 E \_ 暫止，取決於物件是否已要求封鎖或非封鎖的儲存區。

5.  如果物件不會執行 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))，則為 [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage)的標記查詢，這表示物件的持續性狀態會儲存在儲存物件中。 如果物件傳回 **IPersistStorage** 的指標：

    1.  此標記本身會呼叫 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) ，要求封鎖 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (因為物件不是非同步感知) 、會建立異步儲存、保留包裝函式物件 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 介面的參考、在根儲存體上註冊 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) 介面，以及呼叫 [**IPersistStorage：： Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load)，傳遞非同步儲存的 **IStorage** 指標。 當資料抵達背景執行緒上的 (時) 標記會呼叫 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 以填滿暫存檔案上的 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) 。
    2.  物件會從儲存體讀取資料，並在收到足夠的資料可視為已初始化時，從 [**IPersistStorage：： Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) 傳回資料。 如果物件嘗試讀取尚未下載的資料，它會收到 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify)的通知。 在 [**IProgressNotify：： OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) 方法內，下載執行緒一律會在強制回應訊息迴圈中封鎖。

6.  無論下載是同步或非同步，此標記都會從 [**IMoniker：： BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)傳回，而瀏覽器會接收其所要求的已初始化物件。
7.  瀏覽器會查詢 [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) ，並將物件裝載為檔物件。  (此時物件可能未完全初始化，但足以顯示有用的部分，在這種情況下，下載會在背景繼續進行。 ) 

 

 