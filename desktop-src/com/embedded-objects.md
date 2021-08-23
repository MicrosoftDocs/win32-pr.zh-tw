---
title: COM)  (的内嵌物件
description: 内嵌物件
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df671850dc167a0751f69cbc57f8c19698db06a0454dd6283553c4d8ffa1609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048356"
---
# <a name="embedded-objects-com"></a>COM)  (的内嵌物件

内嵌物件實際上會儲存在複合檔案中，以及管理物件所需的所有資訊。 換句話說，嵌入的物件實際上是它所在的複合檔案的一部分。 這種安排有幾個缺點。 首先，包含内嵌物件的複合檔案將會大於一個，其中包含與連結相同的物件。 其次，對内嵌物件來源所做的變更將不會自動複寫到內嵌的複本中，而且內嵌複本中的變更不會反映在來源中，因為它們是使用連結。

但基於特定目的，內嵌提供數個優於連結的優點。 首先，使用者可以將包含内嵌物件的複合檔案傳輸到其他電腦，或同一部電腦上的其他位置，而不會中斷連結。 其次，使用者可以編輯内嵌物件，而不需要變更原始內容。 有時候，這項分隔正是必要的。 第三，内嵌物件可以就地啟用，這表示使用者可以編輯或操作物件，而不需要在與物件容器不同的視窗中工作。 相反地，當物件啟用時，容器應用程式的使用者介面會變更，以公開管理或修改物件時所需的工具。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從現有資料建立連結和內嵌物件](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




