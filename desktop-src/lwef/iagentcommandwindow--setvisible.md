---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021644"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

設定 [語音命令] 視窗的 [**Visible**](visible-property.md) 屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

[**可見**](visible-property.md) 的屬性設定。 值為 **True** 時，會顯示 [語音命令] 視窗; **False** 會隱藏它。

</dd> </dl>

使用者可以覆寫這個屬性。

## <a name="see-also"></a>另請參閱

[**IAgentCommandWindow：： GetVisible**](iagentcommandwindow--getvisible.md)


 

 




