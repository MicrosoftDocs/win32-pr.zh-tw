---
title: " (工作排程器) 的程式設計考慮"
description: 開發使用工作排程器1.0 的應用程式時，請記住下列程式設計問題。您的應用程式必須先確認工作排程器服務正在執行，然後再嘗試使用工作排程器 API 進行任何呼叫。在抓取字串時，請確定您在不再需要每個字串之後，呼叫 CoTaskMemFree 來釋放每個字串。 在抓取字串的陣列時，請務必先釋出陣列中的每個字串，然後釋放陣列本身。建立或修改工作專案（包括與工作專案相關聯的觸發程式）時，請務必呼叫 IPersistFile Save，以將工作專案儲存至磁片。使用工作排程器 API 所提供的任何介面之後，請務必呼叫 IUnknown 版本來釋放介面。 每個工作排程器物件都支援 IUnknown。
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- 開始工作排程器
- 程式設計考慮工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa04e5987ea375dfdfc535b0d4d27b21621d2d9678bd69ea15819c8f90bffee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943616"
---
# <a name="programming-considerations-task-scheduler"></a> (工作排程器) 的程式設計考慮

開發使用工作排程器1.0 的應用程式時，請記住下列程式設計問題。

-   您的應用程式必須先確認工作排程器服務正在執行，然後再嘗試使用工作排程器 API 進行任何呼叫。
-   在抓取字串時，請確定您在不再需要每個字串之後，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放每個字串。 在抓取字串的陣列時，請務必先釋出陣列中的每個字串，然後釋放陣列本身。
-   建立或修改工作專案（包括與工作專案相關聯的觸發程式）時，請務必呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) ，以將工作專案儲存至磁片。
-   使用工作排程器 API 所提供的任何介面之後，請務必呼叫 [**IUnknown：： release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 來釋放介面。 每個工作排程器物件都支援 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。

工作排程器檔的 Using 區段提供許多遵循這些指導方針的範例。 下表提供其中一些範例的跳躍。

| 如需範例         | 請參閱                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| 釋放字串         | [正在抓取工作專案屬性範例](retrieving-work-item-property-examples.md)       |
| 將工作專案儲存至磁片 | [設定工作專案屬性範例](setting-work-item-property-examples.md)             |
| 釋放介面      | [使用 NewWorkItem 範例建立工作](creating-a-task-using-newworkitem-example.md) |



 

 

 
