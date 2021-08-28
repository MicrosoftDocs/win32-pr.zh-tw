---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c821d4e3686a9e454798cb80a85f3047f8cbdbaf57c075dae1361db6606d4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478592"
---
# <a name="iagentballoonsetvisible"></a>IAgentBalloon::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




