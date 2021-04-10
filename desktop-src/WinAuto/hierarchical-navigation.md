---
title: 階層式導覽
description: 用戶端通常必須根據其父子式關聯性，在物件之間移動。 例如，用戶端可能已經有工具列控制項的相關資訊，但沒有包含其中按鈕的相關資訊。
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183484"
---
# <a name="hierarchical-navigation"></a>階層式導覽

用戶端通常必須根據其父子式關聯性，在物件之間移動。 例如，用戶端可能已經有工具列控制項的相關資訊，但沒有包含其中按鈕的相關資訊。

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面會公開物件之間的階層式關聯性。 用戶端可以藉由呼叫 [**IAccessible：： get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 或 [**IAccessible：： get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)，從父物件移至其子系，或從子物件到父物件。

 

 




