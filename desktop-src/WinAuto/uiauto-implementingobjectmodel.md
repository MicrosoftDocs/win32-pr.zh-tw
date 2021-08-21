---
title: System.collections.objectmodel.observablecollection 控制項模式
description: 描述執行 IObjectModelProvider 的方針和慣例，包括方法的相關資訊。 System.collections.objectmodel.observablecollection 控制項模式是用來公開檔基礎物件模型的指標。
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- 消費者介面自動化，執行 System.collections.objectmodel.observablecollection 控制項模式
- 消費者介面自動化，System.collections.objectmodel.observablecollection 控制項模式
- 消費者介面自動化、IObjectModelProvider
- IObjectModelProvider
- 執行消費者介面自動化 System.collections.objectmodel.observablecollection 控制項模式
- System.collections.objectmodel.observablecollection 控制項模式
- 控制項模式，IObjectModelProvider
- 控制模式，消費者介面自動化執行 System.collections.objectmodel.observablecollection
- 控制項模式，System.collections.objectmodel.observablecollection
- 介面，IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62081f8fb841e7827f589fd2441c7b6411810f9a71c1c1962a0dfcf8b0e37180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114991"
---
# <a name="objectmodel-control-pattern"></a>System.collections.objectmodel.observablecollection 控制項模式

描述執行 [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)的方針和慣例，包括方法的相關資訊。 **System.collections.objectmodel.observablecollection** 控制項模式是用來公開檔基礎物件模型的指標。

許多應用程式會執行豐富的物件模型，以增加 Microsoft 消費者介面自動化所提供的價值。 此控制項模式可讓用戶端從消費者介面自動化元素流覽至基礎物件模型。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IObjectModelProvider** 的必要成員](#required-members-for-iobjectmodelprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **system.collections.objectmodel.observablecollection** 控制項模式時，請注意下列方針和慣例：

-   [**IObjectModelProvider：： GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel)方法應該將指標傳回至盡可能接近來源 UI 元素的物件。 例如，在網頁瀏覽器中，單一元素的消費者介面自動化提供者應該會傳回專案的物件模型指標。 傳回檔根目錄的物件模型指標並不太實用。
-   **System.collections.objectmodel.observablecollection** 控制項模式的用戶端預期會有其所要搜尋之介面的 IID，這就是它足以傳回簡單 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)指標的原因。
-   因為消費者介面自動化會將指標封送處理至用戶端進程，所以提供者應該預期用戶端必須使用標準元件物件模型來存取物件模型 (COM) 實務。

## <a name="required-members-for-iobjectmodelprovider"></a>**IObjectModelProvider** 的必要成員

以下是執行 [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) 介面的必要方法。



| 必要成員                                                                             | 成員類型 | 備註                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | 方法      | 傳回基礎物件模型的 COM 指標。 用戶端必須呼叫 [**IUnknown：： QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法，以取得特定的物件模型指標。 |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 