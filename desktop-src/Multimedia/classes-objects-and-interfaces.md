---
title: 類別、物件和介面
description: 類別、物件和介面
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54008f316103a8a113e6702e4a4b1192bc0576f5a61fb28b38dbe2502bae881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786178"
---
# <a name="classes-objects-and-interfaces"></a>類別、物件和介面

在 c + + 程式設計語言中， *類別* 是由 *屬性* (或成員資料) 和 *方法*)  (或成員函式所組成。 這些屬性是資料元素，例如結構中所包含的專案。 這些方法會用於各種用途，例如初始化、指派、作業和資料存取。 使用類別宣告的方式，與使用結構宣告的方式相同。 當您定義類別 *物件* 時，會為類別配置記憶體。 每個類別物件都有其屬性的資料區域，以及它所支援之方法的指標資料表。

在 OLE 中，物件是由資料和方法所組成，就像在 c + + 中一樣。 不過，OLE 物件會遵守更嚴格的規則。 資料完全是內部的。 物件只會公開介面。 *介面* 是一組物件的相關方法。 每個物件都可以支援多個介面。 所有 OLE 介面都支援 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。

 

 




