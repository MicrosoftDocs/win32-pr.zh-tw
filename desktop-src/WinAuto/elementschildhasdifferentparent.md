---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311522"
---
# <a name="elementschildhasdifferentparent"></a>ElementsChildHasDifferentParent

## <a name="text"></a>Text

專案的子 ({0}) 具有不同于元素的父 ({1}) 

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤表示在目標專案的子系上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 時，子系不會報告一致的父系。

![一個專案的子系的範例，其會報告不一致的父系](images/accchecker-inconsistent-parent.png)

此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




