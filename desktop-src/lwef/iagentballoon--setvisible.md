---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838c34397bc089ea49579b5f6a8c7d5834c8a580
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965371"
---
# <a name="iagentballoonsetvisible"></a>IAgentBalloon::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

設定文字氣球的 [**Visible**](visible-property.md) 屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

可見的屬性設定。 值為 **True** 時，會顯示文字提示; **False** 值會將它隱藏。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentBalloon：： GetVisible**](iagentballoon--getvisible.md)


 

 




