---
title: 執行 IClassFactory
description: 執行 IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382918"
---
# <a name="implementing-iclassfactory"></a>執行 IClassFactory

當用戶端使用 CLSID 要求物件實例的建立時，第一個步驟是建立類別物件，這個中繼物件包含 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面的方法的執行。 雖然 COM 提供數個實例建立函式，但這些函式的執行中的第一個步驟是建立類別物件。

因此，所有伺服器都必須執行 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面的方法，其中包含兩種方法：

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)。 這個方法必須建立物件的未初始化實例，並將指標傳回物件上要求的介面。
-   [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver)。 這個方法只會遞增類別物件上的參考計數，以確保伺服器留在記憶體中，而且在用戶端準備好執行這項作業之前，不會關閉它。

為了讓伺服器負責自己的授權，COM 會定義 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)，以從 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)繼承其定義。 因此，執行 **IClassFactory2** 的伺服器必須依照定義執行 **IClassFactory** 的方法。

COM 也提供 helper 函式來執行跨進程伺服器。 如需詳細資訊，請參閱 [跨進程伺服器執行](out-of-process-server-implementation-helpers.md)協助程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 伺服器責任](com-server-responsibilities.md)
</dt> <dt>

[授權和 IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 