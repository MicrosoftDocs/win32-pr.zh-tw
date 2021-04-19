---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966802"
---
# <a name="iagentpropertysheetgetsize"></a>IAgentPropertySheet：： GetSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

抓取 Microsoft Agent 屬性工作表視窗的大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

接收屬性工作表寬度的變數位址（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

以圖元為單位的變數位址，此變數會接收屬性工作表的高度（以圖元為單位），相對於螢幕原點 (左上角) 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet：： GetPosition**](iagentpropertysheet--getposition.md)


 

 




