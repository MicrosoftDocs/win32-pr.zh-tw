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
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="c5696-103">IAgentCommandWindow::SetVisible</span><span class="sxs-lookup"><span data-stu-id="c5696-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="c5696-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c5696-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="c5696-105">設定 [語音命令] 視窗的 [**Visible**](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c5696-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="c5696-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="c5696-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c5696-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="c5696-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="c5696-108">[**可見**](visible-property.md) 的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="c5696-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="c5696-109">值為 **True** 時，會顯示 [語音命令] 視窗; **False** 會隱藏它。</span><span class="sxs-lookup"><span data-stu-id="c5696-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="c5696-110">使用者可以覆寫這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c5696-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5696-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5696-111">See Also</span></span>

[<span data-ttu-id="c5696-112">**IAgentCommandWindow：： GetVisible**</span><span class="sxs-lookup"><span data-stu-id="c5696-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 




