---
title: 檔案名字
description: 檔案名字
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51d000964bcfe7cad29db333bbbbc68b3a94d0f977c47b29affab4eed0b139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048286"
---
# <a name="file-monikers"></a>檔案名字

檔案 *名字* 標記是最簡單的標記類別。 檔案標記可以用來識別儲存在它自己的檔案中的任何物件。 檔案的標記可做為原生檔案系統指派給檔案之路徑名稱的包裝函式。 針對這個標記呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 會導致這個物件啟動，然後傳回物件的介面指標。 以標記命名的物件來源必須提供 [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) 介面的實作為支援系結檔案的標記。 檔案副檔名可以是完整或相對路徑。

例如，儲存為 file C： WorkMySheet.xls 之試算表物件的檔案標記 \\ \\ 會包含與該路徑名稱相等的資訊。 但是，此標記不一定是由相同的字串所組成。 字串只是其 *displayÂ名稱*，表示對使用者有意義的名字標記內容。 顯示名稱（可透過 [**IMoniker：： GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) 方法取得）只會在向使用者顯示標記時使用。 這個方法會取得任何標記類別的顯示名稱。 就內部而言，此標記可能會以較有效率的格式來儲存相同的資訊，以執行「名字」作業，但對使用者來說不具意義。 然後，當這個相同的物件透過呼叫 [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 方法系結時，就可能會將該檔案載入試算表中，以啟用該物件。

OLE 提供 helper 函式 [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) 的 helper 函式，它會建立檔案的標記物件，並將其指標傳回給提供者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[反標記](anti-monikers.md)
</dt> <dt>

[類別名字標記](class-monikers.md)
</dt> <dt>

[複合的名字](composite-monikers.md)
</dt> <dt>

[專案的名字](item-monikers.md)
</dt> <dt>

[指標標記](pointer-monikers.md)
</dt> </dl>

 

 




