---
title: 指標和 RPC
description: 使用指標做為 C 函數參數非常有效率。
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840520"
---
# <a name="pointers-and-rpc"></a>指標和 RPC

使用指標做為 C 函數參數非常有效率。 指標只會有幾個位元組，可用來存取大量的記憶體。 不過，在分散式應用程式中，用戶端和伺服器程式位於不同的位址空間中，它們可以在不同的電腦上。 因此，用戶端和伺服器通常無法存取相同的記憶體空間。

當其中一個遠端程式的參數是物件的指標時，用戶端必須將該物件的複本及其指標傳送至伺服器。 如果遠端程式透過其指標修改物件，伺服器會傳回指標及其修改過的複本。

MIDL 提供指標屬性，將所需的額外負荷和應用程式大小降到最低。 本節討論 MIDL 指標屬性的用途和用法。 它也會提供 RPC 應用程式中指標處理的資訊。 它分成下列主題：

-   [指標種類](kinds-of-pointers.md)
-   [指標和記憶體配置](pointers-and-memory-allocation.md)
-   [預設指標類型](default-pointer-types.md)
-   [指標屬性類型繼承](pointer-attribute-type-inheritance.md)

 

 




