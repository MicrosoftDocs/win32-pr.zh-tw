---
title: 伺服器上的持續性儲存體
description: 您可以將應用程式優化，讓伺服器 stub 在遠端程序呼叫結束時，不會釋放伺服器上的記憶體。
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932395"
---
# <a name="persistent-storage-on-the-server"></a>伺服器上的持續性儲存體

您可以將應用程式優化，讓伺服器 stub 在遠端程序呼叫結束時，不會釋放伺服器上的記憶體。 例如，當多個遠端程式將操作內容控制碼時，您可以使用 ACF 屬性 **\[ 配置 (不要 \_ 釋放) \]** 來保留伺服器上配置的記憶體。

**\[ 配置 (不會 \_ 釋放) \]** 屬性會新增至 ACF 中的 ACF **typedef** 宣告。 例如：

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

當 **\[ 配置 (未 \_ 釋放) \]** 屬性時，會由伺服器 stub 配置樹狀結構資料結構，但不會加以釋放。 當您將指標變成可供其他常式使用的持續性資料區域時（例如，藉由將指標複製到全域變數），保留的資料可供其他伺服器函數存取。 **\[ 配置 (不會 \_ 釋放) \]** 屬性特別適合用來將持續性指標結構維護為與內容控制碼類型相關聯的伺服器狀態資訊的一部分。

 

 




