---
title: 移動物件
description: 移動物件
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，移動物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1158bfc3fb85712b2ab52b6b69d86c7af52675d210b75b0c9974fc2da6359ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025856"
---
# <a name="moving-objects"></a>移動物件

若要移動網域內的物件，請使用 [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) 方法。

**移動網域內的物件**

1.  系結至要移動之物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面。
2.  取得物件的 ADsPath 以從 [**IADs**](/windows/desktop/ADSI/iads-property-methods) 屬性移動。
3.  系結至將移至物件的容器的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。
4.  使用 [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) 方法移動物件。

如果已移動的物件有介面，則在移動物件之後，介面會無效，因為介面表示的目錄物件已不存在。

如需顯示如何移動物件的詳細資訊和程式碼範例，請參閱 [移動物件的範例程式碼](example-code-for-moving-an-object.md)。

 

 