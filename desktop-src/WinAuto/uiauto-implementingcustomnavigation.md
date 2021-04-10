---
title: CustomNavigation 控制項模式
description: 描述執行 ICustomNavigationProvider 介面的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183452"
---
# <a name="customnavigation-control-pattern"></a>CustomNavigation 控制項模式

描述執行 **ICustomNavigationProvider** 介面的方針和慣例，包括屬性和方法的相關資訊。 **CustomNavigation** 控制項模式是用來在階層式結構中的控制項（例如清單專案、項目符號清單、編號清單和標題）之間啟用自訂導覽。 這可讓提供者描述結構，或單獨使用元素來定義可導覽的關聯性，而不只是包含控制項。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ICustomNavigationProvider** 的必要成員](#required-members-for-icustomnavigationprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在實施 **CustomNavigation** 提供者時，請注意下列方針和慣例：

-   **>positioninset**、 **SizeOfSet** 和 **Level** 的屬性值是以一為基礎的整數值。
-   **ICustomNavigationProvider** 不提供控制項的主動式操作，例如移動位置、新增和移除專案，或升級和降級層級。
-   執行 **ICustomNavigationProvider** 的控制項通常會有階層式結構，但是可以使用 **導覽** 方法略過層級。 屬性 **>positioninset**、 **SizeOfSet** 和 **Level** 需要在模式上。

## <a name="required-members-for-icustomnavigationprovider"></a>**ICustomNavigationProvider** 的必要成員

執行 **ICustomNavigationProvider** 介面需要下列屬性。



| 必要成員                                                                  | 成員類型 | 備註                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | 屬性    | 位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。 |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | 屬性    | 位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。 |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | 屬性    | 位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。 |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | 屬性    | 位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。 |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | 屬性    | 位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。 |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | 屬性    | 位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。 |
| [**導航**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | 方法      | 無                                                                                |



 

此控制項模式沒有任何相關聯的方法或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[[中] 控制項](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[HeaderItem 控制項](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem 控制項](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




