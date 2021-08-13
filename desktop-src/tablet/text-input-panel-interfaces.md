---
description: 本節包含用來控制 Tablet PC 輸入面板之外觀和行為的介面資訊。
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: 文字輸入面板介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2dcffe1eb67f00b4fe4d2ed3f371af003e040a30213516ae93eab73def6ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715404"
---
# <a name="text-input-panel-interfaces"></a>文字輸入面板介面

本節包含用來控制 Tablet PC 輸入面板之外觀和行為的介面資訊。

> [!Note]  
> 文字輸入面板介面不符合自動化規範。

 

## <a name="in-this-section"></a>本節內容



| 介面                                                                | 描述                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IHandWrittenTextInsertion 介面**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | 由應用程式的自訂文字專案程式碼用來將文字插入文字欄位和文字服務備份存放區。<br/> |
| [**ITextInputPanel 介面**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | 提供 Tablet PC 輸入面板的控制權。<br/>                                                                                  |
| [**ITextInputPanelEventSink 介面**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | 定義處理 [**ITextInputPanel 介面**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 事件的方法。<br/>                                      |
| [**ITextInputPanelRunInfo 介面**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | 提供方法來判斷文字輸入面板目前是否正在執行。<br/>                                                      |
| [**ITipAutocompleteClient 介面**](itipautocompleteclient.md)       | 可讓用戶端呼叫應用程式的文字輸入面板自動完成提供者物件。<br/>                                      |
| [**ITipAutocompleteProvider 介面**](itipautocompleteprovider.md)   | 管理文字輸入面板自動完成整合的應用程式端。<br/>                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




