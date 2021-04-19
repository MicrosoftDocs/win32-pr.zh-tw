---
title: 標記用戶端
description: 「名字」用戶端必須透過取得名字標記來開始，而且有數種方式可讓「標記」用戶端取得標記。
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969835"
---
# <a name="moniker-clients"></a>標記用戶端

「名字」用戶端必須透過取得名字標記來開始，而且有數種方式可讓「標記」用戶端取得標記。 例如，在 OLE 複合檔案中，當使用者建立連結專案 (使用 [ **插入物件** ] 對話方塊、剪貼簿或拖放) 時，會將標記內嵌為連結專案的一部分。 在這種情況下，程式設計人員與名字的聯繫性最短。 以程式設計的方式，如果您有一個介面指標指向可執行 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的物件，您可以使用該介面指標來取得標記，並在定義的其他介面上提供方法來傳回名字標記。

有不同類型的標記，用來識別不同類型的物件，但對標記用戶端而言，所有的標記看起來都一樣。 標記用戶端只會在標記上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ，並取得標記所識別之物件的介面指標。 無論是否將物件識別為與整個試算表一樣大的物件，或以試算表內的單一資料格作為小者，呼叫 **BindToObject** 將會傳回該物件的指標。 如果物件已在執行中， **BindToObject** 會在記憶體中找到它。 如果物件是以被動的狀態儲存在磁片上， **BindToObject** 將會找出該物件的伺服器、執行伺服器，然後讓伺服器將物件帶到執行中狀態。 所有的系結程式詳細資料都不會從 [標記用戶端] 中隱藏。 因此，針對標記用戶端，使用標記非常簡單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[標記提供者](moniker-providers.md)
</dt> <dt>

[OLE 標記執行](ole-moniker-implementations.md)
</dt> </dl>

 

 




