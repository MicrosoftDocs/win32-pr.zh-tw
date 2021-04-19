---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968038"
---
# <a name="iagentpropertysheetsetvisible"></a>IAgentPropertySheet::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

設定 Microsoft Agent 屬性工作表的 [**Visible**](visible-property.md) 屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

可見的屬性設定。 值為 **True** 會顯示內容表; **False** 值會將它隱藏。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet：： GetVisible**](iagentpropertysheet--getvisible.md)


 

 




