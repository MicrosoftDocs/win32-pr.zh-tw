---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984509"
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

 

 




