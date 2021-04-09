---
title: 從現有資料建立連結和內嵌物件
description: 從現有資料建立連結和內嵌物件
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675711"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a>從現有資料建立連結和內嵌物件

使用者通常會使用剪貼簿或拖放將資料物件從其伺服器應用程式複製到使用者的容器應用程式，以組合複合檔案。 使用支援 OLE 的應用程式，使用者可以從伺服器或容器起始傳送。 例如，伺服器可以將資料複製到伺服器應用程式中的剪貼簿，然後切換至容器應用程式，並選擇 [貼上特殊/内嵌物件] 或 [對應的功能表] 命令，從選取的資料建立新的内嵌物件。 或者，使用者可以將資料從一個應用程式拖曳到另一個應用程式。 此程式類似于建立連結化物件。

> [!Note]  
> 同時做為 OLE 伺服器和容器使用的應用程式可以使用自己的資料選取範圍，在相同檔中的新位置建立內嵌或連結的物件。

 

OLE 伺服器和容器應用程式之間的資料傳輸是以統一的資料傳輸為基礎，如 [資料傳輸](data-transfer.md)中所述。 OLE 伺服器和物件處理常式會執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ，以便使用剪貼簿或拖放功能，將其資料提供給傳輸。 OLE 物件支援所有常用的剪貼簿格式。 此外，它們支援六種剪貼簿格式，可支援從選取的資料物件建立連結和內嵌的物件。

OLE 剪貼簿格式描述在 OLE 容器中卸載或貼上的資料物件，會成為內嵌或連結的複合檔案物件。 資料物件會將這些格式呈現給容器應用程式，以將其精確度視為資料的描述。 換句話說，物件會先顯示最能代表它的格式，然後是下一個最佳格式，依此類推。 這種刻意的順序鼓勵容器應用程式使用最可能的格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案](compound-documents.md)
</dt> <dt>

[資料轉送](data-transfer.md)
</dt> </dl>

 

 




