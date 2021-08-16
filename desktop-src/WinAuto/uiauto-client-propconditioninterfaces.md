---
title: 用戶端的屬性條件介面
description: 本節說明適用于 Microsoft Win32 應用程式之消費者介面自動化用戶端的屬性條件介面。
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447c2bf9a67a5fc9cbd303e86599502e2b6154f53485af5a57bf13a6268fa930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133481"
---
# <a name="property-condition-interfaces-for-clients"></a>用戶端的屬性條件介面

本節說明適用于 Microsoft Win32 應用程式之消費者介面自動化用戶端的屬性條件介面。

## <a name="in-this-section"></a>本節內容



| 介面                                                                                  | 描述                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | 公開屬性和方法，Microsoft 消費者介面自動化用戶端應用程式可以使用這些屬性和方法來取得和屬性條件的相關資訊。 <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | 表示可以是 **TRUE** 的條件 (選取所有元素) 或 **FALSE** (不會選取) 的任何元素。<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | 這是搜尋消費者介面自動化樹狀結構中的專案時，用來進行篩選的條件主要介面。<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | 表示另一個條件中負的條件。<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | 表示由多個條件所組成的條件，至少其中一個條件必須為 true。<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | 表示以用來尋找消費者介面自動化元素的屬性值為基礎的條件。<br/>                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化用戶端](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

