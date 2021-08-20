---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115355"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Text

重複的自動化識別碼 \\ " {0} \\ " 會在元素之間造成不明確的問題。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

專案的自動化識別碼與另一個元素相同。

此問題可能會導致自動化問題，而導致測試程式碼無法參考正確的元素。

## <a name="possible-causes"></a>可能的原因

-   同級元素具有相同的自動化識別碼。
-   不正確的 UIA AutomationId 屬性執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




