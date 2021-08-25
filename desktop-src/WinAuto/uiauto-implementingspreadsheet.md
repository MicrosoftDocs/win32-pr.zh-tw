---
title: 試算表控制項模式
description: 描述執行 ISpreadsheetProvider 的方針和慣例，包括方法的相關資訊。
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- 消費者介面自動化，執行試算表控制項模式
- 消費者介面自動化，試算表控制項模式
- 消費者介面自動化、ISpreadsheetProvider
- ISpreadsheetProvider
- 執行消費者介面自動化試算表控制項模式
- 試算表控制項模式
- 控制項模式，ISpreadsheetProvider
- 控制項模式，執行消費者介面自動化試算表
- 控制項模式，試算表
- 介面，ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7991937f1530e28ed85227fbe19be13b628f9722d5609367e2f483c86a2bb70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098278"
---
# <a name="spreadsheet-control-pattern"></a>試算表控制項模式

描述執行 [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)的方針和慣例，包括方法的相關資訊。 其他參考的連結列於主題的結尾。 **試算表** 控制項模式是用來公開試算表或其他以方格為基礎之檔的內容。

**試算表** 控制項模式與 [方格](uiauto-implementinggrid.md)控制項模式緊密相關;執行 **試算表** 控制項模式的控制項也應該執行方格控制項模式。 控制項也可以執行 [Table](uiauto-implementingtable.md) 控制項模式（如果適用）。 如需執行這些控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **試算表** 控制項模式時，請注意下列方針和慣例：

-   如果試算表實行 [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) 介面，其儲存格必須實 [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) 介面。
-   [**ISpreadsheetProvider：： GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname)方法的目的，是要提供應用程式可能會以 **跳至標籤** 功能提供的相同流覽類型。 許多試算表程式都可讓特定的資料格獲得易記的名稱或標籤。 **GetItemByName** 可讓用戶端根據其易記名稱查閱儲存格。 這個方法不應該抓取任何包含該名稱文字的資料格，因為結果可能會有極明確的混淆。 如果試算表程式允許相同試算表中的多個資料格具有相同的易記名稱或標籤，則不會定義 Microsoft 消費者介面自動化行為。

## <a name="required-members-for-ispreadsheetprovider"></a>**ISpreadsheetProvider** 的必要成員

以下是執行 [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) 介面的必要方法。



| 必要成員                                                       | 成員類型 | 備註 |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 