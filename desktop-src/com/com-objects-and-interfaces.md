---
title: COM 物件和介面
description: COM 物件和介面
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a663b5d6e5966422927e37f1501924bf8ec8921210c9d38765153dc0d80fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501548"
---
# <a name="com-objects-and-interfaces"></a>COM 物件和介面

COM 是一種技術，可讓物件在進程和電腦界限之間進行互動，就像在單一進程內一樣簡單。 COM 可透過指定操作與物件相關聯之資料的唯一方法，來達成此目的。  本檔中使用此詞彙時，是指與物件相關聯之 COM 二進位相容介面的程式碼中的實作為。

COM 使用 word *介面* ，與通常用於 Visual C++ 程式設計的意義不同。 C + + 介面指的是類別支援的所有函式，而物件的用戶端可以呼叫來與其互動。 COM 介面指的是 COM 類別所執行的一組預先定義的相關函式，但特定介面不一定代表該類別支援的所有函式。

參考執行介面的物件表示物件使用的程式碼會 *執行* 介面的每個方法，並將這些函式的 com 二進位相容指標提供給 com 程式庫。 然後，COM 會將這些函式提供給要求介面指標的任何用戶端使用，不論用戶端是在執行這些函式的進程內部或外部。

如需詳細資訊，請參閱下列主題：

-   [介面和介面的實現](interfaces-and-interface-implementations.md)
-   [介面指標和介面](interface-pointers-and-interfaces.md)
-   [IUnknown 和介面繼承](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[介面](interfaces.md)
</dt> </dl>

 

 




