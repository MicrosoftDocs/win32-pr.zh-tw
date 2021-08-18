---
title: Top-Level 和內嵌指標
description: 若要瞭解如何在 Microsoft RPC 中配置指標和其相關聯的資料元素，您必須區分最上層指標和內嵌指標。
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fab18cfb345587f4c152f6890d94c5177e5bd9344e542592c33e462915beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011266"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level 和內嵌指標

若要瞭解如何在 Microsoft RPC 中配置指標和其相關聯的資料元素，您必須區分 *最上層指標* 和 *內嵌指標*。 參考非最上層指標的所有指標集合也很有用。

*最上層指標* 是在函式原型中指定為參數名稱的指標。 最上層指標及其對等一律會在伺服器上進行配置。

*內嵌指標* 是內嵌在資料結構中的指標，例如陣列、結構和等位。 當內嵌指標只會將輸出寫入緩衝區，而且在輸入上是 null 時，伺服器應用程式可以將其值變更為非 null。 在此情況下，用戶端 stub 會為此資料配置新的記憶體。

如果在呼叫之前，用戶端上的內嵌指標不是 null，則存根不會在傳回時配置用戶端上的記憶體。 取而代之的是，存根會嘗試將與內嵌指標相關聯的記憶體寫入與該指標相關聯之用戶端的現有記憶體中，以覆寫已存在的資料。

> [!Note]  
> 對於從緩衝區讀取或寫入的資料，以及未指定緩衝區大小的資料，輸出長度必須小於或等於輸入長度。 偵測到溢位時，就會引發 RPC 例外狀況。 針對字串資料，輸出長度是藉由檢查輸入字串的長度來決定。 因此，輸出字串的長度不能超過輸入字串的長度。 最佳做法指引是藉由一律包含大小指定的參數來表示緩衝區大小，以避免此情況。

 

內嵌的僅限寫入指標會在 [結合指標和方向屬性](combining-pointer-and-directional-attributes.md)中討論。

詞彙 *nontop 層級指標* 會參考未在函式原型中指定為參數名稱的所有指標，包括內嵌指標和多層級的嵌套指標。

 

 




