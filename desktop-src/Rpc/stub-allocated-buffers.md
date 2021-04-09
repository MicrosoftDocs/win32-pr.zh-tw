---
title: Stub-Allocated 緩衝區
description: 您可以藉由對 midl \_ 使用者 \_ 配置或 midl \_ 使用者免費進行單一呼叫，而不是針對樹狀結構或圖形的每個節點強制進行不同的呼叫 \_ 。
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023820"
---
# <a name="stub-allocated-buffers"></a>Stub-Allocated 緩衝區

您可以藉由對 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1) 或 [midl \_ 使用者 \_ 免費](/windows/desktop/Midl/midl-user-free-1)進行單一呼叫，而不是針對樹狀結構或圖形的每個節點強制進行不同的呼叫。 ACF 屬性 **\[ (所有節點配置， \_) \]** 引導存根在使用者所提供的單一呼叫中配置或釋放所有節點–記憶體管理函數。

例如，RPC 應用程式可能會使用下列二進位樹狀結構資料結構：

``` syntax
/* IDL file fragment */
typedef struct _TREE_TYPE 
{
    short sNumber;
    struct _TREE_TYPE * pLeft;
    struct _TREE_TYPE * pRight;
} TREE_TYPE;

typedef TREE_TYPE * P_TREE_TYPE;
```

ACF 屬性會 **\[ 配置 (\_) \]** 套用至此資料類型的所有節點都會出現在 ACF 的 **typedef** 宣告中，如下所示：

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

**\[ 配置 \]** 屬性只能套用至指標類型。 **\[ 配置 \]** ACF 屬性是 DCE IDL 的 Microsoft 擴充功能，因此，如果您使用 MIDL **/osf** 參數進行編譯，就無法使用此屬性。 當 **\[ 配置 (所有 \_ 節點) \]** 套用至指標類型時，MIDL 編譯器所產生的存根會遍歷指定的資料結構，以判斷配置大小。 然後，存根會進行單一呼叫，以配置圖形或樹狀結構所需的整個記憶體量。 用戶端應用程式可以對 **midl \_ 使用者 \_ 免費** 進行單一呼叫，以更有效率的方式釋放記憶體。 不過，使用節點節點記憶體配置時，伺服器存根的效能通常會增加，因為伺服器 stub 通常會使用不需要配置的私用記憶體。

如需詳細資訊，請參閱 [節點節點配置和解除配置](node-by-node-allocation-and-deallocation.md)。

 

 