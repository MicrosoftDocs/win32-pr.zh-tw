---
description: 直接裝載
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: 直接裝載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688507"
---
# <a name="directly-hosting-a-dmo"></a>直接裝載

本章節描述應用程式如何做為 a 的直接用戶端。 應用程式會將輸入傳遞給 SQL-DMO，而是會建立輸出，而應用程式會使用輸出來呈現、進一步處理或其他任何東西。 應用程式會負責問題，例如記憶體配置、時間和同步處理，以及執行緒。 這些需求會視應用程式的本質而定。

如果您要撰寫的元件是應用程式和 (SQL-DMO 之間的層級（例如，裝載 SQL-DMO) 的 ActiveX 控制項），本節中的資訊也適用。 此外，如果您要撰寫一節，請閱讀本節，因為它描述了您的

本節包含下列主題：

-   [設定中的媒體類型](setting-media-types-on-a-dmo.md)
-   [處理 SQL-DMO 中的資料](processing-data-in-a-dmo.md)
-   [就地處理](in-place-processing.md)
-   [選用資料流程](optional-streams.md)
-   [執行 IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DMOs](using-dmos.md)
</dt> </dl>

 

 



