---
title: 複合的名字
description: 其中一個最有用的名字，就是您可以同時串連或撰寫名字標記。
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad815cdb89dda7f58fe1507d43a07a14d24875309668297e20ec51114dd65d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737024"
---
# <a name="composite-monikers"></a>複合的名字

其中一個最有用的名字，就是您可以同時串連或撰寫名字標記。 *複合的標記* 是標記，是其他標記的組合，而且可以決定元件之間的關聯性。 這可讓您將具有相同部分路徑的兩個或多個名字標記之物件的完整路徑組合在一起。 您可以撰寫相同類別 (的名字，例如兩個檔案的標記) 或不同類別 (例如檔案的名字和專案的標記) 。 如果您要撰寫自己的「名字標記」類別，您也可以使用檔案或專案的名字寫來撰寫您的名字。 複合的基本優點是它會提供您一段程式碼，以實作為更簡單的名字組組合的每個可能的標記。 這可大幅減少特定自訂的「標記」類別的需求。

因為不同類別的名字可由另一個類別組成，所以名字可提供聯結多個命名空間的能力。 檔案系統會針對儲存為檔案的物件定義通用命名空間，因為所有應用程式都瞭解檔案系統路徑名稱。 同樣地，容器物件也會定義其所包含之物件的私用命名空間，因為沒有任何容器可理解另一個容器所產生的名稱。 因為可以組成檔案的標記和專案的名字標記，所以標記允許聯結這些命名空間。 標記用戶端可以使用單一機制來搜尋所有物件的命名空間。 用戶端只會在標記上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ，而此標記代碼會處理其餘部分。 在複合上呼叫 [**IMoniker：： GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) ，會使用所有個別的名字標記之顯示名稱的串連來建立名稱。

此外，由於您可以撰寫自己的「標記」類別，因此，「標記撰寫」可讓您將自訂延伸加入至物件的命名空間。

有時可以使用特殊方式結合特定類別的兩個名字標記。 例如，代表不完整路徑的檔案表示檔和另一個代表相對路徑的檔案表示檔，都可以合併成單一檔案的標記，代表完整的路徑。 例如，檔案的標記「c： \\ 工作 \\ 美工」可能由相對檔案的「名字標記」組成」。 \\備份 \\myfile.doc 「等於」 c： \\ work \\ 備份myfile.doc」 \\ 。 這是 *非泛型組合* 的範例。

另一方面，*泛型組合* 允許任何兩個標記的連接，無論其類別為何。 例如，您可以將專案的標記撰寫到檔案的名字標記上，不過當然不是如此。

因為非泛型組合取決於所涉及的名字標記類別，所以其詳細資料是由特定的標記類別的實作為定義。 如果您撰寫新的 [標記] 類別，則可以定義新的非泛型組合類型。 相反地，泛型組合是由 OLE 定義。 作為泛型撰寫結果而建立的標記稱為泛型複合標記。

這三個類別、檔案擁有者、專案的名字和泛型複合標記、全部一起運作，而且是最常用的標記類別。

標記用戶端應該呼叫 [**IMoniker：： ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) ，在具有另一個的標記上建立複合。 它在內部呼叫的標記會決定是否可以進行泛型或非泛型組合。 如果「標記實行」判斷出一般組合可供使用，OLE 會提供 [**CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) 函式來加速這項工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[反標記](anti-monikers.md)
</dt> <dt>

[類別名字標記](class-monikers.md)
</dt> <dt>

[檔案名字](file-monikers.md)
</dt> <dt>

[專案的名字](item-monikers.md)
</dt> <dt>

[指標標記](pointer-monikers.md)
</dt> </dl>

 

 




