---
description: 決定何時以及如何在應用程式中使用分界線物件時，請考慮下列事項：
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: 其他分隔因素考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193718"
---
# <a name="other-divider-considerations"></a>其他分隔因素考慮

決定何時以及如何在應用程式中使用 [**分界線**](inkdivider-class.md) 物件時，請考慮下列事項：

-   [**分隔**](inkdivider-class.md)物件是設計用來分隔繪圖和手寫區塊，但無法辨識較高層級的結構，例如資料表或資料行。
-   [**分隔**](inkdivider-class.md)物件不會提供特別用來更正版面配置分析結果的介面。
-   使用 timeout 和筆劃啟發學習法來從 [**分隔**](inkdivider-class.md) 物件中的筆劃一次新增或移除多個筆劃，可能會改善效能。

## <a name="reanalysis-considerations"></a>Reanalysis 考慮

如果您考慮在應用程式中使用 [**分割**](inkdivider-class.md) 物件，而該應用程式中的 **分隔** 物件可能必須重新分析大量筆墨，請記住下列事項。

### <a name="retaining-copies-of-ink-and-strokes"></a>保留筆跡和筆劃的複本

應用程式可以針對稍後會在應用程式會話中進行的應用程式專案，保留 [**筆跡**](inkdisp-class.md) 和 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件的複本。 如此一來，如果使用者返回專案，就不需要重新分析 **筆墨** 物件。 這種方法會將記憶體交易成更好的效能。

### <a name="data-reduction-heuristics"></a>資料縮減啟發學習法

您或許可以將分析結果記錄為應用程式資料，並執行啟發學習法來決定何時要重新分析一組筆劃。 這種作法可減少在應用程式會話之間重新分析應用程式中所有筆墨的需求。 但是，必須小心保留結構化專案界限，或重新分析受影響專案的所有筆觸。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**InkDivider 類別**](inkdivider-class.md)
</dt> <dt>

[Node.js 類別](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
