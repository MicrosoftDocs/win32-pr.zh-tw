---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8d06c40fd88b525cadf9f90a1edd4edaaf3a9e9be7ccdcfa98dd6abf8b833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692641"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




