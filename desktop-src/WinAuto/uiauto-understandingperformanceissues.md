---
title: 瞭解效能問題
description: 本主題描述與使用 Text 和 TextRange 控制項模式相關聯的效能問題。
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- 用戶端，瞭解效能問題
- 用戶端，以文字為基礎的控制項
- 用戶端、文字範圍
- 用戶端、文字控制項模式
- 用戶端、TextRange 控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24846fea2f35cd9d265ab4f898b60dba2fc4e959b9a0f8bd7baea4661855f0a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861218"
---
# <a name="understanding-performance-issues"></a>瞭解效能問題

本主題描述與使用 [Text 和 TextRange](uiauto-implementingtextandtextrange.md) 控制項模式相關聯的效能問題。


[**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern)和 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)介面會依賴跨進程呼叫，而不會提供快取機制來改善在抓取或處理文字內容時的效能。

用戶端應用程式可以使用 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) 方法來取得中等大小的文字區塊，以改善效能。 例如，使用 **GetText** 來取出單一字元將會對每個字元產生跨進程效能的影響，而不會在呼叫 **GetText** 時指定最大長度，而會產生一個跨進程叫用，但視文字範圍的大小而定，可能會有高延遲。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Text 和 TextRange 控制項模式](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[使用以文字為基礎的控制項](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




