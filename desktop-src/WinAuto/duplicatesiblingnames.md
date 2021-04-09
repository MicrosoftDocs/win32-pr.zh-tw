---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675875"
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

 

 




