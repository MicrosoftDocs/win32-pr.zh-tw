---
title: 提供類別資訊
description: 提供類別資訊
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092262"
---
# <a name="providing-class-information"></a>提供類別資訊

這通常適用于物件的用戶端檢查物件的型別資訊。 根據物件的 CLSID，用戶端可以使用登錄專案找出物件的類型程式庫，然後在符合 CLSID 的程式庫中掃描 coclass 專案的類型程式庫。

不過，並非所有物件都有 CLSID，不過它們仍然需要提供類型資訊。 此外，用戶端可以輕鬆地要求物件提供其類型資訊，而不是透過所有冗長工作從登錄專案中解壓縮相同的資訊。 這項功能在處理可連線物件上的連出介面時相當重要。  (如需可連線物件如何提供這項功能的詳細資訊，請參閱 [使用 IProvideClassInfo](using-iprovideclassinfo.md) 。 ) 

在這些情況下，用戶端可以查詢 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 或 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)的物件。 如果這些介面存在，用戶端會呼叫 [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) 方法來取得介面的類型資訊。

藉由執行 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 或 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)，物件指定它可以提供整個類別的型別資訊。也就是說，它在其類型程式庫的 coclass 區段中所描述的內容（如果有的話）。 [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) 會傳回對應至物件之 coclass 資訊的 **ITypeInfo** 指標。 透過這個 **ITypeInfo** 指標，用戶端可以檢查所有物件的傳入和傳出介面定義。

物件也可以提供 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)。 **Iprovideclassinfo2.getguid** 介面是 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)的簡單延伸，可讓您快速且輕鬆地針對其預設事件集取得物件的輸出介面識別碼。 **Iprovideclassinfo2.getguid** 衍生自 **IProvideClassInfo**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 用戶端和伺服器](com-clients-and-servers.md)
</dt> </dl>

 

 




