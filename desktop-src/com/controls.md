---
title: '控制項 (COM) '
description: 控制項
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fb125988ad73c997772f1a07a170833b6cb36837437632aed46ba3ac0298fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919638"
---
# <a name="controls-com"></a>控制項 (COM) 

ActiveX 控制項其實只是 OLE 物件的另一個詞彙，也是更明確的 COM 物件。 換句話說，一個控制項至少是一個支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面且也可自行註冊的 COM 物件。 透過 [**IUnknown：： QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) ，容器可以管理控制項的存留期，也可以根據可用的介面，以動態方式探索控制項功能的完整範圍。 如此一來，控制項就可以在必要時執行幾乎不需要的功能，而不是支援大量不會執行任何動作的介面。 簡單來說，這種不超過 **IUnknown** 的基本需求，可讓任何控制項盡可能輕量。

簡單地說，除了 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 和自我註冊以外，還有其他控制項的需求。 不過，有一些慣例應該遵循介面的支援，其方式就是由控制項提供給容器的各項功能。 接著，本節會說明控制項實際支援介面的意義，以及控制項在支援方法、屬性和事件時，應提供作為基準的方法、屬性和事件。

如需詳細資訊，請參閱下列主題：

-   [控制項的自我註冊](self-registration-for-controls.md)
-   [介面的支援代表](what-support-for-an-interface-means.md)
-   [持續性介面](persistence-interfaces.md)
-   [控制項介面中的選擇性方法](optional-methods-in-control-interfaces.md)
-   [Class Factory 選項](class-factory-options.md)
-   [透過 IDispatch 公開屬性](properties.md)
-   [透過 IDispatch 公開方法](exposing-methods-through-idispatch.md)
-   [控制項中的事件](events-in-controls.md)
-   [屬性頁](property-pages.md)
-   [控制項的環境屬性](ambient-properties-for-controls.md)
-   [使用容器的功能](using-the-container-s-functionality.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX控制和控制容器指導方針](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




