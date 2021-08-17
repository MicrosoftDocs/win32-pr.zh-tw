---
title: 值屬性
description: Value 屬性提供物件中所含視覺資訊的文字標記法。 並非所有物件都支援 Value 屬性。
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcebf689016add11008b5d8249ce4eaa8adf4a99a406afea8d1267f01f94201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133271"
---
# <a name="value-property"></a>值屬性

**Value** 屬性提供物件中所含視覺資訊的文字標記法。 並非所有物件都支援 **Value** 屬性。

藉由呼叫 [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)，即可取出 **Value** 屬性。

**Value** 屬性會告知用戶端有關物件中所包含的視覺資訊。 例如，編輯控制項的值是它所包含的文字，而功能表項目則沒有任何值。

## <a name="providing-hierarchical-information"></a>提供階層式資訊

[ **值** ] 屬性會在例如樹狀檢視控制項的情況下提供階層式資訊。 雖然樹狀檢視控制項中的父物件不提供 [ **值** ] 屬性中的資訊，但控制項內的每個專案都有以零為基底的值，表示其在階層內的層級。 最上層專案的值為零，第二層專案的值為1，依此類推。

 

 




