---
description: 直接裝載 DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: 直接裝載 DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f421ed470ae1d39c04054e1cb4ec6252652ed2083ea336a58525f60a6e525b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982988"
---
# <a name="directly-hosting-a-dmo"></a>直接裝載 DMO

本節描述應用程式如何作為 DMO 的直接用戶端。 應用程式會將輸入傳遞給 DMO，DMO 會建立輸出，而應用程式會使用輸出來呈現、進一步處理或其他任何東西。 應用程式會負責問題，例如記憶體配置、時間和同步處理，以及執行緒。 這些需求會視應用程式的本質而定。

如果您要撰寫的元件是應用程式和 (DMO 之間的層級（例如，裝載 DMO) 的 ActiveX 控制項），本節中的資訊也適用。 此外，如果您要撰寫 DMO，請閱讀本節，因為它會說明您的 DMO 必須執行的功能。

本節包含下列主題：

-   [在 DMO 上設定媒體類型](setting-media-types-on-a-dmo.md)
-   [處理 DMO 中的資料](processing-data-in-a-dmo.md)
-   [就地處理](in-place-processing.md)
-   [選用資料流程](optional-streams.md)
-   [執行 IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DMOs](using-dmos.md)
</dt> </dl>

 

 



