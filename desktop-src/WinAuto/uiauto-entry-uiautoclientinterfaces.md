---
title: 用戶端的消費者介面自動化元素介面
description: 本節說明 Microsoft 消費者介面自動化用戶端用來尋找、存取和查詢消費者介面自動化元素的介面。
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356bd61a3f4a4626c8cc382c924b62967c01ddb201b8411eaa5451c822ede38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133411"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>用戶端的消費者介面自動化元素介面

本節說明 Microsoft 消費者介面自動化用戶端用來尋找、存取和查詢消費者介面自動化元素的介面。

## <a name="in-this-section"></a>本節內容



| 介面                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | 公開方法，可讓消費者介面自動化用戶端應用程式探索、存取及篩選消費者介面自動化元素。 消費者介面自動化會將消費者介面自動化的每個元素公開為 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面所代表的物件。 這個介面的成員並非特定專案的特定成員。<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | 擴充 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面，以公開用來控制消費者介面自動化功能的其他方法。<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | 擴充 [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) 介面，以公開用來控制消費者介面自動化功能的其他方法。<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | 擴充 [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) 介面，以公開用來控制消費者介面自動化功能的其他方法。<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | 擴充 [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) 介面，以公開用來控制消費者介面自動化功能的其他方法。<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | 擴充 [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) 介面，以公開用來控制消費者介面自動化功能的其他方法。<br/>                                                                                                                                                                                                 |
| [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | 公開快取要求的屬性和方法。 用戶端應用程式會使用此介面來指定取得消費者介面自動化元素時要快取的屬性和控制項模式。<br/>                                                                                                                                                 |
| [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | 公開消費者介面自動化元素的方法和屬性，其代表 UI 專案。 <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | 擴充 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面。 <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | 擴充 [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) 介面。 <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | 擴充 [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) 介面。 <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | 擴充 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面，以提供目前和快取的地標資料的存取權。<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | 擴充 [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) 介面，以提供目前和快取完整描述的存取權。<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | 擴充 [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6) 介面。<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | 擴充 [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7) 介面。<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | 擴充 [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8) 介面。<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | 代表消費者介面自動化元素的集合。<br/>                                                                                                                                                                                                                                                                                              |
| [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | 公開註冊新控制項模式、屬性和事件的方法。<br/>                                                                                                                                                                                                                                                                   |
| [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | 公開屬性和方法，消費者介面自動化用戶端應用程式用來查看和導覽桌面上的消費者介面自動化元素。 <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化用戶端](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





