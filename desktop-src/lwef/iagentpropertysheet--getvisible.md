---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95d1da3d1c0b4e5bf65c2f5f43c67153cc1d6af934e1814735abb12ed8d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692300"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

判斷 Microsoft Agent 屬性工作表是否可見或隱藏。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

如果屬性工作表是可見的，則為收到 **True** 的變數位址，如果隱藏，則為 **False** 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet::SetVisible**](iagentpropertysheet--setvisible.md)


 

 




