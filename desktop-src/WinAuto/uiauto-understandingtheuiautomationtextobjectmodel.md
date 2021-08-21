---
title: 瞭解消費者介面自動化 Text 物件模型
description: 本主題說明 Microsoft 消費者介面自動化用戶端應用程式如何存取以文字為基礎之控制項的文字內容。
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- 用戶端，瞭解消費者介面自動化 text 物件模型
- 用戶端，以文字為基礎的控制項
- 用戶端、文字範圍
- 用戶端、文字控制項模式
- 用戶端、TextRange 控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655f291e9cc11d925f947617fe31be96ebd81a2dbff73506a0e474dcde9e4446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823887"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>瞭解消費者介面自動化 Text 物件模型

本主題說明 Microsoft 消費者介面自動化用戶端應用程式如何存取以文字為基礎之控制項的文字內容。

-   [控制項特定的物件模型](#control-specific-object-model)
-   [相關主題](#related-topics)

以文字為基礎的控制項透過簡單的文字物件模型，將文字內容公開給消費者介面自動化用戶端應用程式。 用戶端應用程式可以透過 [text 和 TextRange](uiauto-about-text-and-textrange-patterns.md) 控制項模式介面（包括 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 和 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)）來存取 text 物件模型。 用戶端應用程式可以使用這些介面，從以文字為基礎的控制項取出文字內容、文字屬性和内嵌物件，例如資料表和超連結。

支援消費者介面自動化 text 物件模型的控制項類型包括 [編輯](uiauto-supporteditcontroltype.md) 和 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型。 其他控制項類型（例如 [工具提示](uiauto-supporttooltipcontroltype.md) 和 [文字](uiauto-supporttextcontroltype.md) ）也可能支援 text 物件模型，但不一定要這樣做。

> [!Note]  
> 消費者介面自動化的 text 物件模型並未提供插入或修改文字的方法。 不過，某些控制項可透過 [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) 介面或透過直接鍵盤輸入來插入或修改文字。

 

## <a name="control-specific-object-model"></a>控制項特定的物件模型

以文字為基礎的控制項，其本身檔物件模型 (DOM) 可以藉由執行 [system.collections.objectmodel.observablecollection](uiauto-implementingobjectmodel.md) 控制項模式來公開 DOM。 公開 DOM 可讓用戶端應用程式更能存取及控制以文字為基礎的控制項內容。

用戶端應用程式可以藉由抓取控制項的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面，來探索特定以文字為基礎的控制項是否會實作為 DOM。 然後，呼叫 [**IUIAutomationElement：： GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) 方法，並指定 [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) 屬性識別碼，以及如果控制項執行 DOM，則會收到 TRUE 的變異。

若要存取 DOM，請呼叫 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) 方法，並指定 [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) 控制項模式識別碼，以及接收 [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) 介面的變數。 呼叫 [**IUIAutomationObjectModelPattern：： GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) 方法以取出 DOM 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Text 和 TextRange 控制項模式](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[使用以文字為基礎的控制項](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




