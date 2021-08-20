---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18f0e04ed0b2aba3b0637ca8535e2ca5a18110ee29edb397fc250944035f895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115328"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Text

重複的同級名稱 + Role \\ " {0} \\ " 在元素之間會造成不明確的情況。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

專案的名稱和角色/ControlType 與另一個元素相同。

此問題可能會造成混淆，因為螢幕讀取器將會針對所有具有相同名稱和角色/ControlType 的元素讀取相同的文字。

## <a name="possible-causes"></a>可能的原因

-   元素的名稱包含角色/ControlType 文字。
-   專案的名稱或其父系的名稱未設定或設定不正確。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name 屬性](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




